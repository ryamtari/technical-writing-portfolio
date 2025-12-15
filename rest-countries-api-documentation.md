# Rest Countries API Documentation
### Overview

The REST countries API provides information about countries around the world. Access data including country names, populations, currencies, languages, flags, and more through simple HTTP requests.


**Base URL:** https://restcountries.com/  
**Version:** 3.1  
**Authentication:** None required

---

### Getting Started
**Prerequisites**
* Basic understanding of HTTP requests
* A tool to make API calls on (browser, Postman, cURL, or code editor)
* Internet connection

**Your First Request**  
Try this simple request to get information about all countries:

`https://restcountries.com/v3.1/all?fields=name,capital,population,flags`

Copy this URL into your browser to see the response.

**Note:** The `/all` parameter endpoint requires you to specify which fields you want using the `fields` parameter to prevent large responses.

---

### Endpoints
**1. Get All Countries**  
Retrieve information about all countries.

**Endpoint:** `GET /all?fields={field1,field2,...}`  

**Parameters:**   
* `fields` (required) - Comma-separated list of fields to return

**Available Fields:** `name`, `capital`, `population`, `region`, `subregion`, `languages`, `currencies`, `flags`, `area`, `timezones`, `borders`, `cca2`, `cca3`
  
**Example Request:**
`https://restcountries.com/v3.1/all?fields=name,capital,population,region`

**Example with More Fields:**
`https://restcountries.com/v3.1/all?fields=name,capital,currencies,languages,flags`

**Response:** Returns an array of country objects with only the requested fields.

**Important:** Without the `fields` parameter, this endpoint will return a 400 Bad Request error to prevent server overload.

**2. Search by Country Name**  
Search for countries by their common or official name. 

**Endpoint:** `GET /name/{name}`  

**Parameters:** 
* `{name}` (required) - The country name or part of it

**Example Request:** `https://restcountries.com/v3.1/name/germany`  

**Example Response:**
```json
[
  {
    "name": {
      "common": "Germany",
      "official": "Federal Republic of Germany"
    },
    "capital": ["Berlin"],
    "population": 83240525,
    "region": "Europe"
  }
]
```

**3. Search by Country Code**  
Get a specific country using its ISO 3166-1 alpha-2 or alpha-3 code.

**Endpoint:** `GET /alpha/{code}`  

**Parameters:** 
* `{code}` (required) - Two-letter (alpha-2) or three-letter (alpha-3) country code

**Example Requests:**  
`https://restcountries.com/v3.1/alpha/us`  
`https://restcountries.com/v3.1/alpha/usa`

**Response:** Returns a single country object.

**4. Search by Currency**  
Find countries that use a specific currency.

**Endpoint:** `GET /currency/{currency}`  

**Parameters:** 
* `{currency}` (required) - Currency code (e.g., USD, EUR, JPY)

**Example Request:**  
`https://restcountries.com/v3.1/currency/eur`  

**Response:** Returns an array of countries using that currency.

**5. Search by Language**  
Find countries where a specific language is spoken.

**Endpoint:** `GET /lang/{language}`  

**Parameters:** 
* `{language}` (required) - Language code (e.g., spa for Spanish, fra for French)

**Example Request:**  
`https://restcountries.com/v3.1/lang/spa`  

**Response:** Returns an array of countries speaking that language.

**6. Search by Capital City**  
Find a country by its capital city.

**Endpoint:** `GET /capital/{capital}`  

**Parameters:** 
* `{capital}` (required) - Capital city name

**Example Request:**  
`https://restcountries.com/v3.1/capital/paris`  

**Response:** Returns an array of countries (usually one) with that capital.

**7. Search by Region**  
Get all countries in a specific region.

**Endpoint:** `GET /region/{region}`  

**Parameters:** 
* `{region}` (required) - One of: Africa, Americas, Asia, Europe, Oceania

**Example Request:**  
`https://restcountries.com/v3.1/region/europe`  

**Response:** Returns an array of countries in that region.

--- 

### Response Fields
Each country object contains the following key fields:
| **Field**      | **Type** | **Description**                              | **Example**                                                      |
|----------------|----------|----------------------------------------------|------------------------------------------------------------------|
| `name`         | Object   | Contains common, official, and native names  | {"common": "Germany", "official": "Federal Republic of Germany"} |
| `cca2`         | String   | ISO 3166-1 alpha-2 two-letter country code   | "DE"                                                             |
| `cca3`         | String   | ISO 3166-1 alpha-3 three-letter country code | "DEU"                                                            |
| `capital`      | Array    | List of capital cities                       | ["Berlin"]                                                       |
| `region`       | String   | Geographic region                            | "Europe"                                                         |
| `subregion`    | String   | Geographic subregion                         | "Western Europe"                                                 |
| `languages`    | Object   | Languages spoken (code: name pairs)          | {"deu": "German"}                                                |
| `currencies`   | Object   | Currencies used with name and symbol         | {"EUR": {"name": "Euro", "symbol": "€"}}                         |
| `population`   | Number   | Country population                           | 83491249                                                         |
| `area`         | Number   | Country area in km²                          | 357114                                                           |
| `borders`      | Array    | Country codes of bordering countries         | ["AUT", "BEL", "CZE"]                                            |
| `flags`        | Object   | URLs to flag images (PNG and SVG)            | {"png": "https://...", "svg": "https://..."}                     |
| `timezones`    | Array    | List of timezones                            | ["UTC+01:00"]                                                    |
| `maps`         | Object   | Links to map services                        | {"googleMaps": "https://..."}                                    |
| `tld`          | Array    | Top-level domains                            | [".de"]                                                          |
| `translations` | Object   | Country name in various languages            | {"spa": {"official": "...", "common": "..."}}                    |
| `independent`  | Boolean  | Whether country is independent               | true                                                             |
| `landlocked`   | Boolean  | Whether country is landlocked                | false                                                            |
| `flag`         | String   | Unicode flag emoji                           | "🇩🇪"                                                             |

---

### Filtering Responses
This API requires field filtering for the `/all` endpoint. Use the `fields` query parameter to specify which data fields should be returned.

**Example:** `https://restcountries.com/v3.1/all?fields=name,capital,population`

This returns only the name, capital, and population fields.

---

### Code Examples
**JavaScript (Fetch API)**
```bash
fetch('https://restcountries.com/v3.1/name/mexico')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

**Python (requests)**
```bash
import requests

response = requests.get('https://restcountries.com/v3.1/name/canada')
data = response.json()
print(data)
```

**cURL**
```bash
curl https://restcountries.com/v3.1/name/mexico
```

---

### Error Responses
**404 Not Found**  
Returned when no countries match your search.

**Example Response:**  
```json
{
  "message": "Not Found",
  "status": 404
}
```

**400 Bad Request**  
Returned when the request format is invalid.

---

### Rate Limits
While no rate limits are currently imposed, developers are expected to use the API responsibly. Best practice is to avoid excessive requests and implement caching where possible.

---

### Use Cases
**Travel & Hospitality**
* Destination research and trip planning applications
* Hotel booking platforms showing local information
* Currency conversion tools with country data
  
**Data Visualization & Analytics**
* Interactive maps and demographic charts
* Economic indicators and population trends
* International business intelligence dashboards
  
**Form Management & UX**
* Country selection dropdowns in registration forms
* Address auto-completion and validation
* Localized content based on user's country

**Business Applications**
* E-commerce platforms for international shipping
* Multi-language website localization
* Market research and regional analysis
---

### Troubleshooting
**Common Issues and Solutions**  

**Problem: Getting 404 "Not Found" Errors** 

**Possible Causes:** 
* Incorrect country name spelling
* Using non-English country names
* Country name variations

**Solutions:**
  1. Verify the country name spelling
  2. Use the common English name (e.g., "South Korea" not "한국")
  3. Try alternative names: "United States" or "USA" or "America"
  4. Use the country code endpoint if you know the ISO code

**Example:**

**Problem: Response Takes Too Long** 

**Possible Causes:**
* Fetching all countries (/all endpoint)
* Not filtering fields
* Network latency
* Large response size

**Solutions:**
1. Use specific endpoints instead of `/all`
2. Filter fields to return only what you need:
   
```bash
/all?fields=name,capital,population
```
4. Implement caching (see Performance Considerations)
5. Use pagination if processing many countries

**Problem: Missing or Undefined Data Fields**

**Possible Causes:**
* Not all countries have fields
* Some countries have no capital or multiple capitals
* Field names changed in API version

**Solutions:**
1. Always check if fields exist before accessing:
```bash
const capital = country.capital ? country.capital[0] : "N/A";
```
2. Use optional chaining in JavaScript:
```bash
const currency = country.currencies?.USD?.name ?? "Unknown";
```
3. Provide fallback values for missing data

**Problem: CORS Error in Browser**

**Error Message:** 
```bash
Access to fetch has been blocked by CORS policy
```
**Cause:** Your web application is being blocked by browser security

**Solutions:**
1. This API supports CORS, so check your request syntax
2. Ensure you're using HTTPS, not HTTP
3. Test in a different browser to rule out extensions
4. If developing locally, use a local server instead of opening HTML files directly

**Problem: Rate Limiting or Blocked Requests**

**Possible Causes:**
* Too many requests in a short amount of time
* Using `/all` endpoint repeatedly
* Bot-like behavior patterns

**Solutions:**
1. Implement caching to reduce requests
2. Add delays between requests
3. Use specific endpoints instead of `/all`
4. Consider storing data locally

**Problem: Inconsistent Language or Currency Data**

**Cause:** Countries may have multiple languages or currrencies

**Solutions:** 
1. Languages and currencies are returned as objects, not arrays
2. Extract all values if you need them:
```bash
const languages = Object.values(country.languages).join(", ");
   const currencies = Object.values(country.currencies)
     .map(c => c.name)
     .join(", ");
```

---

### Performance Considerations
Understanding how to optimize your application's speed and efficiency when using the REST Countries API.

**Caching Strategies**  

Country data is well suited for caching because it changes infrequently. Details such as capital cities, population figures, and national flags typically remain stable over long periods.

**Types of caching:**
* In-memory caching
* Browser storage
* Server-side caching

**Recommended cache duration:**
* All countries list: 7 days (data rarely changes)
* Individual country data: 24-48 hours
* Flag images: 30 days (almost never change)

**When to refresh cache:** Set a expiration time on your cached data. When data is older than this time, fetch fresh data from the API and update your cache.

---

**Query Optimization**

Query optimization is the process of selecting the most efficient method to retrieve exactly the data you need, without extra information.

**Use Specific Endpoints**

**The principle:** Always use the most specific endpoint available for your needs. For example, instead of fetching 250 countries and filtering for the 50 European ones you require, request data directly from a dedicated European countries endpoint.

**Endpoint selection guide:**
| **Your Goal**                      | **Best Endpoint**                    | **Why It's Better**                         |
|------------------------------------|--------------------------------------|---------------------------------------------|
| Find one specific country          | `/name/{country}` or `/alpha/{code}` | Returns only the country you need           |
| Get countries in a region          | `/region/{region}`                   | Filters server-side, reducing data transfer |
| Find countries using a currency    | `/currency/{code}`                   | Pre-filtered by the API                     |
| Find countries speaking a language | `/lang/{language}`                   | Returns only relevant matches               |

**Avoid:** Fetching all countries with `/all` and then filtering on your end. This downloads unnecessary data and slows your application.

---

**Field Filtering**

**The Principle:** Only request the data fields you actually need. For example. if you only require country names and flag images, do not request additional fields such as population, area, languages, or other attributes.

**How it works:** Use the `fields` query parameter to specify exactly which fields you want returned. The API will send only those fields, response size by up to 80%.

**Example Use Cases:**
* **For a dropdown menu:** Fetch only the `name` field.
* **For a summary card:** Fetch only `name`, `capital`, `population`, and `flag`.
* **For a search:** Fetch `name` and relevant searchable fields.
* **For a full profile:** Fetch all necessary display fields.

**Remember:** The `all` endpoint requires the `fields` parameter. Without it, you'll receive a 400 error.

---

**Bandwith Considerations**  
Bandwidth is the amount of data transferred over a network. Minimizing data transfer is critical for faster loading times and a better user experience, especially on mobile devices or slow connections.

**Response Size Comparison**  
Different API requests transfer significantly different amounts of data. Choose the most efficient request for your use case.

| **Request Type**           | **Approximate Size** | **Best Used For**                    |
|----------------------------|----------------------|--------------------------------------|
| Single country, all fields | ~5 KB                | Detailed country profile pages       |
| Single country, 3-5 fields | ~1 KB                | List items, search results           |
| All countries, 3-5 fields  | ~200 KB              | Dropdown menus, complete directories |
| One region, minimal fields | ~30-50 KB            | Regional browsing interfaces         |

**Impact of optimization:** Applying field filtering can reduce response sizes by 60–80%, significantly accelerating your application.

**Best Practices by Application Type**

**Mobile Applications**
* Fetch only essential fields on the initial load.
* Load detailed data on-demand (e.g., when a user selects a country).
* Implement client-side caching to avoid redundant requests.
* Schedule large dataset downloads for WiFi connections.

**Web Applications**
* Apply field filtering for list, grid, and search views.
* Request complete data only for individual detail pages.
* Implement lazy loading or pagination for long lists.
* Cache static assets and frequently accessed data.

**Offline-First Applications**
* Pre-download full datasets over WiFi.
* Store data locally for offline access.
* Implement periodic background syncs for updates.
* Clearly indicate when data is stale or being refreshed.

---

**Strategic Querying**

**Choose Specific Endpoints for Targeted Needs**  
Use precise endpoints like `/name/{country}` or `/alpha/{code}` when:
* You know exactly what you are looking for.
* Real-time accuracy is critical.
* Minimizing bandwidth is a priority.
* Responding directly to a user’s search.

**Choose Broad Endpoints for Batch Operations**  
Use wider endpoints like `/all` or `/region/{region}` when:
* You need data for multiple countries at once.
* Populating selection menus, dropdowns, or directories.
* Implementing client-side search or filtering.
* You can cache the result set for reuse.

**The Principle: Minimize Sequential Requests**  
Instead of making multiple API calls in a loop, fetch a broader, relevant dataset once. Then, filter and use the data locally. This reduces network overhead and improves performance.

---

**Performance Monitoring**  
Tracking key metrics helps you identify bottlenecks, validate the effectiveness of your optimizations, and ensure your application scales efficiently.

**Key Metrics to Track**

**Response Time**
* **Target:** <500ms for single countries; <1000ms for regions.
* **Purpose:** Measures network and API latency. Indicates overall system health.

**Cache Hit Rate**
* **Target:** 80% or higher.
* **Purpose:** Measures how often requests are served from cache versus the API. A high rate validates your caching strategy.

**Error Rate**
* **Target:** <1% of total requests.
* **Purpose:** Tracks failures (404s, timeouts, network errors). Helps identify reliability issues.

**Bandwidth Usage**
* **Target:** Monitor trends over time.
* **Purpose:** Quantifies total data transferred. Highlights opportunities for further optimization, crucial at scale.

---

**Common Performance Mistakes** 

**Fetching Inside Loops:** Making separate API calls for each item in a loop multiplies network overhead and slows your application. Instead, fetch the required dataset once (using a broader endpoint if necessary) and iterate through the local result.

**Over-Fetching Data:** Requesting all available fields when you only need a few wastes bandwidth and increases latency. Always use the `fields` parameter to retrieve only the data you will use.

**Ignoring Error Handling:** Network requests can and will fail. Applications without proper error handling (e.g., try/catch blocks, user-friendly fallback messages) will crash or hang, providing a poor user experience.

**Skipping Loading States:** Users need visual feedback. Always implement loading indicators (spinners, skeleton screens) during data fetches so users know the application is responding.

**Neglecting Cache Invalidation:** Cached data becomes stale. Without an expiration or refresh strategy, users may see outdated information. Implement time-based expiration or manual refresh triggers.

---

**Performance Optimization Checklist**  
Before deploying your application, confirm you have implemented:    
✅ **Caching** for static or infrequently changed data.  
✅ **Field filtering** on all requests to minimize response size.  
✅ **Specific endpoints** instead of fetching /all and filtering client-side.  
✅ **Error handling** for all network requests and API calls.  
✅ **Loading states** to provide user feedback during data fetching.  
✅ **Cache expiration** to ensure data does not become stale.  
✅ **Performance monitoring** to track key metrics and identify bottlenecks.  

---

### Best Practices
1. **Cache API responses** to minimize repeated calls
2. **Filter response fields** to reduce data transfer
3. **Implement error handling** for reliable user experience  
4. **Choose specific endpoints** over general searches
5. **Add delays between rapid requests** to avoid overwhelming the API
6. **Store common data locally** for instant access
7. **Monitor API usage** to identify optimization opportunities

---

### Support and Resources
* **Official Website**: [restcountries.com](https://restcountries.com)
* **GitHub Repository**: [apilayer/restcountries](https://github.com/apilayer/restcountries)
* **Issue Tracking**: [Report issues](https://github.com/apilayer/restcountries/issues) via GitHub Issues
* **API Status**: Monitor GitHub for service updates and downtime notifications

---

### Frequently Asked Questions
**Q: Is authentication required?**  
A: No, the API is completely open and requires no authentication.

**Q: Can I use this in production?**  
A: Yes, the API is free for commercial and non-commercial use.

**Q: How often is the data updated?**  
A: The data is updated periodically as country information changes.

**Q: What format does the API return?**  
A: All responses are in JSON format.  

---

### Version History
**v1.0** (Current)

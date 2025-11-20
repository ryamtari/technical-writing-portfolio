# Rest Countries API Documentation
### Overview

The REST countries API provides information about countries around the world. Access data including country names, populations, currencies, languages, flags, and more through simple HTTP requests.


**Base URL:** https://restcountries.com/v3.1  
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
| **Field**    | **Object** | **Description**                            |
|--------------|------------|--------------------------------------------|
| `name`       | Object     | Contains common and official country names |
| `capital`    | Array      | List of capital cities                     |
| `population` | Number     | Country population                         |
| `region`     | String     | Geographic region                          |
| `subregion`  | String     | Geographic subregion                       |
| `languages`  | Object     | Languages spoken (code: name pairs)        |
| `currencies` | Object     | Currencies used                            |
| `flags`      | Object     | URLs to flag images (PNG and SVG)          |
| `area`       | Number     | Country area in km²                        |
| `timezones`  | Array      | List of timezones                          |

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

### Storing Country Data in a Database

---

### Troubleshooting

---

### Performance Considerations

---

### Best Practices

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

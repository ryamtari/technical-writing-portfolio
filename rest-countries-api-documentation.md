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

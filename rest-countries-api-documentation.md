# Rest Countries API Documentation
### Overview

The REST countries API provides information about countries around the world. Access data including country names, populations, currencies, languages, flags, and more through simple HTTP requests.


**Base URL:** https://restcountries.com/v3.1  
**Version:** 3.1  
**Authentication:** None required

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

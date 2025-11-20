# Rest Countries API - Quickstart Tutorial
### Build Your First Country Information Application in 10 Minutes
This tutorial will walk you through creating a simple web page that displays country information using the REST Countries API.

**What You'll Build**
A web page where users can search for a country and see its flag, capital, population, and region.

**Prerequisites**
* A text editor (Notepad, VS Code, or any code editor)
* A web browser (Chrome, Firefox, Safari)
* No programming experience required.

---

### Step 1: Create Your HTML File
Create a new file called `country-finder.html` and add this code:
```bash
<!DOCTYPE html>
<html>
<head>
    <title>Country Finder</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
        }
        .search-container {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
        }
        input {
            padding: 10px;
            flex: 1;
            font-size: 16px;
            box-sizing: border-box;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            white-space: nowrap;
        }
        #result {
            padding: 20px;
            border: 1px solid #ddd;
            border-radius: 5px;
            box-sizing: border-box;
            width: 100%;
        }
        img {
            width: 100px;
            margin: 10px 0;
        }
    </style>
</head>
<body>
    <h1>Country Finder</h1>
    
    <div class="search-container">
        <input type="text" id="countryInput" placeholder="Enter country name (e.g., Japan)">
        <button onclick="searchCountry()">Search</button>
    </div>
    
    <div id="result"></div>

    <script>
        function searchCountry() {
            // Get the country name from input
            const countryName = document.getElementById('countryInput').value;
            
            // Make API request
            fetch(`https://restcountries.com/v3.1/name/${countryName}`)
                .then(response => response.json())
                .then(data => {
                    // Get the first country from results
                    const country = data[0];
                    
                    // Display the results
                    document.getElementById('result').innerHTML = `
                        <h2>${country.name.common}</h2>
                        <img src="${country.flags.png}" alt="Flag">
                        <p><strong>Capital:</strong> ${country.capital}</p>
                        <p><strong>Population:</strong> ${country.population.toLocaleString()}</p>
                        <p><strong>Region:</strong> ${country.region}</p>
                        <p><strong>Language(s):</strong> ${Object.values(country.languages).join(', ')}</p>
                    `;
                })
                .catch(error => {
                    document.getElementById('result').innerHTML = 
                        '<p style="color: red;">Country not found. Please try another name.</p>';
                });
        }
    </script>
</body>
</html>
```

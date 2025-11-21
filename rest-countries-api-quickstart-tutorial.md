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

---

### Step 2: Test Your App
1. **Save the file** as `country-finder.html`
2. **Open it** in your web browser (double-click the file)
3. **Type a country name** (try "Japan" or "Brazil")
4. **Click Search**

You should see the country's information appear.

---

### Step 3: How It Works
Let's break down the important parts:  

**The API Request**
```bash
fetch(`https://restcountries.com/v3.1/name/${countryName}`)
```
This line sends a request to the REST Countries API with the country name you typed.  

**Processing the Response**
```bash
.then(response => response.json())
.then(data => {
    const country = data[0];
    // Display the data
})
```
This converts the API response to JSON format and extracts the first country from the results.  
**Error Handling**
```bash
.catch(error => {
    // Show error message
})
```
If the country isn't found, this displays a friendly error message.

---

### Troubleshooting
**Problem:** Nothing happens when I click Search.
**Solution:** Check the browser console (F12) for error messages. Make sure you're connected to the internet.

**Problem:** I see "Country not found" for valid countries.
**Solution:** Try using the country's common English name or name variations (e.g. "Islamic Republic of Iran" instead of "Iran").

**Problem:** The page looks broken.
**Solution:** Make sure you copied all the code and correctly saved the file with a `.html` extension. Also ensure all the HTML tags are properly closed.

---

### Next Steps
Now that you've built your first application with the REST Countries API, here are some ideas to enhance it:
1. **Improve styling:** Add color, different fonts, or a background image
2. **Add more features:** Display neighboring countries or timezone information
3. **Filter by region:** Create buttons to show all countries in Europe, Asia, etc.
4. **Save favorites:** Let users bookmark countries they're interested in

---

### What You Learned
* How to make API requests using JavaScript
* How to handle API responses
* How to display data dynamically on a webpage
* How to Handle Errors Properly

Congratulations! You've successfully integrated the REST Countries API into a working application.

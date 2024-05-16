# web-scraping-challenge

## Module 11 Challenge

For this challenge, I scraped two websited for Mars data, particularly related to news and weather on the planet. I was instructed to scrape titles and text from the news articles about Mars, as well as scrape and analyze Mars weather data from a table. Using Splinter and BeautifulSoup, I was able to scrape via automated browsing, and then perform anlyses on the resulting data.

### Part 1: Mars Data

For the first part, I used automated browsing to visit the Mars news site (https://static.bc-edx.com/data/web/mars_news/index.html). I then extracted all text elements for each article on the page under the *div* class *list_text*. I then stored the results in a Python dictionary, with the __title__ as the key and the __preview__ text as the value. To do this, I looped through each article and extracted these elements, placed them in a temporary dictionary, and appended the dictionary to a blank list. At the end, I printed all the titles and preview texts to confirm it was sucessfully queried.

As an optional bonus, I set a path to a JSON file and wrote the resulting array to the JSON file for easier sharing with others. This file is in the __Resources__ directory.

### Part 2: Mars Weather

For the second part, I used automated browsing once more to visit the Mars Temperature Data Site (https://static.bc-edx.com/data/web/mars_facts/temperature.html). Here, there is an HTML table with the data, and after extracting the elements of the table, I stored the data in a Pandas DataFrame by looping through each row and assigning the values to an array of variables, while also defining the column names accordingly. After, I prepared the data for analysis by changing the data types for certain columns (either *integers*, *floats*, or *datetime*). I then used the DataFrame to answer the following questions:

1. How many months exist on Mars?
    * I counted the frequency of each month for the dataset and printed the results.
2. How many Martian (and not Earth) days worth of data exist in the scraped dataset?
    * 1867 days.
3. What are the coldest and the warmest months on Mars (at the location of Curiosity)?
    * Coldest month: March (3).
    * Warmest month: Auguest (8).
    * For this answer, I also plotted the results as 2 bar charts.
4. Which months have the lowest and the highest atmospheric pressure on Mars?
    * Lowest pressure: June (6).
    * Highest pressure: September (9).
    * I also plotted the results as a bar chart.
5. About how many terrestrial (Earth) days exist in a Martian year?:
    * It is roughly 675 days, according to the dataset.
    * I visually represented this by making a line chart of the minimum temperatures for the number of days recorded in the dataset.

At the end, I saved the DataFrame to a CSV file in the __Resources__ directory.
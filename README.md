# Web-Scrapping-Ebay, API Call, and MySQL Database

Part 1 MySQL Database

Creates a database “msba”. Within the database, creates the table “ip_addresses” in “msba” containing the columns “ip”, “city”, and “zip”.

Part 2 API Call

1. request free API from https://ipstack.com/
2. Write 4 URL strings that return the “main” fields in JSON format for IP addresses “8.8.8.8”, “128.120.0.25”, “128.32.12.14”, “64.165.72.144”, and your IP address
3. Create a program in Python or Java that executes above five API calls and prints the result to screen.
4. Parse the JSON strings in previous step to an internal Python object for further handling. Then write code that iterates through the five API requests and prints the “city” and “zip” fields to screen. 
5. Import it into MySQL database

Part 3 Web Scrapping

Ebay's President’s Day Deals: https://www.ebay.com/e/daily-deals/hiw-presidents-day-deals-white-sale
1. Loop through first 10 pages to save all URLs for each item, save all URLs in to a local file 'deals.txt'
2. Write a program that opens the file 'deals.txt' and downloads each of the pages (URLs) into the folders "deals". Each file should be named as "<item-id>.html" where you want to replace "item-id" with the ID of the item you are saving. E.g., "264616053293.html" for the item with ID "264616053293".
3.Write a separate piece of code that loops through the pages you downloaded in (2) and opens and parses them into a Python object. Identify and select: seller name, seller score, item price, item price, list price, # items sold, title, returns allowed (true / false), shipping price, condition (e.g., used, new, like new, seller refurbished, ...).
4.Save the information of items in (3) into a single table named "deals" in “msba”. Convert any price (item price and shipping price) into a "dollar-cent" format (e.g., convert $12.34 into 1234 and $12 into 1200. Insert the price as INT into the table
5.Run summary stats on each item based on conditions and whether there is listing price avaliable on the page. 

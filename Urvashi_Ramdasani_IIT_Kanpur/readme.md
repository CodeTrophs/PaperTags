## Accessing IIT Kanpur Faculty Data - Using Web Scraping

The notebook consists the code for getting faculty data from IIT Kanpur website using web scraping in Python. It uses the following packages - 

1. requests (2.23.0)
2. bs4 (0.0.1)
3. lxml (4.2.6)

The notebook uses requests.get(url) method to get the HTML content of the entered url in response. This response is pretified using soup.pretify() in lxml format. Using the 
find_all method, we find out all the divs with class as jwts_content and then the text inside the p tag. This text is appended to a list and later on information is extracted
from the list using simple string slicing. The information contains the name of the faculty, email address, phone number and department. In the end, some corrections are made 
to correct for missing data on the website (Eg. Environment Engineering and Management). All the extracted information is converted to a dataframe and then to a csv file.

The website was last accessed on 9 December 2020. To get the data, simply execute the notebook and download the output csv file. 

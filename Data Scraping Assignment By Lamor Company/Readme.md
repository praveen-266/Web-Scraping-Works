# Data-Scraping-Engineer-Task

#### Overview and Approach

* This code is an implementation of a web scraper using the Selenium library in Python. The scraper is designed to extract data from the website "https://lawrato.com/free-legal-advice" by navigating through multiple pages and scraping information from each page's HTML.

* The code begins by importing the necessary modules, including Selenium, JSON, Markdown, and time. It then defines the base URL and the number of pages to scrape. 

* The keys variable is used to define the keys for the JSON file that will store the scraped data. The html_to_markdown function is defined to convert HTML tables to Markdown format.

* The main function, scrape_website, is where the actual scraping takes place. It starts by creating an empty list to store the scraped data. Next, it sets up the Selenium driver using the Chrome browser.

* The code then loops through the specified number of pages and loads each page in the browser. It waits for 5 seconds to allow the page to load completely. The code then finds all the question boxes on the page using the class name 'question-box'.

* For each question, the code extracts the title and content by locating the corresponding elements in the HTML using XPath. If there is an error in extracting the data, a warning message is printed and the code continues to the next question.

* The content is then converted from HTML to Markdown using the html_to_markdown function. The title and content are added to the data list as a dictionary.

* After scraping all the pages, the data is written to a JSON file named 'data.json'.

* Finally, the browser is closed using the quit() method.

* The code can be executed by calling the scrape_website function.


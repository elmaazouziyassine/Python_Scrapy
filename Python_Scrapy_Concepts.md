http://quotes.toscrape.com/

(venv) C:\Users\ELMAAZOUZI\Desktop\Python Projects\scraper\myProject>scrapy crawl quotes



CSS Selectors


### Scrapy Shell : 
Scrapy Shell helps to control Scrapy in command line mode. 
- (venv) C:\Users\ELMAAZOUZI\Desktop\Python Projects\scraper>**scrapy shell "http://quotes.toscrape.com/"**
- (venv) C:\Users\ELMAAZOUZI\Desktop\Python Projects\scraper>**scrapy shell "https://www.amazon.fr/books/s?k=books"**

>>> response.css(".a-color-base.a-text-normal::text").extract()

Extracting data w/ CSS Selectors
- \>>> response.css("title")
- \>>> response.css("title").extract()
- \>>> response.css("title::text").extract()
- \>>> response.css("title::text")[0].extract()
- \>>> response.css("title::text").extract_first()
- \>>> response.css(".author::text").extract()

For complex website, we need a tool to find the css selectors (like small.author, title...)
add this extenstion to google chorm navigator : https://chrome.google.com/webstore/detail/selectorgadget/mhjhnkcfbdhnjickkkdbjoemdmbfginb?hl=en

Easy, powerful CSS Selector generation.
Selector Gadget is an open source Chrome Extension that makes CSS selector generation and discovery on complicated sites a breeze.

After having installed the extension, go to any page and launch it. A box will open in the bottom right of the website. Click on a page element that you would like your selector to match (it will turn green). SelectorGadget will then generate a minimal CSS selector for that element, and will highlight (yellow) everything that is matched by the selector. Now click on a highlighted element to remove it from the selector (red), or click on an unhighlighted element to add it to the selector. Through this process of selection and rejection, SelectorGadget helps you come up with the perfect CSS selector for your needs.

There is a tutorial video and a bookmarklet version available at http://selectorgadget.com


Python Scrapy Tutorial - 10 - Extracting data w/ XPATH
2 types of Selectors :
- CSS Selectors
- XPATH Selectors


-\>>> response.xpath("//title/text()").extract()
-\>>> response.xpath("//span[@class='text']/text()")[0].extract()
-\>>> response.css("li.next a").xpath("@href").extract()
>>> response.css("a").xpath("@href").extract()


https://stackoverflow.com/questions/52678981/scrapy-spider-gives-an-error-in-processing

Python Scrapy Tutorial - 12 - Item containers ( Storing scraped data )

Extract data --> Temporary containers (items) --> store in a file

# Web Scraping

## Reading
* [Web Scrape with Python in 4 min](https://towardsdatascience.com/how-to-web-scrape-with-python-in-4-minutes-bc49186a8460)
* [What is Web Scraping?](https://towardsdatascience.com/how-to-web-scrape-with-python-in-4-minutes-bc49186a8460)
* [How to scrape websites without getting blocked?](https://www.scrapehero.com/how-to-prevent-getting-blacklisted-while-scraping/)

## Videos
* [Track Amazon Prices](https://www.youtube.com/watch?v=Bg9r_yLk7VY)

### Bookmark & Review
* [Beautiful Soup](https://www.youtube.com/watch?v=Bg9r_yLk7VY)

* Web scraping is a technique used to automatically access and extract large amounts of data from a website.
* Web scraping a.k.a data mining
* ***Note:***
  * Read the site's Terms and Conditions to understand HOW you can LEGALLY use the data.
  * Make sure you are not downloading the data at too fast a rate. If you cause their site to crash... you could get 
  blocked.
* Imports needed:
  * requests
  * urllib.request
  * time
  * bs4 from BeautifulSoup
* Techniques used:
  * Human copy & paste
  * Text pattern matching with regex
  * HTTP programming -> the use of HTTP requests to a socket programming
  * HTML parsing
  * DOM parsing
  * Vertical aggregation -> create and monitor "bots"
  * Semantic annotation recognizing
  * Computer vision web-page analysis
* Web Scraping best practices:
  * Respect Robots.txt -> follow the site's robot.txt file for good behavior
  * Crawl slower -> the faster you crawl the worse it is for all of us
  * Do not follow the same crawling pattern -> this helps to avoid intelligent anti-crawling mechanisms
  * Make requests through proxies and rotate them often
  * Rotate `user-agents` and corresponding `HTTP request headers` between requests
  * Use a headless browser:
    * Puppet
    * Selenium
    * Playwright
  * Beware of Honey Pots
  * Avoid scraping behind a login
  * Use captcha solving services
  
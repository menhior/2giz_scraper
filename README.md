# 2giz_scraper
2giz scraper implemented in bs4 and selenium(python).

To use:
1)Install mozilla firefox webdriver and set path to it. (https://www.browserstack.com/guide/geckodriver-selenium-python)
2)Change url to scrape in scraper file to the search query that you are interested in and last value in the for loop range, The last value should be the number of pages that you will be scraping plus 1. 
So if there are 50 pages in the search query you are going to scrape set it to be 51. You can also change output file name, for how it better fits you. 
3)After getting output file, either change its name to combined.xlsx or change the input file name in check_duplicates.py and proceed with running it to clean the dataset from identical lines.

if you want scraper to stop openning windows in the browser add following:

from selenium.webdriver.firefox.options import Options as FirefoxOptions

options = FirefoxOptions()
options.add_argument("--headless")
driver = webdriver.Firefox(options=options)

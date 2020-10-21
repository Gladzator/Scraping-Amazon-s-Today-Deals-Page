# Scraping Amazon's Today Deal Page

## Table of Content
  * [Motivation](#motivation)
  * [What to Scrape?](#what-to-scrape)
  * [Installation](#installation)
  * [Technical Approach](#technical-approach)
  * [Run](#run)
  * [Technologies/Libraries Used](#technologieslibraries-used)
  * [Team](#team)


## Motivation
I am always trying to improve myself and in my quest of learning webscraping I wanted to scrape a website which wasn't really going to be straightforward. Amazon is used by millions of people worldwide and the data it holds surely must be of use to many. I decided to scrape Amazon's Today Deal page with the same intention.

## What to Scrape?
Following is the content of each product from the website (https://www.amazon.in/gp/goldbox/) being scraped:
  1. Product Name
  2. Product Price
  3. Prime Deal (whether benefit of prime user is available)
  4. Product Rating
  5. Product URL
  
## Installation
The Code is written in Python 3.7.6. If you don't have Python installed you can find it [here](https://www.python.org/downloads/). If you are using a lower version of Python you can upgrade using the pip package, ensuring you have the latest version of pip. To install the required packages and libraries, run this command in the project directory after [cloning](https://www.howtogeek.com/451360/how-to-clone-a-github-repository/) the repository:
```bash
pip install -r requirements.txt
```
Additionally, you will need chromedriver version to be same as your Google Chrome version.
  - Open Google Chrome.
  - Visit "chrome://settings/help" and check your version.
  - Get chromedriver similar to your version from https://sites.google.com/a/chromium.org/chromedriver/home and replace the one provided with this new one.
  
## Technical Approach
Scraping mainly involves inspecting the html of the website and writting the required correct XPath in case of Scrapy. Since, Amazon is a website based on javascript, the need for selenium arose. Thus, the required changed in settings.py were made too. 

As an entire page was scraped, next button was clicked to navigate into further pages and scrape them too. This was continued until next button existed. This was particularly tricky at first as Amazon's html page isn't quite straightforward.

To learn more about Scrapy, click [here](https://scrapy.org/).

To learn more about Selenium, click [here](https://selenium-python.readthedocs.io/).

## Run
To run this scrapy project, you need to open your Terminal/Command Prompt and navigate to the root of this project.
```bash
scrapy crawl todaydeal -o data.json
```
todaydeal is the name of the spider while data.json denotes the name and type of output file. You can save it in either xml, csv or json formats by just changing the extensions.

## Technologies/Libraries Used
![](https://forthebadge.com/images/badges/made-with-python.svg)

[<img target="_blank" src="https://repository-images.githubusercontent.com/529502/dab2bd00-0ed2-11eb-8588-5e10679ace4d" width=100>](https://scrapy.org/)
[<img target="_blank" src="https://selenium-python.readthedocs.io/_static/logo.png" width=100>](https://selenium-python.readthedocs.io/)

## Team
<img src="https://avatars2.githubusercontent.com/u/40065133?s=460&v=4" width="200" height="200">|
-|
Yash Vora

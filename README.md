## Colorado Crawler Wikipedia

Welcome to the **Colorado Crawler Wikipedia** project, a solution designed for extracting and analyzing web data from Wikipedia pages related to Colorado. This Python toolkit is specifically tailored for web scraping, data cleaning, and geolocation extraction, offering an easy way to find datasets for an LLM or RAG system according to your specified keywords and weights.

## Features

- **Web Scraping**: Utilize `COCrawler.py` to crawl web pages and gather the data you need.
- **Data Cleaning**: Employ `cleaner.py` to refine your URL's by removing unnecessary or redundant information, ensuring a cleaner analysis.
- **TXT to CSV**: Use `CSVConverter.py` to convert the txt files and summaries to CSV. This will allow the LLM to ingest the data we have crawled. 
- **Geolocation Extraction**: With `GeoLocator.py`, extract geographical information and summaries and attach it to each article.
- **Word Cloud Analysis**: Run `WordCloud.py` to regenerate weights for your crawler. This will scrape each URL you crawled and create a word cloud analysis for the most common words.
- **Easy Setup**: Quick installation with a simple `requirements.txt` file to manage all necessary dependencies.

## Getting Started

### Dependencies

Ensure you have Python installed on your system. This project requires several dependencies that can be installed via pip.

```bash
pip install -r requirements.txt
```

### Installing

- Clone the repository and set up the environment:

```bash
git clone https://github.com/LukeFarch/COCrawlerWiki.git
cd COCrawlerWiki
```

- Change the paths in the code as necessary to match your environment and needs.

### Executing the Program

- To start crawling Wikipedia for Colorado-related pages, run:

```bash
python COCrawler.py
```

- For data cleaning:

```bash
python cleaner.py
```

This ensures all URLs can be accessed and scraped for information.

- To extract geolocation data:

```bash
python GeoLocator.py
```

This will scrape coordinates using the `geo-dec` class on Wikipedia pages.

- Convert the txt files you crawled to CSV: Use this after using GeoLocator.py. 

```bash
python CSVConverter.py
```

This ensures all CSV's include a summary, coordinates, and a link. This will be used to ingest and embed this data with our LLM

- Run a word cloud analysis off the URL's you crawled.

```bash
python WordCloud.py
```

This will help you regenerate weights and words to exclude which help make your crawler more efficient for the data you're searching for. 



## Authors

- **Luke Farchione (J4eva)** - Visit [www.0xFarch.com](http://www.0xFarch.com) 

## TODO:

- [x] Implement Word Cloud Analysis on the extracted pages from Wikipedia.
- [x] Update the weights based on Word Cloud Analysis results.
- [x] Add additional data cleaning functions.
- [ ] Improve the efficiency of the web scraping process.
- [ ] Write comprehensive documentation for all new features.



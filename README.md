# Scraper for prnt.sc

## Introduction
The website [LightShot or prnt.sc](https://prnt.sc/) is a public image sharing website which is most well known for its quick and easy 
downloadable sharing utility activated by pressing the PrtScn key. It's a very useful tool, however I noticed that it stores images
based on a sequential 6 digit code, meaning the 1.3 billion or so images uploaded there can be indexed programmatically quite easily. 
That is what this utility will do.

## Pre-requisites

This script was tested on the following python modules, however earlier/later versions may work fine:

```
- python 3.6
- requests 2.8.1
- beautifulsoup4 4.6.0
- lxml 3.8.0
```

## Using the Script

The script takes 3 arguments as follows:

* ```--start_code```: 6 character string made up of lowercase letters and numbers which is where the scraper will start.
  * e.g. ```lj9me9```
* ```--count```: The number of images to scrape.
  * e.g. ```200```
* ```--output_path```: The path where images will be stored.
  * e.g. ```output/```
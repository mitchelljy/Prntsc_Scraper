# Scraper for prnt.sc

## Introduction
The website [LightShot or prnt.sc](https://prnt.sc/) is a public image sharing website which is most well known for its quick and easy 
downloadable sharing utility activated by pressing the PrtScn key. It's a very useful tool, however I noticed that it stores images
based on a sequential 6 digit code, meaning the 1.3 billion or so images uploaded there can be indexed programmatically quite easily. 
That is what this utility does.

## Pre-downloaded Dataset

I have already published a set of around 13,000 images downloaded from the site [on Kaggle](https://www.kaggle.com/datasnaek/lightshot/home)
which may be of use if you do not want to use the scraper utility.

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
  
## Uses/Explanation

It can be very interesting to see what people upload to these sites, generally having sequential IDs of any type is bad, and the
same applies here. People might not be aware that what they are uploading is visible to others, however prnt.sc/lightshot have 
not shown any inclination in wanting to change their site design.

As a result, this provides a useful way to create datasets of real world images. A useful/interesting use case is building a machine
learning algorithm to classify images into categories, which requires some manual classification, but is nonetheless interesting
and a good learning task.

# Licensing
 
This project is released under the MIT license, see LICENSE.md for more details.
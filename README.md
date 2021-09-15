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
- faker 8.11.0
```

## Using the Script

The script takes 4 arguments as follows:

* ```--start_code```: 6 or 7 character string made up of lowercase letters and numbers which is where the scraper will start.
  * e.g. ```lj9me9```
* ```--count```: The number of images to scrape.
  * e.g. ```200```
* ```--output_path```: The path where images will be stored.
  * e.g. ```output/```
* ```--resume_from_last ```:If files allready exist in the output get last created/modified and resume from there,default=True

  
## Uses/Explanation

It can be very interesting to see what people upload to these sites, generally having sequential IDs of any type is bad, and the
same applies here. People might not be aware that what they are uploading is visible to others, however prnt.sc/lightshot have
not shown any inclination in wanting to change their site design.

As a result, this provides a useful way to create datasets of real world images. A useful/interesting use case is building a machine
learning algorithm to classify images into categories, which requires some manual classification, but is nonetheless interesting
and a good learning task.

### Sequential is a poor practice
     --start_code values on prnt.cs is sequential, so from image context...
     14akf6 ~ Oct 2013
     999997 ~ Jan 2015
     a9998j ~ Feb 2016
     h4akgb ~ Oct 2017
     sp2gna ~ May 2020 ;sp2nuo=2020-05-27;sp2v18=2020-05-27;sp2v7o=2020-05-28
     z4akga ~ Feb 2021
     10000am ~ Feb 18, 2021; 100001g=2021-02-18;10000rt=2021-02-18-194850
     1qrrrav ~ Aug 30, 2021
     
## Licensing

This project is released under the MIT license, see LICENSE.md for more details.

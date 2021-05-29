# Programming with advanced computer languages - IMDBscraper and subsequent analysis of the data

## Authors
* Nils Martens
* Wouter Hendriks
* Daniel Zimmermann
* Moritz Daendliker


## Background

This repository is part of a project from the course "Programming with advance computer languages" at the University of St. Gallen which was held in the spring semester 2021 as part of contextual master studies.

## About the project

The aim of the following project was to scrape the IMDb homepage for data on the 250 best-rated movies. The code subsequently cleans the dataset, provides some descriptive statistics before concluding with an analysis of different factors while also considering data from further datasets in the analysis. Further details of each part are provided below.

## How to execute this code

1. as the underlying html code on the IMDb page was completely redone after our scraper was built, most parts will not work anymore. However, the datasets needed to execute the code where gathered prior to the launch of the new homepage and can all be found within the repository. Thus, there is no need for further data download.

2. Make sure that the appropriate packages are loaded and installed.

3. Run code files sequentially and use functions as further elaborated in the specific chunk of code.

### Note on code components
This code was written by using Conda by using packages from the Anaconda repository as well as from the Anaconda Cloud. By using Conda there was no need to have compilers available to install those packages. Additionally, the packages are not not limited to Python software and might alos contain C or C++ libraires, R packages or even further software.


## Project Structure

### Scraper

The scraper used the free library of Beautiful Soup which allowed to scrape HTML and XML content from the IMDb homepage on te top 250 movies (the presen homepage can be found under the following link: https://www.imdb.com/chart/top/). 13 different characters were scrapped, including .... 


## Disclaimer

This code was used for research-purposes only. 

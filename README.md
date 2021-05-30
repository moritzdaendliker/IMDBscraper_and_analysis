# Programming with advanced computer languages - IMDb scraper and subsequent analysis of the data

## Authors
* Moritz Daendliker
* Wouter Hendriks
* Nils Martens
* Daniel Zimmermann



## Background

This repository is part of a project from the course "Programming with advance computer languages" at the University of St. Gallen which was held in the spring semester 2021 as part of contextual master studies.

## About the project

The aim of the following project was to scrape the most important platform for movie ratings (IMDb homepage) for data on the 250 best-rated movies. The code subsequently cleans the dataset, provides some descriptive statistics before concluding with an analysis of different factors while also considering data from further datasets in the analysis. Further details of each part are provided below.

## How to execute this code

1. as the underlying html code on the IMDb page was completely redone after our scraper was built, most parts of the scraper will not work anymore. However, the dataset needed to execute the code was gathered prior to the launch of the new homepage and can be found within the repository (imdb_top_movies). Thus, there is no need for further data download or rerunning the scraper. The user can thus directly start with file 2: data preparation & descriptive statistics.

2. Make sure that the appropriate software packages are loaded and installed.

3. Run code files sequentially and use functions as further elaborated in the specific chunk of code.

## Note on code components
This code was written by using Conda by using packages from the Anaconda repository as well as from the Anaconda Cloud. By using Conda there was no need to have compilers available to install those packages. Additionally, the packages are not limited to Python software and might alos contain C or C++ libraires, R packages or even further software.

## Project Structure
Our project was structured around three sets of codes

### Scraper (file name: 1. Scraper)

The scraper used the free library of Beautiful Soup which allowed to scrape HTML and XML content from the IMDb homepage on the top 250 movies (the homepage can be found under the following link: https://www.imdb.com/chart/top/). 13 different characters were scrapped, including the movie name, the year, the rating, the number of reviews, the genre, the production country, the language, the budget, the box office revenue as well as the running time. The data was then stored as a csv file for further processing (imdb_top_movies). Note that IMDb has completely changed their website structure in the past days and that the scraper therefore does not work on the new website.

### Data Preparation & descriptive Stats (file name: 2. Data Preparation & descriptive statistics)
After the csv file was loaded, we first gained an overview of the data by looking at the first five rows and also having a look at the datatypes of all scraped characteristic. After that, strings were splitted, NA's ommitted, unnecessary signs such as brackets etc. were removed so that the data was ready for the subsequent analysis. 
First, a bar chart showing the distribution of the movies according to their runtime (incl. the mean value) was created. Subsequently, the movies were separated according to genre. This split was then visualized with a pie chart. Similarly, the movies were grouped according to the country of origin, again visualized with a pie chart. Subsequently an interactive tool was created in which the user can check how many movies are available in a language of his choice. Some movies are available in more than one language, which was also accounted for.
Further insight was gained by counting and visualizing the splits according to country in which the movies were produced 

### Data Analysis (file name: 3. Analysis)
Last but not least, the data was further processed and analysed. After a rating classification dsiplayed in a table according to genre and decade, a candle chart was built in order to visually determine if ratings have in general changed over time. We additionally analysed if the rating is impacted by the runtime of a movie. 

In a next step, the starring and the directors of the movies were further looked at. As each movie potentially had multiple mentions of actors which participated in the cast, the string had to be splitted in order to be able to count how many times single actors were mentioned. The user can tell the programm how many top actors (according to number of starrings in top 250 movies) he would like to display and can also check whether (and also how many times) his most favorite actor/actress was casted in one of the top movies. In addition, a ranking of top directors (measured by revenue) was created.

Last but not least, this paper wanted to analyse whether the share of female actresses in the cast is a determinant of the revenue-based succes of a movie. In order to allow for this, a second database of names and a corresponding gender classification had to be loaded (retrieved from: https://parseapi.back4app.com/classes/Complete_List_Names?limit=250000).
In a next step, all actors were classified as either gender according to their first names. This allowed to a) count the number of male/female actors/actresses across all top 250 movies but also allowed to calculate a female ratio for each movie. The latter was then ultimately used to run a regression and determine if movies with a higher ratio of male actresses yielded higher box office revenues. A further regression was executed to determine if higher ratio of males per movie was associated with higher ratings. For both analyses, not statistically signifficant relationships could be foumd.

## Disclaimer

This code was used for research-purposes only. 

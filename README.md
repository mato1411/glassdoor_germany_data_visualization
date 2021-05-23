# Glassdoor Germany Data Exploration
The project is about wrangling and exploring a Glassdoor dataset to gain insights about the German job market in the field of data science and related disciplines. In particular the job listings with focus on the relationship of job titles, locations, number of employees and industry will be investigated. Additionally, reported salaries for job titles of the job listing employers will be examined. This notebook covers two parts. The first part are data wrangling techniques that are used to obtain the data for the exploratory analyses. This analyses represents the second part and will focus on the use of data visualizations techniques.

## Motivation
I live in Munich, Germany and enrolled Udacity's Data Analyst Nanodegree program to deepen my knowledge of data analysis. This project was submitted as part of this program in order to demonstrate the importance and value of exploratory and explanatory data visualization techniques in the data analysis process. I choose to select not any of the given Udacity datasets, because I wanted to search and find a dataset focusing on the German job market in the field of data science and related disciplines for this project. Besides the data visualization tasks, I wanted to train my data wrangling techniques, too.

## Dependencies
Ensure that you install the packages to run the [Jupyter Nootebooks](#files).

 Requirements generated for conda environment:
`conda list -e >` [conda_requirements.txt](conda_requirements.txt)

Requirements generated using pip:
`pip freeze > `[pip_requirements.txt](pip_requirements.txt)


## Dataset
The examination relies on the dataset provided by André Sionek on [Kaggle](https://www.kaggle.com/andresionek/data-jobs-listings-glassdoor). The information provided on Kaggle and the [GitHub repository](https://github.com/andresionek91/Job-Listing-Scraper) states how the data was scraped and prepared. The data was scraped on the 10th of December 2019 from [Glassdoor](https://www.glassdoor.co.uk). 

The dataset was cleaned and prepared using wrangling techniques.

## Files

### Datasets used for Data Wrangling
* [`data/glassdoor.csv.gz`](data/glassdoor.csv.gz): Job listings - **Please download the file from [Kaggle](https://www.kaggle.com/andresionek/data-jobs-listings-glassdoor/?select=glassdoor.csv), because it exceeds the GitHub upload limit of 100M.**
* [`data/glassdoor_salary_salaries.csv.gz`](data/glassdoor_salary_salaries.csv.gz): Reported salaries for employers of job listings (downloaded from [Kaggle](https://www.kaggle.com/andresionek/data-jobs-listings-glassdoor))
* [`data/currency_exchange.csv`](data/currency_exchange.csv): Currency exchange rates for the date the Glassdoor data was scraped (downloaded from [Kaggle](https://www.kaggle.com/andresionek/data-jobs-listings-glassdoor))

### Cleaned Datasets used Exploratory and Explanatory Data Analysis
* [`data/glassdoor_cleaned.csv.gz`](data/glassdoor_cleaned.csv.gz): Cleaned job listings data for Germany
* [`data/salaries_cleaned.csv.gz`](data/salaries_cleaned.csv.gz): Cleaned reported salaries data for employers of job listings

### Data Wrangling and Exploratory Data Analysis
* [`glassdoor_germany_exploration.ipynb`](glassdoor_germany_exploration.ipynb): Jupyter Notebook; Code for data wrangling and EDA using visualization techniques
* [`glassdoor_germany_exploration.html`](glassdoor_germany_exploration.html): HTML export of `glassdoor_germany_exploration.ipynb`

### Explanatory Data Analysis
* [`glassdoor_germany_exploration_slides.ipynb`](glassdoor_germany_exploration_slides.ipynb): Jupyter Notebook; Code for nbconvert slideshow
* [`glassdoor_germany_exploration_slides.html`](glassdoor_germany_exploration_slides.html): HTML presentation

## Key Insights

### For what kind of job in the field of data science and related disciplines in Germany should you apply?
Based on the job listings, the companies with up to 200 employees in the Internet Industry are looking especially for Software Engineers in Berlin.

### What's the median salary for such a job in Germany?
Smaller companies have higher median base salaries for Software Engineers compared to larger companies. The median base salary is between 33,000 and 58,000 Euro.

### Looking for a higher salary?
The highest median base salaries with approx. 72,000 Euro have been reported for Product Managers of companies with more than 10,000 employees. Product Manager in Internet industry have a median salary of roughly 82,000 Euro.

Product Manager jobs are listed in companies with the companies with up to 200 employees or with more than 10000 employees in the Internet industry in Berlin as well as in München.


## Acknowlegdement, License & Disclaimer
Many thanks to André Sionek for providing this dataset on [Kaggle](https://www.kaggle.com/andresionek/data-jobs-listings-glassdoor). The data is available under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International Public License (CC BY-NC-SA 4.0). This data analysis project was done for personal educational purposes only. The author does not have any connection to Glassdoor.
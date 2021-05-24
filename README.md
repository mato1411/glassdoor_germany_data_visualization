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

## Summary of Findings

### Job Listings

I found that there was a strong relationship between the qualitative features of main interest: Job Title, Location, Industry and Company Size. Outside of those main variables, I verified the relationship with the date when a job listing was posted. THis did not lead to any suprising interaction.

Following findings were revealed by the exploration:
* Approx. 54% of the job listing records have no null values for the features Title, City, Industry and Company Size.
* For approx. 90% of the job listings a normalized job title could be assigned. The Engineering Manager and Scrum Master job listing are outliers only covering 10 records.
* For roughly 80% of the job listings records the company size in terms of number of employees is known. Those job listings are well distributed among all company sizes. Companies with more than 10000+ employees provide the most job listings (25%). The two smallest companies sizes have the next highest shares with each almost 20%.
* The city is known for 96% of the job listings. The top 10 out of 344 unique locations are representing 65% of the job listings that have a location provided. 55% of the records that have a location are within the top 5 locations. Berlin has the highest frequency with more than 25%.
* For only 64% of the job listings the employer industry is known. The top 10 out of 91 unique industries are representing 60% of the job listings that have an industry provided. 47% of the records that have an industry are within the top 5 industries. The Internet industry has the highest frequency with more than 16%. It's remarkable that the top 4 industries are IT-related and sum up to a share of approx. 40.5%.
* Small companies count more job listings for Product Owner than large companies. Software Engineers and Data Engineers are the most listed among all company sizes.
* Especially in Berlin, but also in München (Munich) and Köln (Cologne) Software Engineer listings have the highest share. The second largest share in Berlin by far is Product Manager. 
* Job listings of Software Engineers have the largest share in Internet, Computer Hardware & Software and Enterprise Software & Network Solutions by far. In IT Services and Consulting industry it's a large share, but not the largest. Instead Data Engineers are most listed for those industries. The second largest share in Internet industry by far is Product Manager.
* For companies with 10000+ employees, Berlin lists the most Data Scientists, Business Analysts, Machine Learning Engineers and Reseacher. The largest listing counts for such companies are for Data Scientists, Data Analysts, Business Analysts and Project Manager in Frankfurt am Main.
* In Berlin companies with 51 to 200 employees list the most jobs for Data Engineer, Data Analyst, Product Owner and Product Manager.
* Companies with 1 to 50 employees have in München the most listed jobs for Software Engineers, Data Scientists, Data Analysts and Project Managers.
* In 3 out of 5 locations are Software Engineers most listed for companies with 1 to 50 employees.
* In 3 out of 5 locations are Product Owners the most listed for companies with 51 to 200 employees.
* Companies with more than 10000+ employees provide listings for Business Analysts for 3 out of 5 locations.
* The focus of the Internet industry is Berlin. The listing for all job titles besides for Product Owners have the highest frequency in Berlin for the Internet Industry. In 3 out of 5 locations are Software Engineers for the Internet industry the most listed.


### Salaries

I found that there was a strong relationship between the qualitative features of main interest Job Title, Industry and Company Size and the quantitative features Low, Median and High Base Salary. Outside of those main variables, I verified the relationship with the count of reported base salaries. This lead to suprising interactions.

Following findings were revealed by the exploration:
* 21% of the records have no null values for the features Job Title, Industry and Company Size, Low, Median and High Base Salary.
* Still, only 5 of the normalized job titles taken from the job listings present a signifigant share (97%) of the reported salaries.
* 5 times more salaries have been reported for Software Engineers (67%) compared to the second largest number of reported salaries for Project Manager (13%). For Business Analyst 11%, for Product Manager 5% and 3% for Researcher have been reported.
* The highest average salaries are reported for Product Managers by far.
* Companies with 10000+ employees have the largest counts of reported salaries for each of the top 5 job titles: Software Engineers, Business Analysts, Project Manager, Product Manager and Reseacher (ranked by count; Software Engineers have the largest count by far, which is approx. 8 times larger than the second largest count for Business Analysts and Project Manager)
* Software Engineers in Internet industry have the largest count of reported salaries by far, which is approx. 10 times larger than the second largest count across the top 5 job titles and industries
* The Internet industry has the largest count among the top 5 normalized job titles
* Product Manager have the highest median salary of companies with 10000+ employees and considering all company sizes for the top 5 normalized job title. 
* Larger companies have higher median salaries for Product Manager and smaller companies have higher median salaries for Software Engineers.
* Product Manager have the the highest median salary reported in Internet industry, which equals the highest salary among the top 5 industries and job titles.


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
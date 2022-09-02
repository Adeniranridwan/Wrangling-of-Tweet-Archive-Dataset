# Wrangling-of-Tweet-Archive-Dataset

# Table of Contents

Project title
About the Project
Project Summary
Prerequisites
dataset
Credit

# Project Title:
Wrangling of Tweet Archive Dataset
    
# About the project:
This project is on Wrangling and Analysis of tweet archive dataset of Twitter user @dog_rates also known as WeRateDogs to create interesting and trustworthy analyses and visualizations

# Project Summary
WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. The numerators, though? Almost always greater than 10. 11/10, 12/10, 13/10, etc. Why? Because "they're good dogs Brent." WeRateDogs has over 4 million followers and has received international media coverage.

Data wrangling is the process of removing errors and combining complex data sets to make them more accessible and easier to analyze.

Wrangling Process was carried out on three messy datasets which are:

twitter archive enhanced which was readily available by udacity
json file that supposed to be screaped from twitter API
image prediction that was downloaded with request method

These datasets above needed thorough cleaning. The datasets was said to have both quality and tidiness issues after being assessed manually and programmatically. some of the quality and tidiness issues solved are:

#Quality:

twitter_achieved_enhanced

The datatypes of these columns(tweet_id, in_reply_to_status_id, in_reply_to_user_id, retweeted_status_user_id, retweeted_status_user_id) should be in string not float.

The columns (timestamp,retweeted_status_timestamp) are stored as object rather than datatime

The columns (doggo, floofer, pupper, puppo) all have a value 'None' present instead of 'Nan'

The columns 'name' have some odd values such as 'a', 'the' as the stage name

The columns(expanded_urls) have some duplicated value

Columns that contain Retweet data (retweeted_status_id,retweeted_status_user_id and retweeted_status_timestamp) are not needed. we only want to work with real tweets NOT retweets

Also columns that contain reply tweets data(in_reply_to_status_id, in_reply_to_user_id) are not needed since they are not the real tweets

image-predictions.tsv

tweet_id is stored in int instead of string

many tweet_id have a duplicated jgp_url

json_ file

tweet_id is stored in int instead of string

columns like (doggo, floofer, pupper, puppo) should be melt in a single column.

All dataset should be merge into one under tweet_id

# Tidiness

columns like (doggo, floofer, pupper, puppo) should be melt in a single column.

All datasets should be merge into one under tweet_id.


The above issues were solved.


After the cleaning was performed, then, Anlaysis was carried out and finally perform explantory visualization to draw an toughtful insights.

Some of the insights deduced from the Visualization at the end of the Analysis are:

The most common dog class by frequency. Doggo

What is the most common dog breed? golden_retriever.

what is the correlation between retweet and favorite count? 0.91

Which day of the week has the most average retweet_count? Monday

Which month of the year has the most average retweet_count? December

Which year has the highest retweet_count? 2016

What are the most common tweet sources? Iphone tweets

# Dataset:
you can find the dataset here:
twitter-archive-enhanced :  https://d17h27t6h515a5.cloudfront.net/topher/2017/August/59a4e958_twitter-archive-enhanced/twitter-archive-enhanced.csv
image prediction: https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv
json file: scraped from twitter

# Require for the project:
- Intergrated Development Environment
- python 3
- Installed python packages
- Access to twitter API

# Credit:
Google
Stackover


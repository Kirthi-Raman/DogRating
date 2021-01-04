# DogRating

This project considers a dataset consisting of various dog details and performs data wrangling to create a good dataset which can be applied in various analysis.<br>

## Data Wrangling Report

The ‘WeRateDogs’ Twitter dataset has been wrangled to create a good data source which is clear of all the dataset cleanliness issues and can be understood and directly used for further analysis.<br>
The steps followed in data wrangling the ‘WeRateDogs’ Twitter dataset are:<br> 
1)	Gather
2)	Assess
3)	Clean

#### Gather:
There are three datasets used in this project:<br>
1)	The 'twitter-archive-enhanced.csv' has been manually downloaded from the Udacity link and its data has been saved in Pandas dataframe ‘archived’.
2)	The image tweet predictions data 'image-predictions.tsv' has been gathered from Udacity's server by downloading it using requests library and saving it in project workspace. Its data has been saved in Pandas dataframe ‘images’.
3)	Twitter JSON data has been gathered by accessing project data without Twitter account. It is then saved into Pandas dataframe ‘tweets’ by using requests library.<br>

#### Assess:
The three dataframes are explored and thoroughly understood to detect the Quality and tidy issues in the data table. Eight quality issues and two tidiness issues are identified.<br>

##### Quality Issues
In archived' table,
1)	Column 'timestamp' and 'retweeted_status_timestamp' are of type 'object', instead of being datetime.
2)	Column 'rating_numerator' has a maximum value of 1776, which seems to be an anomaly. Any numerator value greater than 1000 can be considered as abnormal.
3)	Column 'rating_denominator' has 23 count of values that are not 10. There is one value with denominator 0 which is a clear case of anomaly.
4)	Tweet ids without expanded_urls values.
5)	Expanded_urls should include the tweet_id after the keyword 'status'.
6)	There are retweet ratings.
7)	In columns: doggo, floofer, pupper and puppo, Nulls represented as 'None'.
In tweets table,
8) Column name of Tweet IDs is 'id’.

##### Tidy Issues:
1)	The 'retweet_count' and 'favorite_count' columns should be a part of archived table.
2)	In the 'images' table, the prediction of algorithms: p1, p2 and p3 are given as column names, instead of values. Similarly, the confidence level of algorithm's prediction: p1_conf, p2_conf and p3_conf are given as column names instead of values. Also, prediction correctness p1_dog, p2_dog and p3_dog is given as column names instead of values.

#### Clean: 
The cleaning process is performed in a sequence of 3 steps: Define, Code and Test on a copy of the initially saved three dataframes: ‘archived’, ‘images’ and ‘tweets’ i.e., ‘archived_clean’, ‘images_clean’ and ‘tweets_clean’.<br>
Each of the eight quality issues and two tidiness issue cases are cleaned thoroughly to overcome the given issue and correct it inorder to make it suitable for further analysis.<br>
The final dataframes of the data wrangling process are ‘archived_clean’ and ‘images_clean’.<br>


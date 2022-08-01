# We_Rate_Dogs_Data_Wrangling_Project

## **Project Overview**
This project is about gathering data from different sources manually and programmatically
and wrangling the data. The main purpose of the project is to master the act of data gathering and wrangling messy and untidy data.
The project phases as follows"
- Step 1: Gathering data
- Step 2: Assessing data
- Step 3: Cleaning data
- Step 4: Storing data
- Step 5: Analyzing, and visualizing data
- Step 6: Reporting

## **Dataset Overview**
The datasets used in this project is the WeRateDogs Twitter archive data. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. The numerators, though? Almost always greater than 10. 11/10, 12/10, 13/10, etc. Why? Because "they're good dogs Brent." WeRateDogs has over 4 million followers and has received international media coverage.
In order to complete the project, I used the **Twitter archive csv file**, and programatically downloaded the **image prediction tsv file** provided by Udacity. I shall also used the Twitter API to collect data from Twitter on retweets and favourite counts. 

## **Summary of Data Wrangling Processes employed**
**Data Gathering**

I started the wrangling process by gathering:
- the twitter_archive_enhanced dataset which was provided by Udacity.
- The image_prediction dataset was downloaded programmatically using the URL
provided by Udacity.
- Finally, I downloaded the additional data which contained retweets and favourite
tweets using Twitter API. User IDs derived from the twitter_archive_enhanced were
useful in helping download the right data needed for the wrangling process.

**Assessment of the Data**

After getting all my three datasets, I proceeded to assess the data visually and
programmatically using codes. Visual assessment of the twitter_archive_enhanced data was
done first by loading the data into excel to see if I can see some patterns.
The programmatic assessment was however done after by using the info, describe,
value_counts, duplicated, sample, isnull, etc.
This was done in essence to track quality and tidiness issues associated with the datasets.
Quality issues included missing values, duplicate values, incorrect data types, outliers, etc.
I also checked for the tidiness of the data where I looked at issues related to the structure of
the data. Issues such as some columns containing more than one value were identified and
rectified in the data cleaning process.

**Data Cleaning**

The data cleaning stage was the next. At this stage, I followed the Define, Code, Test
procedure, which I used in rectifying all the issues identified during the assessment stage.
Before I started cleaning, I made a copy of the datasets I gathered. Changing data types,
stripping texts, replacing values, dropping columns, etc were some of the actions I took
during this stage of the wrangling process.
The datasets were merged into one data frame using the merge and join functions.
The data was then stored in a master data frame called the twitter_archive_master at the
storing stage of the wrangling process.
Finally, some analysis was done on the merged data, where I looked at how each of the
three algorithms predicted the dog breeds accurately. The confidence intervals were also
assessed. I checked the correlation between key variables retweet count and favourite
counts and found out how strongly and positively correlated they were. I also generated a
word cloud to see some of the most prevalent words used in the texts

## **Summary of findings**
### **Insight 1**
---
* After cleaning, the numerators in the rating_numerator column look moderate considering the denominator assigned.

* The confidence interval for p3 seems most stronger as it has about 49% of its prediction within a 5% margin of error and most of the 49% below 2.5%.

* The p1_conf algorithm seems to have the worst confidence level as most (99.6%) of its predictions fall above the 5% margin of error.

### **Insight 2**
---
p1_dog shows that the p1 algorithm has predicted about 74% of the breed of dogs correctly,the p3_dog algorithm predicted 72% whereas the p2_dog algorithm predicted about 76% correctly

### **Insight 3**
---
* The correlation coefficient between retweet count and the favorite count is 0.85, which shows that there is a strong positive relationship between these two metrics.

### **Insight 4**
---
Wednesdays seems to have the most retweets and favourite counts.
Both retweets and favourite counts seems to have a positive correlation which explains the fact that people retweet tweets the like 

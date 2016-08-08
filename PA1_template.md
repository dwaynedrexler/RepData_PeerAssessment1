# Reproducible Research: Peer Assessment 1
Dwayne Drexler  


## Loading and preprocessing the data
1. Download the file from the internet using the web address given in the
   instructions:

```r
fn = "https://d396qusza40orc.cloudfront.net/repdata%2Fdata%2Factivity.zip" 
download.file(url=fn, destfile="activity.zip", method="curl")
```
2. Extract the data from the zip file.

```r
unzip("activity.zip")
```
3. Read in the dataset:

```r
library(dplyr)
data <- tbl_df(read.csv("activity.csv", sep=","))
```
4. Some data exploration.
  a. Histogram of total number of steps taken each day:

```r
data %>% 
  group_by(date) %>%
  summarize(total_steps = sum(steps))
```

```
## Source: local data frame [61 x 2]
## 
##          date total_steps
## 1  2012-10-01          NA
## 2  2012-10-02         126
## 3  2012-10-03       11352
## 4  2012-10-04       12116
## 5  2012-10-05       13294
## 6  2012-10-06       15420
## 7  2012-10-07       11015
## 8  2012-10-08          NA
## 9  2012-10-09       12811
## 10 2012-10-10        9900
## ..        ...         ...
```




## What is mean total number of steps taken per day?



## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?

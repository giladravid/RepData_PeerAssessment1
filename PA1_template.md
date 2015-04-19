# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data
The First step is to load the data. We will create  a temporary file, download the zip file and extract it into mydata data frame object.

```r
temp_data <- tempfile()
download.file("https://d396qusza40orc.cloudfront.net/repdata/data/activity.zip",temp_data,method="curl")
mydata <- read.csv(unz(temp_data, "activity.csv"),sep=",",na.strings="NA")
mydata$date<-strptime(mydata$date,"%Y-%m-%d")
unlink(temp_data)
str(mydata)
```

```
## 'data.frame':	17568 obs. of  3 variables:
##  $ steps   : int  NA NA NA NA NA NA NA NA NA NA ...
##  $ date    : POSIXlt, format: "2012-10-01" "2012-10-01" ...
##  $ interval: int  0 5 10 15 20 25 30 35 40 45 ...
```

## What is mean total number of steps taken per day?



## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?

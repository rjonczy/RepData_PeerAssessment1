# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data

Unzip `activity.zip` file if `activity.csv` doesn't exists current directory.

```r
if(!file.exists('activity.csv')) {
    unzip('activity.zip')
}


activitiesData <- read.csv('activity.csv')
```


## What is mean total number of steps taken per day?



## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?

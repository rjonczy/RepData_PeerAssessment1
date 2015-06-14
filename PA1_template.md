# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data

Unzip `activity.zip` file if `activity.csv` doesn't exists in current directory. 


```r
if(!file.exists('activity.csv')) {
    unzip('activity.zip')
}

activitiesData <- read.csv('activity.csv')
```


## What is mean total number of steps taken per day?

Mean value of steps taken per day I've calcuated in variable `meanPerDay`.

### Total number of steps per day

```r
totalPerDay <- aggregate(steps ~ date, activitiesData, sum)
```

Here, I plot a histogram of steps per day
###

```r
hist(totalPerDay$steps, xlab='Mean of steps by day', breaks=10)
```

![](PA1_template_files/figure-html/unnamed-chunk-3-1.png) 

### 


```r
mean(totalPerDay$steps)
```

```
## [1] 10766.19
```

```r
median(totalPerDay$steps)
```

```
## [1] 10765
```


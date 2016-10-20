# Change context on R Server


To develop R code locally and deploy on Spark/Hadoop Server, all I need to do is rewrite the first two lines of RevoScaleR code:

```R
## Setup local environment variables
myLocalCC <- "localpar"
# to work with Spark change this to:
# mySparkCC <- RxSpark()

## Local compute context
rxSetComputeContext(myLocalCC)
# to work with Spark change this to:
# rxSetComputeContext(mySparkCC)
```

The rest of the code does not change:
```R
rxSummary( ~ ArrDelay + DayOfWeek, data = AirlineData, reportProgress = 1)
...
```
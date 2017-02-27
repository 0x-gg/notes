Set the working dir

```r
setwd("/..")
```

Plotting linear regression line

```r
plot(data)
abline(lm(data$dependent ~ data$independent))
```
NROW for vectors, nrow for data frames.
[see SO](http://stackoverflow.com/questions/27674937/why-do-ncol-and-nrow-only-yield-null-when-i-do-have-data#27674980)


```r
# To put numeric column names in a string
check.names = F

# Removes the spaces in the columns
make.names = T
```

Classes of columns
```r
sapply(test, class)
```

Sum of non-NA values across columns
```r
colSums(!is.na(train))
```

Correlation matrix
```r
cor(train)
```

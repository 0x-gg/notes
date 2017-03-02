### Index

##### Plotting - INFX 573: Lecture 3


See the class of the data
```r
class()
```

Generating sequences
```r
1:10
seq(1, 10, length.out = 10) # generate sequence between these numbers
seq(1,10, length.out = 20) # fractional output
seq(1,10, by = 0.5) # step output
```


Working directory related

```r
setwd("/..")
getwd()
```

Descriptive functions
```r
dim() # dimensions of data object
nrow() # number of rows
ncol() # number of columns
length() # length of vector/list
head()
tail()
colnames()
rownames()
```

Applying functions over rows or columns
```r
apply(somedataframe, 1, sum) # sum over rows
apply(somedataframe, 2, sum) # sum over columns
```

Working with groups of data with by()
```r
by(groupedvalue, groupbythisvalue, groupingfunction)
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

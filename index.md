---
title       : Estimate the Expected Circumference of your Orange Tree
subtitle    : Ensure expected growth
author      : Christine
job         : Data Science Student
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Orange Tree Issues

Have you ever wondered if your orange trees were growing appopriately in their first approximately 6 years?



--- .class #id 

## Worry No More

R has a built in dataset called Orange that tracks age and circumference of orange trees!

```r
head(Orange)
```

```
##   Tree  age circumference
## 1    1  118            30
## 2    1  484            58
## 3    1  664            87
## 4    1 1004           115
## 5    1 1231           120
## 6    1 1372           142
```


## If Only Someone Built An App..

There is now a Shiny App that uses a simple linear model predictions to predict the circumference of your orange tree based on age!

---

## How good is the model?

Judge for yourself.  User assumes all risks of improper model and use.  Application provided for informational purposes only.


```r
orangemodel<-lm(Orange$circumference~Orange$age)
summary(orangemodel)$coef
```

```
##               Estimate  Std. Error   t value     Pr(>|t|)
## (Intercept) 17.3996502 8.622659801  2.017898 5.179267e-02
## Orange$age   0.1067703 0.008276623 12.900228 1.930596e-14
```

---

## Where is this fantastic thing?

https://acct252000.shinyapps.io/orangetrees/

Note:  In 5 page requirement, assumed title(first) page counted as 1.


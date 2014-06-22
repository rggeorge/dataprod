---
title       : The best geyser-prediction app on the market
subtitle    : 
author      : Ryan
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [quiz]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---


## The need
  
  Nearly three million people* visit Yellowstone each year. Waiting an average of 70 minutes per eruption, this adds up to 7 human lifetimes of waiting to see the site.

* source: [Yellowstone Park Foundation](http://www.ypf.org/site/News2?page=NewsArticle&id=5267)


--- &radio

## Quick question 

If you go to Yellowstone, how long will you generally have to wait for the eruption to happen?

1. 5 minutes
2. 15 minutes
3. It depends on the time of day
4. _It depends on how long the most recent eruption was_
5. It is ompletely unpredictable 

*** .hint 

Hint: The answer is not choice 5.

---

## A new model

It's clear that people need to know how long to wait for Old Faithful.

We've developed a groundbreaking new algorithm to help tourists better plan their time.  We call it "Old Calculatorful".  The code is below.


```r
data(faithful)
mod <- lm(waiting ~ eruptions, data=faithful)
erupt_time <- 10
wait_time <- as.numeric(mod$coefficients[1])  + as.numeric(mod$coefficients[2]) * erupt_time
wait_time
```

```
## [1] 140.8
```


---

## In the future

We hope to tap existing distribution channels through Yellowstone National Park and other distributors and gain 2 million subscribers in the first year.

After that, we plan to develop a mobile app when the R community makes an easy, open-source framework for implementing mobile apps.


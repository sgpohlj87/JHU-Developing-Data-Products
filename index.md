---
title       : Let's calculate your Body Mass Index (BMI)
subtitle    : Developing Data Products - John Hopkins University
author      : 
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## What is Body Mass Index (BMI)?
The Body mass index (BMI) is a simple index of weight-for-height that is commomly used to classify underweight, overwight and obesity in adults. According to  World Health Organization (WHO), the classification of the BMI of an adult is as follows:

1. BMI of less than 18.5 = Underweight
2. BMI of between 18.5 and less than 25.0 = Normal Weight
3. BMI of between 25.0 and less than 30.0 = Overweigh
4. BMI of 30.0 or more =  Obese

---
## How is BMI calculated?
The BMI is derived from that ratio of weight of the body in kilograms to the square of its height in meters. The formula is the following:

BMI = weight(kg) / height(metres)*height(metres)

An example is as follows:

```r
weight=70
height=1.7
BMI=weight/(height*height)
BMI
```

```
## [1] 24.22145
```

---
## BMI Classification
We use the following function to determine the BMI classification:

```r
classification<-function(weight,height){
  BMI_value<-weight/(height^2)
  ifelse(BMI_value<18.5,"Underweight",ifelse(BMI_value<25,"NormalWeight",ifelse(BMI_value<30,"Overweight","Obesity")))
}
```
Using our example whereby weight=70kg and height=1.7m, the classification of this adult would be:

```r
classification(70,1.7)
```

```
## [1] "NormalWeight"
```

---
## Conclusion
The BMI is a relatively simple and easy method for establishing the weight status of a person and in particular, it correlates reasonably well with their level of body fat.

However, the BMI is only considered an proxy to a person's body fat. There are other factors such as fitness level, health status, ethnicity, age and gender that could affect one's BMI with body fat, and hence should be taken into consideration as well.

---
Thank You


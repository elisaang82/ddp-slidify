---
title       : Height Predictor
subtitle    : 
author      : Elisa 
job         : 
framework   : landslide        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
github:
  user: elisaang82
  repo: ddp-slidify
---

## Predicting a child's height


<h3>By Elisa Ang</h3>

---

## Why

<ul>
<li>Some parents are keen to know if their children are growing well.</li>
<li>Some wish to know what should be the minimum height of their future spouse.</li>
<li>Nerds just wanted to find out if they knew the heights of the parents, could they then predict their childrens' heights.</li>
</ul>

---

## How

The most common method is to subtract 13 cm from the father's height and average with the mother's height for girls, and add 13 cm to the mother's height and average with the father's height for boys.

The code below implements this model.


```r
if (input$gender == "m") {
      ( (input$motherheight + 13) + input$fatherheight ) / 2
    } else {
      ( (input$fatherheight - 13) + input$motherheight ) / 2
    }
}
```

---

## Accuracy

This method although fairly accurate, the child's ultimate height can vary by as much as 13 centimetres above or below this calculation.

---

## Try it out

You can try this model out <a href="https://elisaang.shinyapps.io/heightpredictor/">here</a> and see if your parents heights indeed could predict your height!

---

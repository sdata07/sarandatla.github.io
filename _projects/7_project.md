---
layout: page
title: Forest Area Prediction using GDP
description: Using GDP per Capita to Predict Future Forest Cover
img: assets/img/Project 2/Forest.jpg
importance: 1
category: work
related_publications: true
---

With growing concerns for climate change, scientists are relying on a well known solution - afforestation. 
<br>
However, with rising incomes also surges resource utilization and increase in demand for timber.
<br>
Therefore, I collected and plotted data to see if there was any correlation between the two, and predict future forest area using a regression tree and future GDP projections.

<h3>Context: </h3>
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Project 2/Area Trends Sample.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

A random sample of 7 countries and their forest areas over time. <br>
There is a general decrease in forest area regardless of the continent. However, there are some exceptions like Vietnam which is showing a rapid increase.

<br>

<h3>Data on GDP: </h3>
Used a kaggle dataset to obtain the GDP per capita of every country and then percentage changes across time.
I then averaged the results to obtain a general global trend

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Project 2/Gloabal GDP Change.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The changes in GDP per capital per country from 1992 - 2022
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Project 2/Averaged GDP Change.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Globally average change in GDP per capita
</div>


<h3>Changes in Forest Cover: </h3>
Used another kaggle dataset to find the percentage changes in forest cover and averaged the results.
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Project 2/Change in Forest Cover.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
As you can see there is a consitent and minor increase in forest area compared to 1992 (which I have kept as 0). After that there is a clear downward trend in increase and even a decrease from 2010 onwards. Thus indicating a large change during this time and this is the period I wanted to investigate.


The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}

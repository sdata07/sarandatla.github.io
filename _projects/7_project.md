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

<h3>Combining both datasets: </h3>
I then combined both datasets to find any correlation between the two. I found a strong relationship after 2010, which I selected out

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Project 2/1992 Combined.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Combined data since 1992
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Project 2/2010 Combined.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Combined data since 2010
</div>


<h3>Making predicitons: </h3>
Finally, to make the model capable of predicting future values I split the data after 2010 into training and testing (split on the year 2018).
<br>
From this I implemented a gradient boosting model on the training data. I then predicted the test values' "Forest Cover Change" and compared the results as shown in the graph.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Project 2/Predictions.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<h3>Conclusion: </h3>
As you can see there is a clear correlation between forest cover and GDP, showing how crucial resource aquistion is in developing an economy. Furthermore, I hope that from this data policymakers will be more inclined to protect natural habitats as there is not only an altruistic incentive, but an economic one as well.

Here is a link to the github repo:
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0 text-center">
        <a href = "https://github.com/sdata07/Forest-Area-Predictor" target="_blank">{% include figure.liquid path="assets/img/Project 1/github-mark-white.png" title="git-hub" class="img-fluid rounded z-depth-1" width="80px" %} </a>
    </div>
</div>

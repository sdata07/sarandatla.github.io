---
layout: page
title: IPL Toss and Match Winner
description: A project that visualizes the IPL toss and match prediction winner over time.
img: /assets/img/Project 1/IPL Win Toss Predictor Project.jpg
importance: 1
category: work
related_publications: false
---

I am a big fan of the IPL and wanted to know if winning the toss really gave the team any advantage, and if that advantage changed over time.
My hypothesis is that it would, but it would show less and less of an effect later in the season, because of the monsoons creating more unpredictability.

I used a kaggle dataset over 15 seasons and saw the results and any corrrelation using a linear regression model.
I averaged the data of 7 matches to prevent randomness affecting the results.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Project 1/Toss and Match winner over time.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    2008 - 2022 Season match and toss winner where winning is a 1 and losing is a 0.
    The orange lines indicate predictions over time.
</div>

As you can see there is barely any correleation between with winning the toss and winning the game indicating that the toss rarely affects the game outcome.

Here is a link to the github repo:
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0 text-center">
        <a href = "https://github.com/sdata07/ipl-toss-and-game-winner" target="_blank">{% include figure.liquid path="assets/img/Project 1/github-mark-white.png" title="git-hub" class="img-fluid rounded z-depth-1" width="80px" %} </a>
    </div>
</div>



---
layout: post
title: Rainwater modelling 
---



The Problem:
============
“Do we have enough rainwater? Will we run out?”
A common question for those who lack access to town water, or want to run their premises solely on rainwater. How much rainwater capture-and-storage is needed?
The Solution:
=============
The Australian Bureau of Meteorology has detailed rainfall data going back nearly 150 years. I built a model of rainwater catchment and consumption that consisted of two parts:
## Part 1: water consumption
A month-by-month model of consumption that fluctuated throughout the year. This was based on actual water usage patterns and was reconciled with known consumption data from the utility.
## Part 2: rainfall and water storage
This models the available roof area and storage capacity. Using known historical rainfall from the Bureau of Meteorology, it tracks how much rainwater was stored each month for the period for which rainfall records exist.
## Synthesis
These two models are then combined in a time-series model, which shows how the known rainfall, proposed system configuration and consumption model would have interacted historically. This is very useful in assessing the frequency that the premises would have run out of water.
## Conclusion
The model allows one to explore the interaction of rainwater capture and storage configurations versus water consumption to assess if a given configuration is sufficient at a site. This is a powerful tool for scenario exploration.

If you would like help assessing your rainwater capture-and-storage requirements, please contact me.

![_config.yml]({{ site.baseurl }}/images/business_card_front.png)

The easiest way to make your first post is to edit this one. Go into /_posts/ and update the Hello World markdown file. For more instructions head over to the [Jekyll Now repository](https://github.com/barryclark/jekyll-now) on GitHub.

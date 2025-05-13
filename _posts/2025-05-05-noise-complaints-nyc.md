---
layout: post
title: "What to keep in mind regarding noise complaints in New York City?"
date: 2025-05-05
categories: dataviz
---

<br>

<span style="font-style: italic; font-size: 16px;">
Final Assignment
</span>

<span style="font-style: italic; font-size: 16px;">
Author: Eyjólfur Axel Kristjánsson (s242736)
</span>

<br>


### Notebook

[Click here to view the full Jupyter notebook (Finalassigment.ipynb)](/assets/Finalassigment.ipynb)

This notebook contains the complete analysis including data cleaning, preprocessing, and the code behind all the visualizations in this post.

## Introduction

In this notebook, we explore the noise landscape of New York City using 311 service request data from the past two years. The dataset includes millions of records from residents reporting issues related to noise everything from loud music and parties to banging and construction disturbances.

Since the goal of this project is to understand where one might find peace and quiet within New York City, we begin by identifying which types of noise complaints are most common. From there, we map out where those complaints occur, breaking down the data by borough and neighborhood. We also take a closer look at when these complaints are most likely to happen, revealing patterns by hour and by season.

By combining spatial, temporal, and categorical analysis, this notebook offers a deeper look into how soundi s experienced across the city. Whether you're planning a move or just curious about urban living patterns, this project provides a data driven guide to the noise that shapes daily life in New York.


# Where to move within New York City?

New York City is loud but that’s hardly breaking news. In fact it is ranked as the second loudest city in the world according to Fox. [7] But how loud? And where exactly? For anyone planning to move within the city, **noise complaints** are more than just background chatter. They’re a quality of life issue. 

Too much noise at night can ruin your sleep, stress you out, and wear down your mental health. This blog explores how different areas in NYC vary in terms of noise complaints. Using data from the city’s 311 service, we break down when and where people report noise, what kind of noise it is, and how trends differ from borough to borough.

This isn’t just academic, if you’re someone who values peace and quiet, this information could help guide where to live (or where to avoid).

---

### What type of noise complaints?

Noise isn’t just noise. The city categorizes complaints, and one type dominates them all: **loud music and parties**. This type of complaint vastly outnumbers all others, whether you're in the Bronx or Staten Island.

The distribution of complaint types is surprisingly similar across boroughs. However, Brooklyn and Manhattan do show slightly higher counts for **banging and pounding**. Those persistent, mechanical or construction related noises that seem to echo forever in apartment buildings.

This visualization shows which kinds of sounds get on people’s nerves the most and gives you a clue what kind of noise you’ll be dealing with depending on your borough.

---
<img src="/assets/img/Types_complaint.png" alt="Types of Noise Complaints in NYC" style="width:60%; display:block; margin:auto;" />
<p style="text-align: center;"><strong>Fig. 1:</strong> Types of noise complaints reported in New York City.</p>


## Where do noise complaints happen?

Geography tells a story of its own. In the interactive heatmap below, you can explore complaint concentrations across neighborhoods. 

The **Bronx emerges as the city’s loudest borough**, followed by **Brooklyn**. **Queens and Manhattan** sit somewhere in the middle, while **Staten Island** is the quietest, at least when it comes to official 311 reports.

This doesn’t necessarily mean the Bronx is objectively noisier; it could reflect a combination of housing density, population behavior, or even how likely people are to report problems. But the pattern is strong, and it shows where noise is felt, or at least reported most which gives you a good indication. 

---

<iframe src="/assets/nyc_heatmap_map.html" width="100%" height="600" frameborder="0"></iframe>
<p style="text-align: center;"><strong>Fig. 2:</strong> Heatmap of noise complaints across New York City neighborhoods.</p>

Or [open the map in a new tab](/assets/nyc_heatmap_map.html).

The following graph shows a 50.000 random points in new york city to display where the noise complaints are happening. With this interactive map you can further investigate your neighborhood all the way to your street. This gives you an indication on how often a certain street for example might be complaining about noice. This gives you a chance to look for a place with the fewest points on the map which is likely to be a calmer street. Note that since this is only 5000 random points you cant completelly trust this but it should give a good indication.

<iframe src="/assets/nyc_noise_map.html" width="100%" height="600" frameborder="0"></iframe>
<p style="text-align: center;"><strong>Fig. 3:</strong> Interactive map showing 5,000 sampled noise complaints across NYC.</p>

Or [open the map in a new tab](/assets/nyc_noise_map.html).


### Borough comparison over time

Zooming in month-by-month, we get a better sense of how things are changing. Are some boroughs getting noisier?

In fact, yes especially in the **Bronx**, where the last few months of 2024 show a dramatic spike in complaints. Whether that's due to holiday parties, increased reporting, or something else isn’t entirely clear, but it's a surge that stands out.

*Time Out New York* noted the trend in their citywide rankings, although they didn’t speculate on the cause [1]. *Fox5 News* suggested that newer residents might simply be less tolerant of noise and quicker to call 311 [2].

Another reason for this spike might be due to **local events and street partying** in the Bronx, which reportedly continued well into the fall months. CBS News covered loud car meetups and vehicle speaker “sound offs” on Jerome Avenue, noting that police had to intervene after residents filed repeated complaints [3]. These informal parties often take over streets late at night and are difficult to control once they start.

Adding to this, the **unseasonably warm weather in fall 2024** may have encouraged more people to stay outside and celebrate longer than usual. According to NYC weather records, November 2024 was nearly 3.5°F warmer than average, with multiple days feeling more like September than late autumn [4]. That kind of climate easily extends the “block party season” and could help explain the high volume of complaints coming in as late as December.


Watching these trends over time helps us think beyond averages and look at how neighborhoods are evolving. Maybe a quiet block in spring becomes unbearable in December.

---

<img src="/assets/img/monthly_complaint_trends.png" alt="Monthly Complaint Trends in NYC" style="width:60%; display:block; margin:auto;" />
<p style="text-align: center;"><strong>Fig. 4:</strong> Monthly trend of noise complaints in New York City.</p>

### Noise complaints in relation to population

Raw complaint numbers don’t tell the full story. Some boroughs are more populous than others, so naturally they’ll have more noise reports. To adjust for that, we looked at the **rate of complaints per 1,000 residents**. This was done by listing the amount of residents estimated for each Borough in 2024 from citypopulation.de. [5] That is then divided by the number of complaints. 

Even after accounting for population, the same pattern mostly holds, **Bronx and Brooklyn are still on top**, and Staten Island remains the quietest.

This method gives us more confidence that the trends aren’t just about size. The **complaint per capita metric** adds an important fairness check to the data.

---

<div style="display: flex; justify-content: center;">
  <iframe src="/assets/nyc_noise_rate.html" width="90%" height="600" frameborder="0"></iframe>
</div>
<p style="text-align: center;"><strong>Fig. 5:</strong> Noise complaints per capita across NYC boroughs.</p>

Or [open the map in a new tab](/assets/nyc_noise_rate.html).

## When do noise complaints happen?

Nighttime is when things get loud or at least when people notice. Across all boroughs, there’s a visible spike in complaints around **11:00 PM**. This lines up with the end of the evening for some and the start of the party for others.

Some boroughs show a tighter peak, while others have noise complaints more evenly spread across the evening and night. For residents, this matters: a sharp spike might mean a quick disruption, but a wide spread could mean noise that stretches on for hours.

It is interesting to look how the complaints spread a bit more for some districts than others. For example the time of the complaints vary more in the Bronx than the rest while Staten Island seems to be the narrowest. That allows us to see how some Boroughs receive noice complaints for a longer period than others.

This temporal pattern shows just how nocturnal New York's noise can be.

---
<img src="/assets/img/Polar_time.png" alt="Hourly Distribution of Noise Complaints" style="width:60%; display:block; margin:auto;" />
<p style="text-align: center;"><strong>Fig. 6:</strong> Hourly distribution of noise complaints in New York City.</p>


### Calendar comparison

Not all days are created equal. When we break down noise complaints by calendar day, seasonal patterns and major holidays come into focus.

For example, **December 31st** sees a huge spike each year as people ring in the new year with parties and fireworks. Other peaks appear in summer and around national holidays. But one date in **2024 stands out above the rest**: **September 15**.

That day alone logged **6,546 complaints** — nearly **six times the daily average** of around 924. The next-highest day was December 16 with 5,585. On the calendar heatmap, Sept 15 appears as a major outlier, especially in the 2024 plot.

So what happened?

While no single confirmed event explains it, several factors likely played a role. It was a **warm Sunday night**, about 79°F and marked the start of **Hispanic Heritage Month** [6], right before several Latin American Independence Days. Many Bronx neighborhoods have large Latino communities, and it’s likely that informal block parties and street celebrations were happening that night. Social media posts promoted **DJ led gatherings** and **salsa events** in the Bronx that weekend, suggesting a citywide celebration vibe.

It's also possible that some **data entry or timestamp errors** contributed to the spike, with multiple complaints being logged under the same date but there's no firm evidence of a systemic glitch. The data points to a real event, even if it's hard to trace to one specific cause.

In short, **Sept 15, 2024**, looks like a perfect storm: great weather, cultural celebrations, and maybe a bit of 311 reporting overload — all adding up to the noisiest day in the dataset.

---
<img src="/assets/img/calendar_2024.png" alt="Calendar of Noise Complaints 2024" style="width:80%; display:block; margin:auto;" />
<p style="text-align: center;"><strong>Fig. 7:</strong> Calendar heatmap of daily noise complaints in 2024.</p>

<br>

<img src="/assets/img/calendar_2023.png" alt="Calendar of Noise Complaints 2023" style="width:80%; display:block; margin:auto;" />
<p style="text-align: center;"><strong>Fig. 8:</strong> Calendar heatmap of daily noise complaints in 2023.</p>



### Conclusion

If you’ve ever been jolted awake by a neighbor’s sound system or construction hammer at 6 a.m., you already know: **noise defines New York City life**.

But with this data, we don’t have to rely on guesswork. We can map where it happens, when it happens, and what kinds of noise people are reporting. It’s not perfect, not every noise gets reported but it’s a powerful proxy for what living in each neighborhood might feel like. 

Whether you’re a newcomer trying to pick a quiet block, or a longtime resident wondering if your borough is getting noisier, this analysis offers a data-backed way to tune in to the city’s loudest conversations. Staten Island is clearly according to this study the quitest area to live in and might be good to consider for those who want a calmer neighborhood. But for those who thrive in the chaos it might be good to consider other areas.

### Sources

[1] Time Out New York: [These NYC neighborhoods had the most noise complaints last year](https://www.timeout.com/newyork/news/these-nyc-neighborhoods-had-the-most-noise-complaints-last-year-031924)  
[2] Fox5 News: [Noise tops NYC’s 311 complaints list for 2024](https://www.fox5ny.com/news/noise-tops-nycs-311-complaints-list-2024)  
[3] CBS News: [Noisy car meetups in the Bronx](https://www.cbsnews.com/newyork/news/noisy-car-meetups-bronx-jerome-ave/#:~:text=The%20New%20York%20City%20Police,in%20many%20of%20the%20cars)  
[4] NYC Weather Archive (The Starry Eye): [November 2024 warm spell](https://thestarryeye.typepad.com/weather/2024/11/#:~:text=November%202024%20,the%20warmest)  
[5] City Population: [Population of New York Boroughs](https://www.citypopulation.de/en/usa/newyorkcity/)  
[6] National Hispanic Heritage Month: [About Hispanic Heritage Month](https://www.hispanicheritagemonth.gov/about/)  
[7] Fox5 News: [NYC ranks among the noisiest cities in the world](https://www.fox5ny.com/news/most-noisest-city-world-where-does-nyc-rank?utm_source=chatgpt.com)




---
layout: post
title: "Patterns in Drug Offense Crimes in San Fransisco"
date: 2025-03-30
categories: dataviz
---


This post explores when and where drug offenses occur in San Francisco using data from 2003–2024. The data is drawn from the San Francisco Police Department’s publicly available crime incident reports. Each record includes information such as the type of crime, time of day, police district, and year. For this story, the focus is specifically on drug-relate crimes.

While drug use and policy enforcement vary by neighborhood and over time, this analysis highlights broader spatial and temporal trends in drug-related incidents reported to the police. By visualizing the data in three different ways, we aim to uncover when drug crimes most frequently happen during the day, in what districts do they tend to occur, and how those patterns have evolved across time.

<!-- Visualization and content will go here -->

### When Do Drug Offenses Occur?

The polar plot below displays the relative frequency of drug-related offenses reported throughout the 24-hour day. Each bar represents an hour, and the length of the bar indicates how common drug crimes are during that period.

![Polar Plot of Drug Offenses](/assets/img/drug_hourly_polar.png)

We observe a clear pattern: drug offenses are less frequent in the early morning hours, then gradually increase during the day, peaking in the late afternoon and evening. Notice that they rarely happen during the night time which might be an interesting finding to most. This trend likely reflects a combination of human behavior (more activity in public spaces in the evening) and police enforcement patterns. [^1] 

## Where Do Drug Offenses Happen?


The map below shows the number of drug-related incidents per police district. It allows you to explore geographic variation by hovering or zooming in on districts across San Francisco.

<iframe src="/assets/drug_map.html" width="100%" height="600" frameborder="0"></iframe>

Or [open the map in a new tab](/assets/drug_map.html).

---
Certain areas—particularly the Tenderloin and Southern districts—stand out as hotspots for drug-related crime. These areas have historically been associated with concentrated urban activity, vulnerable populations, and higher visibility of street-level drug use. Tenderloin, in particular, is considered ground zero for San Francisco’s open-air drug market. [^2] 


## How Drug Offenses Have Changed Across Districts


The following interactive chart shows the number of drug offenses in each district by year from 2003 to 2024. You can click on each district in the legend to isolate trends or mute others for clarity.

<iframe src="/assets/drug_trends_bars.html" width="120%" height="395" frameborder="0"></iframe>

Or [open the chart in a new tab](/assets/drug_trends_bars.html).

There was a notable rise in drug-related offenses from 2004 to 2009, followed by a general decline until around 2016. One of the main reasons for the drop in drug-related crimes in San Francisco between 2008 and 2016 was a change in police enforcement and prosecution policies. After scandals involving the San Francisco Police Department’s drug arrests, both the police and the District Attorney’s office reduced the number of drug-related felony arrests and filings. This shift led to fewer people being arrested and charged for drug offenses during that period. [^3]
After that drug related crimes began to increase again and that might be a result of the pandemic that started in 2019 where health officials belived that people feeling isolated and depressed lead to increased drug use. [^4]

### References

[^1]: Ratcliffe, J. H. (2010). *Crime mapping: spatial and temporal challenges*. In Handbook of Quantitative Criminology (pp. 5–24). Springer. https://doi.org/10.1007/978-0-387-77650-7_2

[^2]: CNN. (2023, September 3). *San Francisco’s Tenderloin is ground zero for the city’s drug crisis*. Retrieved from [https://edition.cnn.com/2023/09/03/us/san-francisco-tenderloin-drug-market/index.html](https://edition.cnn.com/2023/09/03/us/san-francisco-tenderloin-drug-market/index.html)

[^3]: Justice Atlas for All. *Reforming San Francisco’s Criminal Justice System: A Decade of Progress.* Retrieved from [https://probation.acgov.org/probation-assets/files/resources-info/Reforming%20San%20Franciscos%20Criminal%20Justice%20System-JA4.pdf](https://probation.acgov.org/probation-assets/files/resources-info/Reforming%20San%20Franciscos%20Criminal%20Justice%20System-JA4.pdf)

[^4]: San Francisco Chronicle. (2024). *Tracking San Francisco’s drug overdose crisis*. Retrieved from [https://www.sfchronicle.com/projects/san-francisco-drug-overdose-deaths/](https://www.sfchronicle.com/projects/san-francisco-drug-overdose-deaths/)


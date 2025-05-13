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

# Where to move within New York City?

New York City is loud — that’s hardly breaking news. But how loud? And where exactly? For anyone planning to move within the city, **noise complaints** are more than just background chatter — they’re a quality-of-life issue. 

Too much noise at night can ruin your sleep, stress you out, and wear down your mental health. This blog explores how different areas in NYC vary in terms of noise complaints. Using data from the city’s 311 service, we break down when and where people report noise, what kind of noise it is, and how trends differ from borough to borough.

This isn’t just academic — if you’re someone who values peace and quiet, this information could help guide where to live (or where to avoid).

---

### What type of noise complaints?

Noise isn’t just noise. The city categorizes complaints, and one type dominates them all: **loud music and parties**. This type of complaint vastly outnumbers all others, whether you're in the Bronx or Staten Island.

The distribution of complaint types is surprisingly similar across boroughs. However, Brooklyn and Manhattan do show slightly higher counts for **banging and pounding** — those persistent, mechanical or construction-related noises that seem to echo forever in apartment buildings.

This visualization shows which kinds of sounds get on people’s nerves the most — and gives you a clue what kind of noise you’ll be dealing with depending on your borough.

---

<!-- Visualization: Noise complaints by hour will go here -->
<img src="/assets/img/Types_complaint.png" alt="Types of Noise Complaints in NYC" style="width:60%; display:block; margin:auto;" />
<p style="text-align: center;"><strong>Fig. 2:</strong> Types of noise complaints reported in New York City.</p>


## Where do noise complaints happen?

Geography tells a story of its own. In the interactive heatmap below, you can explore complaint concentrations across neighborhoods. 

The **Bronx emerges as the city’s loudest borough**, followed by **Brooklyn**. **Queens and Manhattan** sit somewhere in the middle, while **Staten Island** is the quietest — at least when it comes to official 311 reports.

This doesn’t necessarily mean the Bronx is objectively noisier; it could reflect a combination of housing density, population behavior, or even how likely people are to report problems. But the pattern is strong, and it shows where noise is felt — or at least reported — most.

---

<iframe src="/assets/nyc_heatmap_map.html" width="100%" height="600" frameborder="0"></iframe>
<p style="text-align: center;"><strong>Fig. 4:</strong> Heatmap of noise complaints across New York City neighborhoods.</p>

Or [open the map in a new tab](/assets/nyc_heatmap_map.html).

The following graph shows a 50.000 random points in new york city to display where the noise complaints are happening. With this interactive map you can further investigate your neighborhood all the way to your street. 

<iframe src="/assets/nyc_noise_map.html" width="100%" height="600" frameborder="0"></iframe>
<p style="text-align: center;"><strong>Fig. X:</strong> Interactive map showing 5,000 sampled noise complaints across NYC.</p>

Or [open the map in a new tab](/assets/nyc_noise_map.html).


### Borough comparison over time

Zooming in month-by-month, we get a better sense of how things are changing. Are some boroughs getting noisier?

In fact, yes — especially in the **Bronx**, where the last few months of 2024 show a dramatic spike in complaints. Whether that's due to holiday parties, increased reporting, or something else isn’t clear — but it's a surge that stands out.

Watching these trends over time helps us think beyond averages and look at how neighborhoods are evolving. Maybe a quiet block in spring becomes unbearable in December.

---

<img src="/assets/img/monthly_complaint_trends.png" alt="Monthly Complaint Trends in NYC" style="width:60%; display:block; margin:auto;" />
<p style="text-align: center;"><strong>Fig. 1:</strong> Monthly trend of noise complaints in New York City.</p>

### Noise complaints in relation to population

Raw complaint numbers don’t tell the full story. Some boroughs are more populous than others, so naturally they’ll have more noise reports. To adjust for that, we looked at the **rate of complaints per 1,000 residents**.

Even after accounting for population, the same pattern mostly holds — **Bronx and Brooklyn are still on top**, and Staten Island remains the quietest.

This method gives us more confidence that the trends aren’t just about size. The **complaint-per-capita metric** adds an important fairness check to the data.

---

<iframe src="/assets/nyc_noise_rate.html" width="100%" height="600" frameborder="0"></iframe>
<p style="text-align: center;"><strong>Fig. 5:</strong> Noise complaints per capita across NYC boroughs.</p>

Or [open the map in a new tab](/assets/nyc_noise_rate.html).

## When do noise complaints happen?

Nighttime is when things get loud — or at least when people notice. Across all boroughs, there’s a visible spike in complaints around **11:00 PM**. This lines up with the end of the evening for some... and the start of the party for others.

Some boroughs show a tighter peak, while others have noise complaints more evenly spread across the evening and night. For residents, this matters: a sharp spike might mean a quick disruption, but a wide spread could mean noise that stretches on for hours.

This temporal pattern shows just how nocturnal New York's noise can be.

---
<img src="/assets/img/Polar_time.png" alt="Hourly Distribution of Noise Complaints" style="width:60%; display:block; margin:auto;" />
<p style="text-align: center;"><strong>Fig. 3:</strong> Hourly distribution of noise complaints in New York City.</p>


### Calendar comparison

Not all days are created equal. By mapping noise complaints across days and months, we get a richer view of how **seasonality and holidays** might play a role.

Take a look at **December 31st**, for instance — a huge spike in complaints right before midnight in both 2023 and 2024. Parties, music, yelling — it all adds up. Other notable peaks appear in early summer and around major holidays.

Each day on these calendar heatmaps reflects actual complaints logged to 311. Some neighborhoods seem to be noisy year-round, while others only light up on weekends or holidays.

This part of the analysis highlights how noise is woven into the rhythms of city life — not just space, but **time** matters too.

---
<img src="/assets/img/calendar_2024.png" alt="Calendar of Noise Complaints 2024" style="width:80%; display:block; margin:auto;" />
<p style="text-align: center;"><strong>Fig. 6:</strong> Calendar heatmap of daily noise complaints in 2024.</p>

<br>

<img src="/assets/img/calendar_2023.png" alt="Calendar of Noise Complaints 2023" style="width:80%; display:block; margin:auto;" />
<p style="text-align: center;"><strong>Fig. 7:</strong> Calendar heatmap of daily noise complaints in 2023.</p>



### Final Thoughts

If you’ve ever been jolted awake by a neighbor’s sound system or construction hammer at 6 a.m., you already know: **noise defines New York City life**.

But with this data, we don’t have to rely on guesswork. We can map where it happens, when it happens, and what kinds of noise people are reporting. It’s not perfect — not every noise gets reported — but it’s a powerful proxy for what living in each neighborhood might feel like.

Whether you’re a newcomer trying to pick a quiet block, or a longtime resident wondering if your borough is getting noisier, this analysis offers a data-backed way to tune in to the city’s loudest conversations.
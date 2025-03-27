---
layout: default
---

# Title


## Trends in Crime Over Time
We analyzed the time series of these 3 type of crimes from the year 2003 to 2025. In the following barchart, you can explore the trends on an annual and hourly basis.
<br>
{% include crime_visualization.html %}

**Observation**

Hour: <br>
Looking at the hourly distribution, we observe that crime cases are lowest between 4:00 AM and 6:00 AM across all crime categories. After 6:00 AM, the number of cases increases every hour, which indicates a rise in criminal activity as the day progresses.
<br>
**Weapon Laws** has its peak at 3 PM <br>
**Assault** has its peak at 10 PM <br>
**Robbery** has its peak at 9 PM <br>

Year: <br>
From the annual perspective, we can observe that the frequency of violations of **Weapon Laws** has shown an upward trend over the years. In contrast, **Assault** cases have been  decreasing over the years, significantly dropped by 20% from the year 2017 to 2018.
The number of **Robbery** cases fluctuated, rising in some years and falling in others, but in 2024 the cases dropped by nearly 50%.<br>

Overall, there is no clear correlation between these three types of crimes. However, we can suspect that some assault cases may be turning into weapon law cases, as assault cases are decreasing while weapon law cases are increasing.

## Where Do Crimes Occur?

Crime doesn’t happen randomly—it follows patterns. To uncover them, we mapped **assault, robbery, and weapon-related crimes**, using heatmaps and pinpointing high-frequency locations. You can toggle between these views to explore the trends.

{% include crime_heatmap.html %}

One clear takeaway: **assaults are the most widespread, covering nearly the entire city**, while **robbery and weapon crimes cluster in specific areas**, particularly **the southern Northern District and Mission District**—bustling areas where dense crowds may heighten conflict risks.

Interestingly, **assault and robbery hotspots often overlap**, suggesting robberies frequently involve violence. Some areas may even harbor **organized crime or repeat offenders**. **Weapon-related crimes, while partially overlapping, are more dispersed**, indicating their involvement in **various offenses beyond violence, such as illegal possession or drug trade**.

By mapping crime trends, **law enforcement can allocate resources more effectively**, targeting high-risk areas to enhance urban safety.

# Title
{% include crime_trends_with_regression_bokeh.html%}


# Conclusion 
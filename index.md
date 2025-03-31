---
layout: default
---

# Trends and correlations of weapon/assault and robbery crimes in San Francisco
Crime is a complex and multidimensional social phenomenon, taking various forms and exerting far-reaching impacts. Although different types of crime vary in nature and consequences, they are often not isolated but interconnected in certain ways.  

Understanding the relationships between different crimes, visualizing data, and analyzing crime trends are crucial for developing effective law enforcement strategies and crime prediction models. For instance, incidents of lost or stolen weapons may lead to firearms falling into the hands of criminals, thereby increasing the risk of violent assaults or robberies. This potential evolutionary pathway highlights the necessity of systematic data analysis to identify underlying crime chains and triggering factors.  

In this study, we explore the potential connections between weapon, assault, and robbery. Literature such as [_Nonlinear Dynamics of Crime and Violence in Urban Settings_ [1]](https://jasss.soc.surrey.ac.uk/15/1/2.html) and [_Violence in Urban Neighborhoods: A Longitudinal Study of Collective Efficacy and Violent Crime_ [2]](https://doi-org.proxy.findit.cvt.dk/10.1007/s10940-016-9311-z) provides theoretical support for our analysis and inspires us to conduct exploratory data analysis.  

Our core dataset comes from the [_San Francisco Police Department Incident Reports: Historical 2003 to May 2018_](https://data.sfgov.org/Public-Safety/Police-Department-Incident-Reports-Historical-2003/tmnf-yvry). We will analyze the evidence reflected in this dataset from multiple perspectives, attempting to uncover possible causal relationships and co-evolutionary pathways among these three types of crime.  


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
From the annual perspective, we can observe that the frequency of violations of Weapon Laws has shown an upward trend over the years. In contrast, Assault cases have been  decreasing over the years, significantly dropped by 20% from the year 2017 to 2018.
The number of Robbery cases fluctuated, rising in some years and falling in others, but in 2024 the cases dropped by nearly 50%. This finding is the same as the crime control board provided by the official website of the former San Francisco Police Bureau[\[3\]](https://www.sanfranciscopolice.org/stay-safe/crime-data/crime-dashboard).<br>

Overall, there is no clear correlation between these three types of crimes. However, we can suspect that some assault cases may be turning into weapon law cases, as assault cases are decreasing while weapon law cases are increasing.

## Where Do Crimes Occur?

Crime doesn’t happen randomly—it follows patterns. To uncover them, we mapped assault, robbery, and weapon-related crimes, using heatmaps and pinpointing high-frequency locations. You can toggle between these views to explore the trends.

{% include crime_heatmap.html %}

One clear takeaway: assaults are the most widespread, covering nearly the entire city, while robbery and weapon crimes cluster in specific areas, particularly the southern Northern District and Mission District—bustling areas where dense crowds may heighten conflict risks. This conclusion can also be found in the real-time crime data of the San Francisco[\[4\]](https://www.civichub.us/ca/san-francisco/gov/police-department/crime-data).

Interestingly, assault and robbery hotspots often overlap, suggesting robberies frequently involve violence. Some areas may even harbor organized crime or repeat offenders. Weapon-related crimes, while partially overlapping, are more dispersed, indicating their involvement in various offenses beyond violence, such as illegal possession or drug trade.

By mapping crime trends, law enforcement can allocate resources more effectively, targeting high-risk areas to enhance urban safety.

## Correlations and predictions of violent crime
To better understand the trend in the number of crimes over the years, we use linear regression. Note that in the plot containing both crimes, the y-axis scale is the same, so the visualization of the linear model is not misleading and can be easily compared.
{% include crime_trends_with_regression_bokeh.html%}
It can be clearly seen from the chart that Assault and Robbery show an overall downward trend, while Weapon Laws-related crimes remain relatively stable. The regression trend shows that the slope for Assault is significantly negative, indicating a large decrease in its occurrence, while Robbery also shows a downward trend, but at a slower pace. This suggests that between 2003 and 2024, improvements in public security have had a positive impact on these two types of violent crime. However, the regression slope for Weapon Laws-related crimes is close to zero, meaning that issues like illegal gun possession have not significantly changed over time, which may be related to the long-term stability of gun control policies.

Although both Assault and Robbery show a downward trend, the number of Assault incidents has consistently been much higher than that of Robbery, suggesting a possible correlation between the two, such as stricter law enforcement potentially reducing both assault and robbery cases. Additionally, the lack of significant decline in Weapon Laws-related crimes suggests that the relationship between these crimes and Assault and Robbery may be smaller, but still worth further exploration, especially in terms of whether the circulation of illegal weapons has had a long-term impact on violent crime. To gain a more accurate understanding of these trends, we recommend further analysis that incorporates socio-economic factors, law enforcement intensity, and policy changes to explore more complex crime patterns.


## Conclusion 
Understanding the trends and correlations between assault, robbery, and weapon-related crimes is crucial for developing effective crime prevention and intervention strategies. While assaults are the most widespread, occurring throughout nearly the entire city, robbery and weapon crimes tend to cluster in specific areas, particularly in the southern Northern District and Mission District, where dense crowds may increase conflict risks. Interestingly, assault and robbery hotspots often overlap, suggesting that robberies often involve violence, and some areas may harbor organized crime or repeat offenders. Weapon-related crimes, though somewhat overlapping, are more dispersed, indicating their involvement in various offenses beyond violence, such as illegal possession or drug trade. From a trend perspective, assaults have significantly decreased, while robberies have also shown a downward trend, though more gradually, reflecting positive impacts from improvements in public security. In contrast, weapon-related crimes have remained stable over time. The lack of significant decline in these crimes suggests that their relationship with assaults and robberies may be weaker, but further exploration is needed, particularly in relation to the circulation of illegal weapons. By incorporating socio-economic factors, law enforcement intensity, and policy changes, we can gain deeper insights into these trends and better allocate resources to high-risk areas, ultimately enhancing urban safety.

## References
[1]Fonoberova, Maria, et al. "Nonlinear dynamics of crime and violence in urban settings." Journal of Artificial Societies and Social Simulation 15.1 (2012): 2.<br>

[2]Hipp, John R., and Rebecca Wickes. "Violence in urban neighborhoods: A longitudinal study of collective efficacy and violent crime." Journal of Quantitative Criminology 33 (2017): 783-808.<br>

[3]San Francisco Police Department. (n.d.). Crime data dashboard. San Francisco Police Department. https://www.sanfranciscopolice.org/stay-safe/crime-data/crime-dashboard. (Retrieved March 31, 2025).<br>

[4]Civic Hub. (n.d.). Crime data – San Francisco Police Department. Civic Hub. https://www.civichub.us/ca/san-francisco/gov/police-department/crime-data. (Retrieved March 31, 2025).
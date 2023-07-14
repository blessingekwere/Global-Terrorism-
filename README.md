# Global-Terrorism
![](https://github.com/blessingekwere/Global-Terrorism-/blob/main/3d9c078e-2956-4a17-887b-be3ae7efb982.jpg)
##### Data Source:Google

## Overview
In a world faced with the persistent threat of terrorism, gaining a deep understanding of its dynamics is crucial for fostering global security and promoting peace. Our project aims to conduct an extensive analysis of the Global Terrorism Dataset, spanning from 1970 to 2020, in order to unravel hidden patterns, explore underlying causes, and assess the far-reaching impacts of terrorist activities worldwide.

Analyzing global terrorism data is a complex and critical task that requires a thorough examination and comprehension of various factors contributing to acts of terror across the globe. Through this project, we aim to derive insights, identify patterns, and uncover trends related to this global menace by examining data spanning over five decades. Our goal is to shed light on the evolution, characteristics, and root causes of terrorism, providing valuable insights for policymakers, security agencies, and
researchers.

![](https://github.com/blessingekwere/Global-Terrorism-/blob/main/e195d37c-b4e0-47a4-9967-1411fd798b11.jpg)
##### Data Source:Google


## Problem Statement
The issue of global terrorism remains a persistent and escalating concern for nations worldwide, significantly impacting the lives of millions and posing substantial challenges to global peace and security. To effectively address this issue, it is crucial to develop a profound understanding of the dynamics, trends, and underlying causes driving terrorism. However, the vast amount of data associated with global terrorism makes it challenging to extract meaningful insights and patterns without the aid of advanced data analysis techniques.

The primary problem this project aims to address is the need to analyze and make sense of the extensive global terrorism dataset from 1970 to 2020. This dataset comprises detailed information on thousands of terrorist incidents, including data on perpetrators, targets, methods used, locations, and the socio-political context surrounding each event. The challenge lies in efficiently processing, analyzing, and extracting relevant information from this vast dataset to derive actionable insights. This analysis aims to answer important questions regarding global terrorism:

* Global trends and patterns: What are the trends in terrorism over the past five decades?
* Evolution of terrorism: How has terrorism evolved in tactics, targets, and geographical spread?
* Responsible groups: Which groups are mostly responsible for terrorist attacks?
* Temporal and geographical clusters: Are there significant clusters of terrorist activity?
* Success rate and duration: What is the success rate of attacks and their durations?
* Impact on countries: Which countries have been most affected by terrorism?
* Weapon types: What are the commonly used weapons in these attacks?
* Claimed responsibility: Which groups have claimed responsibility for attacks?
* Perpetrators, casualties, and weapons: How many perpetrators, casualties, and what weapon types are involved in attacks?
Addressing these questions will provide valuable insights into global terrorism, aiding in the development of effective counter-terrorism measures.

Addressing these questions will not only contribute to academic research but will also provide practical insights for counter-terrorism efforts, policy formulation, and security strategies. The outcomes of this project will help stakeholders gain a comprehensive understanding of the nature of global terrorism, enabling the development of effective preventive measures and interventions to mitigate the threat and promote global stability.

![](https://github.com/blessingekwere/Global-Terrorism-/blob/main/e195d37c-b4e0-47a4-9967-1411fd798b11.jpg)
##### Data Source:Google


## Data Sourcing:
 The dataset was downloaded from Kaggle. Kindly find the link to the dataset [here](https://www.kaggle.com/datasets/sarfarazsheikh/global-terrorism-data-gtd-19702020)

## About the Dataset
The Global Terrorism Database (GTD) dataset contains a comprehensive record of terrorist incidents worldwide from 1970 to 2020. The dataset includes numerous columns describing different aspects of each incident. It contains 135 columns and 209707 rows. Below is a column description for some columns in the GTD dataset:

## Tool Used: Power BI
## Data Preprocessing
After downloading the dataset onto my local machine, I proceeded to load it into Power BI desktop for analysis. During the initial examination, I observed several noteworthy aspects of the dataset:

* Null Values: There were instances of missing data points within the dataset, represented as null values. These missing values can potentially affect the accuracy and reliability of the analysis, and strategies for handling them will need to be implemented.

* Incorrect Formatting: I noticed instances where the data was not formatted correctly according to the expected structure or data type. This can lead to issues in data manipulation and visualization, necessitating appropriate formatting adjustments.

* Spelling Errors: I identified instances of misspelled or incorrect spellings within the dataset. These errors can impact data integrity and consistency, requiring careful attention and potential corrections to ensure accurate analysis.

* Presence of Placeholders: I observed the presence of placeholders, such as the value '-99', indicating missing or unknown information. These placeholders can introduce biases or inaccuracies in the analysis if not handled appropriately. Appropriate treatment or imputation methods will be necessary to address these placeholders effectively.

By recognizing these issues within the dataset, it is essential to take corrective actions to ensure the reliability and accuracy of the subsequent data analysis process. Cleaning, formatting, and imputation techniques will be employed to address these challenges, ultimately leading to a more robust and trustworthy analysis of the global terrorism data.

## Data Cleaning
* After successfully loading the dataset into Power BI desktop, I previewed it and identified the need for transformations to prepare it for further analysis. To begin the transformation process, I clicked on the transform button, which opened the Power Query Editor.
![](https://github.com/blessingekwere/Global-Terrorism-/blob/main/Screenshot%20(184).png)
#### *Loading the datset into PowerBI desktop before proceeding to power query editor*

* In the Power Query Editor, I took the precaution of duplicating the dataset (although not a standard procedure) and disabled one of the duplicates from loading and refreshing. I then proceeded to rename the duplicated dataset, ensuring clarity in the subsequent steps of the transformation process.

* To start cleaning the data, I meticulously reviewed each column in the dataset. I performed various cleaning operations, such as removing null values, correcting formatting errors, and addressing misspellings. I made sure to format each column with the appropriate data type and renamed them accordingly to maintain consistency and clarity.

* To ensure consistency and clarity, I made replacements in the 'extended,' 'suicide,' and 'success' columns. Specifically, I substituted '1' with 'Yes' and '0' with 'No' to accurately represent the corresponding values in these columns. This modification enhances readability and facilitates a better understanding of the dataset.
![](https://github.com/blessingekwere/Global-Terrorism-/blob/main/Screenshot%20(185)%20-%20Copy.png)
#### *Using replace values command to replace values*

* One particular issue I noticed was that the day, month, and year information were separated into individual columns and not properly formatted. To rectify this, I merged these columns to form a single date column and ensured the correct formatting.

* Additionally, I extracted values for the year,month name and number from the date column since I required this information for my analysis. Instead of creating a separate calendar table, I utilized the existing date column for this purpose.
![](https://github.com/blessingekwere/Global-Terrorism-/blob/main/Screenshot%20(186)%20-%20Copy.png)
#### *Extracting values for year,month name and month number from the date column*

* To further enhance the analysis, I created a date range column using the conditional column command. This allowed me to group the dates into meaningful intervals such as '1970-1980,' '1981-1990,' '1991-2000,' '2001-2010,' and '2011-2020,' facilitating temporal analysis.
![](https://github.com/blessingekwere/Global-Terrorism-/blob/main/Screenshot%20(188).png)
#### *Creating a year range column using conditional column*

* Regarding the "number of perpetrators" column, I noticed the presence of a placeholder value (-99). To ensure accurate analysis, I applied a filter to exclude this placeholder value when examining the number of perpetrators involved in each incident.

* In the columns for "nkill" (number of people killed) and "nwound" (number of people wounded), I encountered null values. To address this, I replaced the null values with a placeholder (-99) and excluded them from the analysis when assessing the casualties.

* Finally, I dropped unnecessary columns from the dataset that were not pertinent to my analysis, streamlining the dataset for further exploration and insights.

By performing these transformations and cleaning operations, I have prepared the dataset to be more suitable and reliable for in-depth analysis in Power BI desktop.

As mentioned earlier, the original dataset contained 135 columns and 209,707 rows. However, after undergoing the cleaning and transformation process, the dataset has been refined, resulting in a reduced number of columns to 26 while retaining the same number of rows, 209,707. The descriptions of the remaining columns are as follows:

* eventid: Unique identifier for the incident.
  
* date: date of the incident.

* extended: Indicates whether the duration of the incident extended beyond 24 hours (0 = No, 1 = Yes)

* country_txt: Name of the country where the incident took place

* success: Indicates whether the attack was successful (0 = No, 1 = Yes).

* attacktype: Description of the primary type of attack.

* targettype: Description of the primary target of attack.

* group responsible: Name of the group claiming responsibility for the attack.

* number of perpetrators: Number of perpetrators of the attack

* weaptype: Description of the primary weapon type.

* number killed: Total number of individuals killed in the incident.

* number wounded: Total number of individuals wounded in the incident.

* year: year the incident occurred
  
* Month: Month of the incident.
  
* Month Number: Month Number of the incident.
  
* suicide: Indicates whether the attack was a suicide attack (0 = No, 1 = Yes).

* nationality of the target: Description of the nationality of the target.

* property: Indicates whether property was damaged or destroyed in the incident (0 = No, 1 = Yes).

* year range: Range of years of attack
  
* region_txt: Name of the region where the incident took place.
  
* city: City where the incident took place.

* multiple: Indicates whether the attack was multiple or not

* guncertain: Indicates whether there was a use of gun for each attack
  
* individual: Indicates if the attack was an individual attack or not

* claimed: Indicates whether any group claimed responsibility for that attack

* claimedtxt: Indicates the means used by the group that claimed responsibility for that attack

## ANALYSIS 
* The dataset covers a total of 204 countries and 45,000 cities, with recorded attacks reaching 210,000. Out of these attacks, 185,000 were successful, resulting in 479,000 deaths and 586,000 injuries. The dataset includes information on 4,000 known terrorist groups.

* Based on the analysis of attack success rates, it was found that 88.38% of attacks in the dataset were classified as successful, while 11.64% of attacks were categorized as not successful. These findings highlight the significant proportion of successful attacks, indicating the effectiveness of terrorist operations in achieving their objectives.

![](https://github.com/blessingekwere/Global-Terrorism-/blob/main/Attacks%20by%20success%20status.png)
#### *Attacks by success status*

* Furthermore, when examining attack durations, it was observed that 5.15% of attacks extended beyond 24 hours, while the majority of attacks, accounting for 94.85%, did not exceed the 24-hour mark. This analysis emphasizes that the majority of attacks were relatively short-lived, with a vast majority resolved within 24 hours.

![](https://github.com/blessingekwere/Global-Terrorism-/blob/main/Attacks%20by%20duration.png)
#### *Attacks by duration*

* Analyzing the top 5 countries based on attack frequency within different time periods, Afghanistan had 4 attacks between 1970 and 1980, while Colombia recorded 560 attacks, India recorded 34 attacks, Iraq recorded 12 attacks, and Pakistan recorded 18 attacks. The numbers increased in subsequent decades, with Afghanistan, Colombia, India, Iraq, and Pakistan experiencing varying levels of attacks.

![](https://github.com/blessingekwere/Global-Terrorism-/blob/main/Top%205%20countries%20by%20attack%20and%20year.png)
#### *Top 5 countries by attack and year*

* The most targeted groups based on the number of attacks were private citizens and property (51,985 attacks), followed by the military (34,131 attacks), police (28,568 attacks), government (23,828 attacks), and businesses (22,169 attacks).

![](https://github.com/blessingekwere/Global-Terrorism-/blob/main/Attacks%20by%20target.png)
#### *Attacks by target*

* Examining the top 5 groups claiming responsibility for attacks, the group categorized as "unknown" caused the highest number of casualties, with 111,570 deaths and 220,321 injuries. Other notable groups include the Taliban, Islamic State of Iraq and Levant (ISIL), Boko Haram, and Shining Path.

![](https://github.com/blessingekwere/Global-Terrorism-/blob/main/Number%20killed%20and%20injured%20by%20top%205%20groups.png)
#### *Number killed and injured by top 5 terrorist groups*

* Attacks varied by year, with 1970 seeing 651 attacks, 1980 witnessing 2,661 attacks, and 2014 reaching the highest point with 16,960 attacks. The lowest number of attacks occurred in 1971, with 471 incidents.

![](https://github.com/blessingekwere/Global-Terrorism-/blob/main/Attacks%20by%20year.png)
#### *Attacks by year*

* Bombing/Explosion was the most deadly attack type, resulting in 157,418 deaths and 330,713 injuries. Unarmed Assault had the lowest death toll (849). Bombing/Explosion accounted for 38.73% of the total number of deaths.

![](https://github.com/blessingekwere/Global-Terrorism-/blob/main/Number%20killed%20and%20injured%20by%20attack%20type.png)
#### *Number killed and injured by attack type*

* Weapon type analysis showed that explosive-based attacks caused the highest number of fatalities (171,453) and injuries (417,940). Firearms and unknown weapons were also responsible for significant casualties.

![](https://github.com/blessingekwere/Global-Terrorism-/blob/main/Number%20killed%20and%20injured%20by%20top%205%20weapon%20type.png)
#### *Number killed and injured by top 5 weapon type*

* Armed Assault had the highest number of perpetrators (358,320), followed by Facility/Infrastructure Attack (329,638). Hijacking had the fewest perpetrators (3,156).

![](https://github.com/blessingekwere/Global-Terrorism-/blob/main/Number%20of%20perpetrators%20by%20attack%20type.png)
#### *Attack type by number of perpetrators*

* Bombing/Explosion had the highest count of successful attacks (85,848), while Hijacking had the lowest count (676). Bombing/Explosion accounted for 46.33% of the total count of successful attacks.

![](https://github.com/blessingekwere/Global-Terrorism-/blob/main/Successful%20attacks%20by%20attack%20type.png)
#### *Successful attacks by attack type*

These insights provide a glimpse into the global terrorism landscape, highlighting the countries, groups, attack types, and their impacts. Through further analysis, we can gain a deeper understanding of the trends, patterns, and factors driving terrorism, ultimately contributing to more effective prevention and counterterrorism strategies.

## Visualization
Below is the dashboard showing the analysis of global terrorism from 1970-2020. Kindly click [here](https://app.powerbi.com/view?r=eyJrIjoiOTQwNjkzNGUtNjgwYi00MDc4LWFlNWItOGEyMTk4MTFiYTc0IiwidCI6IjMwMDM2MmQ4LTZkNmItNGY5ZC04YjQwLTUwZjhkNjkxNmVjZCJ9) to interact with the dashboard 

![](https://github.com/blessingekwere/Global-Terrorism-/blob/main/Global%20Terrorism-1%20(2).jpg)
#### *Dashboard of the global terrorism attack for year 1970-2020*



## Recommendation
According to estimates, the world population in 1969 was around 3.6 billion people, while as of 2021, it is estimated to be around 7.9 billion people. Please note that these figures are approximate and may vary based on different sources and methodologies but you can find a reference for the world population [here](https://www.macrotrends.net/countries/WLD/world/population) 

Global terrorism has undoubtedly affected the population and lives of humans in various ways. The insights from the global terrorism dataset such as the high number of attacks, casualties, and the impact on different groups and regions, highlight the significant consequences of terrorism on human lives and societies. The loss of lives, injuries, and psychological trauma resulting from terrorist attacks have a profound and lasting impact on individuals, families, and communities.

The effect of global terrorism extends beyond the immediate human toll. It disrupts social cohesion, erodes trust, hampers economic development, and destabilizes nations. Terrorism can lead to displacement, migration, and the displacement of communities, further exacerbating social and humanitarian challenges. Moreover, the fear and insecurity generated by terrorism can impede progress in education, healthcare, and other areas of human development.

Based on the analysis of the global terrorism dataset, the following recommendations can be made:

* Strengthen international collaboration: Given the global nature of terrorism, it is crucial for countries to enhance collaboration and information sharing to effectively combat this threat. Sharing intelligence, best practices, and coordinating efforts can lead to better prevention and response strategies.

* Focus on high-impact countries: Countries such as Afghanistan, Colombia, India, Iraq, and Pakistan have experienced a significant number of attacks over the years. Allocating resources and implementing targeted counterterrorism measures in these regions can help mitigate the impact of terrorism and protect the population.

* Enhance security measures for high-risk targets: Private citizens, military personnel, police, government institutions, and businesses have been frequent targets of terrorist attacks. Strengthening security measures, implementing surveillance systems, and providing specialized training for personnel working in these sectors can help prevent and respond to attacks more effectively.

* Improve intelligence gathering and analysis: Investing in advanced technologies and intelligence capabilities can enhance the collection, analysis, and interpretation of terrorism-related data. By identifying patterns, trends, and emerging threats, governments and security agencies can proactively address potential risks.

* Counter radicalization efforts: Understanding the ideologies and factors that drive individuals to join terrorist groups is crucial. Implementing comprehensive counter-radicalization programs that address social, economic, and political grievances can help prevent individuals from being influenced by extremist ideologies.

* Strengthen border security: Enhancing border control measures and cooperation between countries can help curb the movement of terrorists, weapons, and illicit funds. Robust border security measures, including advanced screening technologies and intelligence sharing, are essential for preventing cross-border terrorism.

* Promote community engagement and resilience: Building strong community relationships and fostering trust between law enforcement agencies and local communities can aid in identifying and preventing potential threats. Encouraging community engagement programs, promoting inclusive policies, and addressing social divisions can help create a resilient society less susceptible to extremist ideologies.

* Support victims and survivors: Providing comprehensive support and rehabilitation services for victims and survivors of terrorist attacks is crucial. This includes medical care, psychological support, financial assistance, and legal aid to help rebuild their lives and restore their sense of security.

* Continuously update and refine the dataset: Regularly updating and expanding the dataset with new information, including emerging terrorist groups, evolving attack tactics, and emerging trends, can provide more accurate and comprehensive insights for future analysis and decision-making.

* Foster international dialogue and cooperation: Convening international forums, conferences, and workshops focused on counterterrorism efforts can facilitate knowledge
sharing, foster collaboration, and encourage the exchange of best practices among governments, security agencies, and relevant stakeholders.

## Conclusion
The analysis of the global terrorism dataset spanning from 1970 to 2020 has provided valuable insights into the dynamics, trends, and underlying causes of terrorism worldwide. Through rigorous data cleaning, transformation, and exploration, we have uncovered significant findings that contribute to a deeper understanding of this global menace.

The refined dataset, consisting of 26 columns and 209,707 rows, ensured data integrity and accuracy for further analysis. By examining the dataset, we identified patterns and trends in terrorism over the past five decades, including changes in tactics, targets, and geographical spread. We also observed the evolution of terrorist groups and ideologies, providing crucial information for policymakers, security agencies, and researchers.

Moreover, the analysis shed light on the socio-political factors that contribute to terrorism, allowing for a more comprehensive understanding of its root causes. This understanding can guide the development of effective preventive measures and interventions to mitigate the threat and promote global stability.

The findings from the analysis have important implications for counter-terrorism efforts and policy formulation. They provide actionable insights for policymakers to design strategies that address the ever-evolving nature of terrorism. The analysis also highlights the need for continued research and collaboration to stay ahead of emerging threats.

The results from this analysis can facilitate decision-making, and foster informed discussions on global terrorism.

In conclusion, the analysis of the global terrorism dataset has provided comprehensive insights, patterns, and trends that contribute to the collective efforts in combating terrorism. This analysis serves as a foundation for further research, policy development, and security strategies aimed at promoting global peace and security. It is crucial to continuously analyze and monitor global terrorism to adapt and respond effectively to the evolving nature of this threat.

By implementing these recommendations, governments, security agencies, and policymakers can strengthen their counterterrorism efforts, protect communities, and work towards creating a safer and more secure global environment.




# **Google Data Analytics: Capstone - Bellabeat Fitness Tracking App Analysis**

**Author**: Priyanka Nagaraj

## **Introduction**

Bellabeat is a high-tech company that manufactures health-focused products primarily for women. The company makes products and applications that help monitor their health and wellness 
such as activity, stress levels, sleep and other mindful habits. Bellabeat is a successful small company that is looking forward to expand their capabilities and improve their products to
hopefully become a competitive large player in the global smart device market. Urška Sršen, cofounder and Chief Creative Officer of Bellabeat, is determined to unlock new growth oppurtunities and 
believes that can be done by analyzing data from smart device fitness gadgets.

## **Problem Statements**

The Co-founder and Chief Creative Officer of Bellabeat, Urška, wants to develop effective marketing strategies to help unlock new growth oppurtunities for the company. 
She believes this can be done by analyzing consumer data on smart device usage and gaining insights.

## **The Business Task:**

To analyze data to gain insights on how consumers use smart devices.
Use the discovered insights to help guide marketing strategies for the company.
Identify Trends: Discover trends in FitBit app usage and their implications.

## **Preparing data for Analysis**

This data set contains personal fitness data from fitbit users on minute-level output for physical activity, heart rate, and sleep monitoring. 
It also includes information on daily activity, steps, and heart rate that can be used to explore users’ habits. 
First make sure to import all of the dataset as a .csv file to the database server. 

## **Processing of Data**

Here, I will be transforming and organizing data by adding new columns, extracting information and removing empty and duplicates.
In order to get accurate analysis, validate and make sure the dataset does not include any bias, incorrect data, and duplicates.


## **Analysis of Data**

Here, I will be analysing the consumer data to discover trends and patterns.
                                                  
```
                       Analysis

Select Distinct t1.Id, t1.dates_d, sum(t1.METs)as sum_mets, t2.Calories
From [dbo].[minuteMETsNarrow_merged] as t1
inner join dailyActivity_merged as t2
on t1.Id = t2.Id and t1.dates_d = t2.Date_d
Group By t1.Id, t1.dates_d, t2.Calories
Order by dates_d

```
Like this we have to analyze the data by comparing sleep and calories , by analysing daily average analysis by conidering steps, distance and calories.

## **Visualizing Data**

In this phase, we will be visualizing the data analyzed and tables created using Tableau Public.

## **Conclusion**

After collecting, transforming, cleaning, organizing, and analyzing the datasets, we have gathered sufficient evidence to address the business-related questions posed.
Our analysis indicates a strong correlation between the duration and intensity of physical activities and the number of calories burned.
The recommendations I would provide to help solve this business-related scenario is  below.
- Create tailored challenges that align with users' fitness goals, such as step targets, workout intensity, or sleep improvement.
- Offer time-specific promotions and reminders based on peak activity hours (5:00 AM - 9:00 PM). Introduce morning or evening workout challenges, or remind users to get moving during typically inactive periods.
- Implement smart notifications that specifically target users who consistently oversleep or undersleep.
- Design seasonal campaigns (e.g., summer body challenges, winter wellness tips) that align with users’ changing fitness needs throughout the year. Introduce new features or challenges that cater to seasonal activities or common resolutions.

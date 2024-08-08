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
                                                   --Analysis--
--Calculate average met per day per user, and compare with the calories burned

Select Distinct t1.Id, t1.dates_d, sum(t1.METs) as sum_mets, t2.Calories
From [dbo].[minuteMETsNarrow_merged] as t1
inner join dailyActivity_merged as t2
on t1.Id = t2.Id and t1.dates_d = t2.Date_d
Group By t1.Id, t1.dates_d, t2.Calories
Order by dates_d

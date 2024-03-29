---
author: Solomon
pubDatetime: 2023-01-30T15:57:52.737Z
title: Earthquake Events - Data Engineering project
slug: project-1
featured: false
dataEngineering: true
ogImage: https://resilienceyouthnetwork.org/wp-content/uploads/2022/07/2560px-USGS_logo_green.svg_-1024x410.pnga781-1f3d93bdf0ec.png
tags:
 - project 
 - data Engineering
 - DBT
 - Azure
 - Snowflake
 - Tableau
description: USGS Earthquake Data - Data Engineering project using DBT, Azure ADF, Snowflake, Tableau
---

USGS Earthquake Data - Data engineering to analyze Earthquake events - ETL project using DBT, Azure ADF, Snowflake and Tableau


[View dashboard](https://public.tableau.com/app/profile/solomon8607/viz/EarthquakeEvents/Dashboard1)
<svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="100" height="100" viewBox="0 0 48 48">
<rect width="1.5" height="9" x="22.75" y="1" fill="#78909c"></rect><rect width="9" height="1.5" x="19" y="4.75" fill="#78909c"></rect><rect width="1.5" height="9" x="40.75" y="19" fill="#5c6bc0"></rect><rect width="9" height="1.5" x="37" y="22.75" fill="#5c6bc0"></rect><rect width="1.5" height="9" x="4.75" y="19" fill="#78909c"></rect><rect width="9" height="1.5" x="1" y="22.75" fill="#78909c"></rect><rect width="1.5" height="9" x="22.75" y="37" fill="#5c6bc0"></rect><rect width="9" height="1.5" x="19" y="40.75" fill="#5c6bc0"></rect><rect width="17" height="3" x="15" y="22" fill="#e8762d"></rect><rect width="3" height="17" x="22" y="15" fill="#e8762d"></rect><rect width="2" height="14" x="11" y="6" fill="#ffa000"></rect><rect width="14" height="2" x="5" y="12" fill="#ffa000"></rect><rect width="2" height="14" x="34" y="6" fill="#607d8b"></rect><rect width="14" height="2" x="28" y="12" fill="#607d8b"></rect><rect width="2" height="14" x="11" y="27" fill="#c62828"></rect><rect width="14" height="2" x="5" y="33" fill="#c62828"></rect><rect width="2" height="14" x="34" y="27" fill="#0d47a1"></rect><rect width="14" height="2" x="28" y="33" fill="#0d47a1"></rect>
</svg>

[Github](https://github.com/solo11/Data-engineering-project-2/)
<svg
    xmlns="http://www.w3.org/2000/svg"
    class="icon-tabler"
    stroke-linecap="round"
    stroke-linejoin="round">
    <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
    <path
      d="M9 19c-4.3 1.4 -4.3 -2.5 -6 -3m12 5v-3.5c0 -1 .1 -1.4 -.5 -2c2.8 -.3 5.5 -1.4 5.5 -6a4.6 4.6 0 0 0 -1.3 -3.2a4.2 4.2 0 0 0 -.1 -3.2s-1.1 -.3 -3.5 1.3a12.3 12.3 0 0 0 -6.2 0c-2.4 -1.6 -3.5 -1.3 -3.5 -1.3a4.2 4.2 0 0 0 -.1 3.2a4.6 4.6 0 0 0 -1.3 3.2c0 4.6 2.7 5.7 5.5 6c-.6 .6 -.6 1.2 -.5 2v3.5"
    ></path></svg>

----
![Architecture](https://github.com/solo11/Data-engineering-project-2/assets/32461868/179f2c44-d2f8-4eaf-9953-9a65383b660b)

## Table of contents


## Source

**USGS.GOV**  - https://earthquake.usgs.gov/fdsnws/event/1
The website provides daily activities of earthquake events recorded, using the API the csv file is loaded

## Azure ADF

Using the Azure data factory copy activity, the data is scheduled to load every day to Snowflake
CSV data is extracted using REST API and loaded to the Snowflake warehouse

<img width="1332" alt="Screenshot 2024-03-27 at 6 13 38 PM" src="https://github.com/solo11/Data-engineering-project-2/assets/32461868/081ebe19-c332-41d8-b032-9e10c65c4ef2">


## Snowflake

Used as a data warehouse to store the raw data and connected to DBT for transformations the updated data is merged into the final table, Tableau uses the final table to update the dashboard.

## DBT

DBT cloud is used for data transformations and data cleaning, countries data is extracted from lat and log values and added after applying the transformations the changes are merged into Snowflake. DBT is also scheduled to run every day.

**Lienage graph**
<img width="1284" alt="Screenshot 2024-03-27 at 5 21 19 PM" src="https://github.com/solo11/Data-engineering-project-2/assets/32461868/e324b0b2-4aad-48fe-9f4f-5dda08b4cb61">

## Tableau

Tableau dashboard with data visualizations and graphs - https://public.tableau.com/app/profile/solomon8607/viz/EarthquakeEvents/Dashboard1

Screenshots:

<img width="1076" alt="Screenshot 2024-03-27 at 6 11 36 PM" src="https://github.com/solo11/Data-engineering-project-2/assets/32461868/0c608c5d-6866-4643-9275-55955334a22a">



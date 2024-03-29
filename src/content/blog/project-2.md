---
author: Solomon
pubDatetime: 2023-01-30T15:57:52.737Z
title: Buffalo Reality - Data Engineering project
slug: project-2
featured: false
dataEngineering: true
ogImage: https://d1nhio0ox7pgb.cloudfront.net/_img/o_collection_png/green_dark_grey/512x512/plain/houses.png
tags:
 - project 
 - data Engineering
 - Databricks
 - Azure
 - Tableau
description: Data engineering project using Databricks, web-scraping, Azure blob storage, Azure SQL database and Tableau

---

Buffalo Housing data - Data engineering project using Databricks, web-scraping, Azure blob storage, Azure SQL database and Tableau to analyze and visualize the housing market in Buffalo.



[View dashboard](https://public.tableau.com/views/Book1_17097820994780/Story1?:language=en-US&:sid=&:display_count=n&:origin=viz_share_link)
<svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="100" height="100" viewBox="0 0 48 48">
<rect width="1.5" height="9" x="22.75" y="1" fill="#78909c"></rect><rect width="9" height="1.5" x="19" y="4.75" fill="#78909c"></rect><rect width="1.5" height="9" x="40.75" y="19" fill="#5c6bc0"></rect><rect width="9" height="1.5" x="37" y="22.75" fill="#5c6bc0"></rect><rect width="1.5" height="9" x="4.75" y="19" fill="#78909c"></rect><rect width="9" height="1.5" x="1" y="22.75" fill="#78909c"></rect><rect width="1.5" height="9" x="22.75" y="37" fill="#5c6bc0"></rect><rect width="9" height="1.5" x="19" y="40.75" fill="#5c6bc0"></rect><rect width="17" height="3" x="15" y="22" fill="#e8762d"></rect><rect width="3" height="17" x="22" y="15" fill="#e8762d"></rect><rect width="2" height="14" x="11" y="6" fill="#ffa000"></rect><rect width="14" height="2" x="5" y="12" fill="#ffa000"></rect><rect width="2" height="14" x="34" y="6" fill="#607d8b"></rect><rect width="14" height="2" x="28" y="12" fill="#607d8b"></rect><rect width="2" height="14" x="11" y="27" fill="#c62828"></rect><rect width="14" height="2" x="5" y="33" fill="#c62828"></rect><rect width="2" height="14" x="34" y="27" fill="#0d47a1"></rect><rect width="14" height="2" x="28" y="33" fill="#0d47a1"></rect>
</svg>

[Github](https://github.com/solo11/Data-engineering-project-1)
<svg
    xmlns="http://www.w3.org/2000/svg"
    class="icon-tabler"
    stroke-linecap="round"
    stroke-linejoin="round">
    <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
    <path
      d="M9 19c-4.3 1.4 -4.3 -2.5 -6 -3m12 5v-3.5c0 -1 .1 -1.4 -.5 -2c2.8 -.3 5.5 -1.4 5.5 -6a4.6 4.6 0 0 0 -1.3 -3.2a4.2 4.2 0 0 0 -.1 -3.2s-1.1 -.3 -3.5 1.3a12.3 12.3 0 0 0 -6.2 0c-2.4 -1.6 -3.5 -1.3 -3.5 -1.3a4.2 4.2 0 0 0 -.1 3.2a4.6 4.6 0 0 0 -1.3 3.2c0 4.6 2.7 5.7 5.5 6c-.6 .6 -.6 1.2 -.5 2v3.5"
    ></path></svg>

---
![Architecture](https://github.com/solo11/Data-engineering-project-1/assets/32461868/0e0b245d-a684-422f-b630-59244008d3fc)



## Table of contents

## Source

**Home Harvest**  - https://github.com/Bunsly/HomeHarvest
HomeHarvest is a real estate scraping library that extracts and formats data in the style of MLS listings.
Scraping data from Zillow, Redfin and realtor.com

## Databricks

Databricks is used to load, process and transform the data to load into the Azure SQL database

The JSON data is extracted and loaded into a dataframe, cleaned, transformed and loaded into the warehouse


## Azure SQL DB

Used as a data warehouse to store the raw data and connected to Databricks for transformations the updated data is merged into the final table, Tableau uses the final table to update the dashboard.


## Tableau

Tableau dashboard with data visualizations and graphs - https://public.tableau.com/views/Book1_17097820994780/Story1?:language=en-US&:sid=&:display_count=n&:origin=viz_share_link

Screenshots:

<img width="1076" alt="Screenshot 2024-03-27 at 6 11 36 PM" src="https://github.com/solo11/Data-engineering-project-1/assets/32461868/db1dc1c4-353a-4b1d-8194-f7efb0ad4ceb">


<img width="1076" src="https://github.com/solo11/Data-engineering-project-1/assets/32461868/0f6cc532-8e6a-479c-a062-3c5412c5ca7b">


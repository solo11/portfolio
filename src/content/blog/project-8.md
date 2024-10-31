---
author: Solomon
pubDatetime: 2024-10-30T15:57:52.737Z
title: GDELT Project - Data Engineering project
slug: project-8
featured: false
dataEngineering: true
ogImage: https://resilienceyouthnetwork.org/wp-content/uploads/2022/07/2560px-USGS_logo_green.svg_-1024x410.pnga781-1f3d93bdf0ec.png
tags:
 - project
 - polars
 - DuckDB
 - Data Engineering
 - Azure
description: GDELT Events data - dashboard and react app
---

A Global Database of Society - the GDELT Project monitors the world's broadcast, print, and web news from nearly every corner of every country in over 100 languages and identifies the people, locations, organizations, themes, sources, emotions, counts, quotes, images and events driving our global society every second of every day, creating a free open platform for computing on the entire world


[React App](https://gdelt-project.vercel.app/)


[Evidence Dashboard](https://gdelt-project.evidence.app/)


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
![Architecture](https://github.com/user-attachments/assets/d5ab108f-e8aa-4e73-9cd8-477f5d4628b5)

React App

## Table of contents

The output of this project is
- A React web app that shows the world map with pointers on daily events, this data is refreshed daily.

- An Evidence.dev dashboard, this dashboard further provides more info on the data collected.

## Source

**The GDELT Project**  - https://www.gdeltproject.org/



The GDELT project is a massive data scraping project recording the events occuring all over the world and is refreshed every 15 minutes, in this project I focus on the events table - the raw data file is extracted daily.


## Data ingestion, cleaning and transformation

A python script which extract the raw data file and cleans filters the columns needed and drops the data where the event category is not available, Polars is used for transformations. 

The title is scraped and extracted for each record from its article web page using beautifulsoup.

The data then is loaded into Azure cosmos and MotherDuck. 

The Fast API server is connected to a Azure Cosmos and exposes the API which is used by the React App to get data and update.

Dashboard made using Evidence.dev is connected to the MotherDuck database and is refreshed daily.

Sources: 
https://www.gdeltproject.org/

Screenshots:

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/d9f4a4f3-ba77-4bb3-8afd-91b7b6f5f66e">
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/36190faa-8d16-4f98-8680-baaec2e9736d">




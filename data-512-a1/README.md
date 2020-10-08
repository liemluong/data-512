University of Washington | Autumn 2020 | Data 512 - Human Centered Data Science

Assignment 1: Data Curation

BRIEF INTRODUCTION:
-------------------
The goal of this assignment is to perform an analysis to track the English Wikipedia traffic view from two different Wikimedia REST API endpoints. In details, we construct, analyze, and publish a visualization of monthly traffic on English Wikipedia from January 1 2008 through August 30 2020.
The analysis is carried out in a single Jupyter notebook. A copy of the Jupyter notebook, its data, and documentation are published in this single GitHub repository

DATA SOURCE:
------------
The license of the source data conforms to the Wikimedia Foundation REST API
Terms of use: https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions

The data source of this analysis are collected from the two different API endpoints:
- The Legacy Pagecount API
--- Note: This provides access to desktop and mobile traffic data from December 2007 through July 2016
--- Documentation: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts
--- Link to Endpoint: https://wikimedia.org/api/rest_v1/#/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end

- The Pageview API
--- Note: This provides access to desktop, mobile web, and mobile app traffic data from July 2015 through last month
--- Documentation: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews
--- Link to Endpoint: https://wikimedia.org/api/rest_v1/#/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end

FINAL DATA FILE:
----------------
After performing the data gathering, data transformation, and data joining from five separate JSON data results to produce the final data file, the final version is data file is comprehensive and clean CSV format.
This final CSV file has the following data fields:

Data Fields                      Value          Description
-------------------------------------------------------------------------------------------------------------------------------------------------------
- year - [YYYY] - The year in which the traffic data on the English Wikipedia values being collected

- month - [MM] - The month in which the traffic data on the English Wikipedia values being collected (monthly statistic)

- pagecount_all_views - [num_views] - Number of total views for the legacy pagecount API of all views (desktop & mobile)

- pagecount_desktop_views - [num_views] - Number of total views for the legacy pagecount API of desktop view only

- pagecount_mobile_views - [num_views] - Number of total views for the legacy pagecount API of mobile view only

- pageview_all_views - [num_views] - Number of total views for the new pageview API of all views (desktop & mobile)

- pageview_desktop_views - [num_views] - Number of total views for the new pageview API of desktop view only

- pageview_mobile_views - [num_views] - Number of total views for the new pageview API of mobile view only

HELPFUL NOTES:
--------------
1. Organic user traffic is important and therefore it is valuable than the automated web crawlers or spiders. The new Pageview API has the option to filter by agent = user whereas the legacy Pagecount API doesn't have. You should consider to use this organic user traffic in your API call for better result.

2. Where the legacy Pagecount API ended and new Pageview API started, there was an overlapping traffic data from about 1 year (July 2015 to July 2016).

3. In the final result data file, value 0 indicates there were 0 views for that particular month in year for a given access method (e.g. desktop, mobile, etc.)

4. The code in the Jupyter notebook walks you through the steps by steps and should be executed in sequence.


---
title: A Machine Learning Based Approach, For Predicting Road Closure Events, Given Data of the US Road Construction and Closure
keywords:
- markdown
- publishing
- manubot
lang: en-US
date-meta: '2022-09-18'
author-meta:
- Amirthavarshini Muraleetharan
- Thomas Ngare
- Kapil Shah
header-includes: |-
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta name="dc.title" content="A Machine Learning Based Approach, For Predicting Road Closure Events, Given Data of the US Road Construction and Closure" />
  <meta name="citation_title" content="A Machine Learning Based Approach, For Predicting Road Closure Events, Given Data of the US Road Construction and Closure" />
  <meta property="og:title" content="A Machine Learning Based Approach, For Predicting Road Closure Events, Given Data of the US Road Construction and Closure" />
  <meta property="twitter:title" content="A Machine Learning Based Approach, For Predicting Road Closure Events, Given Data of the US Road Construction and Closure" />
  <meta name="dc.date" content="2022-09-18" />
  <meta name="citation_publication_date" content="2022-09-18" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="Amirthavarshini Muraleetharan" />
  <meta name="citation_author_institution" content="Department of CEE, University of Illinois Urbana Champaign" />
  <meta name="citation_author_orcid" content="677-010-487" />
  <meta name="citation_author" content="Thomas Ngare" />
  <meta name="citation_author_institution" content="Department of CEE, University of Illinois Urbana Champaign" />
  <meta name="citation_author_orcid" content="652-601-317" />
  <meta name="citation_author" content="Kapil Shah" />
  <meta name="citation_author_institution" content="Department of CEE, University of Illinois Urbana Champaign" />
  <meta name="citation_author_orcid" content="668-376-620" />
  <link rel="canonical" href="https://uiceds.github.io/cee-492-term-project-fall-2022-jakt/" />
  <meta property="og:url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-jakt/" />
  <meta property="twitter:url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-jakt/" />
  <meta name="citation_fulltext_html_url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-jakt/" />
  <meta name="citation_pdf_url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-jakt/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://uiceds.github.io/cee-492-term-project-fall-2022-jakt/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://uiceds.github.io/cee-492-term-project-fall-2022-jakt/v/d0e36a283bcaf6e902a1ec75b51c99e9e983dc00/" />
  <meta name="manubot_html_url_versioned" content="https://uiceds.github.io/cee-492-term-project-fall-2022-jakt/v/d0e36a283bcaf6e902a1ec75b51c99e9e983dc00/" />
  <meta name="manubot_pdf_url_versioned" content="https://uiceds.github.io/cee-492-term-project-fall-2022-jakt/v/d0e36a283bcaf6e902a1ec75b51c99e9e983dc00/manuscript.pdf" />
  <meta property="og:type" content="article" />
  <meta property="twitter:card" content="summary_large_image" />
  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />
  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />
  <meta name="theme-color" content="#ad1457" />
  <!-- end Manubot generated metadata -->
bibliography:
- content/manual-references.json
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
manubot-clear-requests-cache: false
...






<small><em>
This manuscript
([permalink](https://uiceds.github.io/cee-492-term-project-fall-2022-jakt/v/d0e36a283bcaf6e902a1ec75b51c99e9e983dc00/))
was automatically generated
from [uiceds/cee-492-term-project-fall-2022-jakt@d0e36a2](https://github.com/uiceds/cee-492-term-project-fall-2022-jakt/tree/d0e36a283bcaf6e902a1ec75b51c99e9e983dc00)
on September 18, 2022.
</em></small>

## Authors



+ **Amirthavarshini Muraleetharan**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [677-010-487](https://orcid.org/677-010-487)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [amirthavarshini246](https://github.com/amirthavarshini246)<br>
  <small>
     Department of CEE, University of Illinois Urbana Champaign
  </small>

+ **Thomas Ngare**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [652-601-317](https://orcid.org/652-601-317)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [thomasNg](https://github.com/thomasNg)<br>
  <small>
     Department of CEE, University of Illinois Urbana Champaign
  </small>

+ **Kapil Shah**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [668-376-620](https://orcid.org/668-376-620)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [kapilrs2](https://github.com/kapilrs2)<br>
  <small>
     Department of CEE, University of Illinois Urbana Champaign
  </small>



## Abstract {.page_break_before}

A nationwide dataset of road construction and closure events, including data from all 49 US states is chosen for the project. The roadwork included in this dataset's construction events ranges from minor paving repairs to significant undertakings that might take months to complete. Several APIs that provide streaming traffic incident (or event) data are used to collect the data between January 2016 and December 2021. These APIs transmit traffic information gathered by several organizations, including the US and state departments of transportation, law enforcement organizations, traffic cameras, and traffic sensors embedded in the road networks. The number of construction and shutdown records in this dataset currently stands at roughly 6.2 million. 
In general, this dataset can be used for a wide range of applications, including the prediction of short- and long-term road construction, the prediction of road closures, the study of the life cycle of road construction, the development of insights to help city planners choose construction sites wisely with the most negligible negative impact on traffic flow, and the investigation of the influence of precipitation or other environmental stimuli on the need for road work. The dataset is being updated on an annual basis. The data will be obtained from US Road Construction and Closures (2016 - 2021), Kaggle, and it is available in CSV format. Presently, the dataset contains 6,170,627 observations comprising of features like Construction severity, Latitude and longitude, Precipitation, Traffic signal and many such taking a total of 47 columns. Table @tbl:features elaborates the specifics of this data set.
		
Using this dataset, a machine learning model will be developed to predict road closure events, given inputs of pertinent features as mentioned in the below table @tbl:features. measurements from pertinent features that will be determined in this study. The developed algorithm will be tested on about 20% of the total samples, and validated with another 20% of the total samples, to be made suitable for real-time applications. The proposed algorithm will have the potential to estimate the likelihood that every road segment satisfying certain requirement will be is closed or open, such that it can be employed in mobile maps (like Google maps). Whenever the likelihood of a closure event exceeds a predetermined threshold, customer can be notified to find the efficient route. For mapping applications, this algorithm can it will automatically update maps further add to its real time monitoring. 

To achieve this goal, data wrangling will be performed. The essential data frames for the study will be extracted from the original dataset followed by exploratory analysis. Exploratory analysis will enable us to drive insights by forming a pattern for better visualization and exploration be performed to make sense of the data and visualize them for better exploration. Based on the analysis, a classification model will be developed to predict the class or category for the data or draw a conclusion to the input data given for training. The developed model will be tested for various conditions.

|[Features]{.center}|[Description]{.center}|
|:------------|:-------------------------------------|
|ID|Unique identifier of construction record|
|Severity|Shows the severity of the construction|
|Start and End Time|Shows the start time of construction|
|End Time|Shows the end time of construction|
|Latitude and Longitude|Shows the GPS coordinates|
|Distance|The length of the road extent affected by the construction|
|Street Details|Shows the street number, name and right/left side in address field|
|Address Details|Shows the city, county, state, country and zip code in address field|
|Time zone|Shows time zone based on the location of the construction event|
|Weather|Shows the time stamp of weather observation record|
|Temperature, Wind, Humidity, and Pressure|Shows the temperature, wind chill, humidity, and pressure|
|Visibility|Shows visibility|
|Wind Direction and Speed|Shows wind conditions|
|Precipitation and Weather condition|Shows precipitation and weather condition|
|Amenity|An annotation which indicates presence of amenity in a nearby location|
|Bump and Crossing|Annotations which indicate presence of speed bump or hump and crossings|
|Give way, Junction, railway|Annotations which indicate presence of give way, junction and railway|
|Exit, Roundabout, Station, Stop|Annotation which indicates presence of no exit, railway, roundabout, and station|
|Traffic Details|Annotations which indicate traffic calming, signal, turning loop|
|Light Details|Annotations which indicate sunrise, sunset, civil twilight, nautical twilight, astronomical twilight|

Table: Description of Undertaking Dataset
{#tbl:features}

Once successfully tested, this algorithm can further be developed (given the time permits) to choose construction sites which has less impact of traffic flow, thereby guiding city planners. Also, a study can be undertaken to understand the impact of precipitation on the need of road work. 

[References:]{.semibold}

1. Karimi Monsefi, Amin, Sobhan Moosavi, and Rajiv Ramnath. “Will there be a construction? Predicting road constructions based on heterogeneous spatiotemporal data.”, _2022_

2. US Road Construction and Closures _2016 - 2021 from Kaggle_
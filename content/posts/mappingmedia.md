---
draft: false
title: Mapping Media - A Qualitative Approach to Estimating Globals News Coverage"
image: https://cdn.britannica.com/25/93825-050-D1300547/collection-newspapers.jpg
tags: [python, adverse media, qualitative research]
---

Recently I was asked to join the adverse media team as their new researcher. While the team had a robust database of news sources, they had no way of knowing what news sources exist in different countries. Not knowing "what's out there" made it difficult to identify gaps in our data, so I set out to build a knoweldge base of the world's news sources.

## Identifying sources

Identifying the world’s news sources is not straightforward. Comprehensive lists of newspapers worldwide do not exist. To estimate available news sources in a country, I developed a research process for collating a comprehensive list of news sources in different countries.


### DBPedia & Wikipedia Lists

Wikipedia is a rich source of information for identifying newspapers in a country. You can use search terms like “list of newspapers in [country]” to find these lists. Wikipedia has two strengths. It usually labels newspapers as national and regional, aiding in labelling easier. Most newspapers also have their own dedicated Wikipedia page with detailed information, such as circulation, owners, and publication status.

You can use the DBPedia scraper to extract information about newspapers in a country. Add the name of the country to the query and the script will iterate through all of the hyperlinks on the page and extract information from the information boxes. 

One thing to keep in mind is that the DBPedia scraper extracts information from all of the hyperlinks on a page, including irrelevant pages like towns or regions. You can filter for "newspaper" type only if you want to avoid cleaning the data. However, filtering reduces the number of hits substantially since DBPedia data is not properly organised. My recommendation is to not filter as the ratio of irrelevant data to newspapers is low.

### Official Directories

Official directories list registered national and regional newspapers and can be found via Google searcher or on a country’s press ombudsman’s website. While these directories often only provide the name and domain of media sources, their official status make them valuable sources of truth.   

### Open-source projects and Unofficial Directories

Several unofficial directories and open-source projects, like WorldMap, contain names and domains of thousands of newspapers worldwide. Additionally, blog posts for language learners and media directories hosted by companies offer useful lists. These sources can supplement official directories, though they may require verification.

## Collating multiple sources of truth into a knowledge base

To estimate media sources in any country, we create a country research sheet on Google Drive and store data from each directory in separate tabs:

<b>Wikipedia</b> : Use DBPedia scraper to extract information from the country’s list of newspapers page. Clean the data to remove irrelevant information, such as ceased publications.

1. **WorldMap**: Run the world newspaper map scraper to collect data from this open-source project.

2. **Official Directories**: Add data manually or with a script from press directories. 

3. **Company Data**: Include our existing database in its own tab. Filter by country code and extract our domains for that country. 

4. Other sources: Add any additional identified sources. 

## Labelling and Collating Sources

The next step is to manually label sources based on our typology, determining their classification. This process is facilitated by first collating sources and then filtering out those without a taxonomy. Collation involves merging research tabs into a master list that serves as our knowledge base of media sources in a country. 

## The Result

The result is a comprehensive list of the adverse media team’s newspapers and the sources we believe exist in each country. With this collated list, our sales team can identify the number and types of media sources we cover. Internally, we can spot data gaps and review new sources for inclusion. Sources rejected in the review are flagged with reasons for their exclusion, maintaining a clear and up-to-date database.




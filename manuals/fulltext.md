---
title: Full-text Search
layout: default
---

### Table of content
1. [Full-text Search](#full-text-search)
    - [Search expressions](#search-expressions)
    - [Search syntax and logical operators](#search-syntax-and-logical-operators)
2. [Options](#options)
    - [Choose corpus](#choose-corpus)
    - [Sample size](#sample-size)
3. [Results](#results)


# Full-text Search
You might want to research events, phenomena or actors that are hard to find with the URL Search. That is why NWA is developing a full-text search engine.  
  
The prototype for full-text search generally works like many other search engines. Beneath the hood is an extensive index with natural language extracted from HTML. When you enter a query, the engine will search through the index and return results with documents that match your search expression.  

## Search expressions
To search, you simply need to enter a word or phrase in the search field.
If you want to search for an exact phrase, you put two or more words within “question marks”.  

## Search syntax and logical operators
Space between words or phrases works the same way as AND. This will limit your query and only return documents that contains all of the word/phrases you enter.  
  
You can also use OR as a logical operator between words/phrases. This will increase the amount of results, and return documents that contains at least one of the words/phrases.  

# Options
In the sidebar, you can choose between different options that will affect your result.  

## Choose corpus
Below “Velg korpus” (eng. “Choose corpus”), you can choose which period you want to search. The two periods (2005-14 and 2019-) refer to the point of time for harvesting. The reason for this is that the engine is working with two separate indexes. Currently, it is only possible to search one of these at a time.  

## Sample size
In cases where many documents match your search expression, the service will randomly sample the resources before returning results. This is due to hardware limitations, and we hope to improve this in the future.  
  
You can manually adjust the sample size, but increased results imply an increased time before results are returned. Further, the sample percentage is automatically limited to 10 times the value of “Maksimalt antall treff”.  
  
If your result contains a high number of documents, we recommend that you narrow down your search. A valuable way to do this is to change your search expression by adding one or more words/phrases you expect to be present in relevant sources.  

# Results
When your search results are returned, you will find valuable information below the search bar.  
  
The first number indicates the total amount of documents in the index that matches your query. The second number shows how many of these were sampled, while the third number refers to the number of matches displayed in the result list below.  
  
For each document listed in the result, you will find some core information about the document. First, you see the date of harvesting and its original URL. The URL is hyperlinked, and if you click the link, your browser will open a version of the document in our Wayback Machine.

Unlike the results you retrieve in Google, our results are not ranked by relevance. We work on different ways to sort results (by date, etc.), but at the moment, the service presents the most recently archived document on top.
---
title: URL search
layout: default
nav_order: 1
---


### Table of content
1. [URL - the address of web resources](#url--the-address-of-web-resources)
2. [Different search modes](#different-search-modes)
    - [Default search](#default-search)
    - [Prefix search](#prefix-search)
    - [Host search](#host-search)
    - [Domain search](#domain-search)
3. [Limiting date/time range](#limiting-datetime-range)
    - [Timestamps and timecode](#timestamps-and-timecode)
4. [Filtering](#4-filtering)
    - [MIME-type](#mime-type)
    - [Status](#http-response-status)
    - [URL](#url)
    - [Adding filters](#adding-filters)

# URL search
A core function in web archives is to search for specific URLs or domain names.[^1] This is significantly different from archives with digitised printed material, where you often would search for authors, titles or Dewey codes, added manually by a librarian.  
  
Archived web resources are no longer online and are actually contained in a format called WARC. However, metadata about their original URLs makes it possible to search for all the archived resources that have been indexed so far.


## 1. URL – the address of web resources
To understand how URL query works, it is beneficial to know what a URL is.  
In simple terms, this is the address of a specific resource on the web. If you visit a friend’s new apartment for the first time, you will probably navigate to her street address. Similarly, the URL tells your browser where to find the resource you want to visit.  
  
Before you search for URL, it is highly beneficial to be familiar with the following terms:  
![](img/urlModel.png)


## 2. Different search modes
The URL search has four different search modes: **Default**, **Prefix**, **Host** and **Domain**. These modes provides different ways to search the archive.

### Default search
In default mode, you search for resources with an exact URL. This is very useful to find front pages, or to locate specific resources (supposing that you know its URL).  
  
To make a query, enter the desired URL and press “Search”.  
  
The service will return matches, displayed in a list, with information about the different points of time when the resource was requested by our harvester.

### Prefix search
In prefix mode, you search for resources that starts in a specific way. In practice, prefix searches puts a wildcard on the end of the text you enter.  
  
If you search for `http://www.hoyre.no/1997` as a prefix, the service will return all resources with a URL that starts with this string – including images, audio, and application scripts. This is especially useful if you want to locate resources from a specific web site or path. Using filters, you can limit your query further (see also [Filtering](#4-filtering)).

### Host search
In host mode, you make a query for resources from a specific host. The engine will ignore protocol, port, path and parameters but is sensitive to subdomains.  
  
If you search for `vg.no` , you will get results which exactly matches vg.no as host, and ignore resources with additional sub domain, such as direkte.vg.no or www.vg.no in the URL. The sensitivity for subdomains in host mode is thus beneficial if you search for resources on a specific subdomain, such as live.vg.no .

### Domain search
Domain mode is similar to host mode but has no sensitivity for subdomains. In practice, the search engine will put a wildcard before the text you enter and ignore any following path or parameter.  
  
Searching for `vg.no` will return resources from this domain, including different subdomains such as live.vg.no.  
  
Since Domain mode ignores everything before the text you enter, you can use this mode to search for resources from a specific top-level domain, such as `edu` , `co.uk` or `com` . The drawback of this strategy is that you ask the engine to search through enormous amounts of data, often causing a time out from the server and a result with 0 resources. 

## 3. Limiting date/time range
Unlike Google, our search engine does not rank results by any kind of relevance. Often, you will therefore need to limit the scope of your query further.  
  
An effective way to limit the scope of your search is to define a date/time range, with a start and end date for harvesting.  
  
Values in the fields **FROM** and **TO** works inclusively, returning results also on this day.

### Timestamps and timecode
The technical term for date/time in web archives is timestamp. Each resource has a 14-digit timestamp on the format **YYYYMMDDHHMMSS**. This refer to the point of time when our harvester collected the resource - not to the publication of the resource.  
  
Timestamps are UTC, which means summer time is not taken into account. If the minutes and hours are important for your analysis, there might be necessary to calculate UCT into local time. This also imply date sensitivity during summer time, as resources harvested around midnight will have different dates in UCT and CEST.

##	4. Filtering
You can limit the results further by *filtering* your search. It is possible to filter your query by three specific attributes: **MIME type**, **Status** and **URL**.  
  
### MIME-type
MIME-type is a standard for classifying media types on the web. It is written on the format `type/subtype`, where **type** represents the general category of media, and **subtype** identifies the specific kind.  
  
The alternatives for type are `text` , `image` , `audio` , `video` and `application`. For each of these, there is a great variety of subtypes. Some common examples are `text/html` , `image/jpg` , `audio/mp3` and `video/mp4` .    
Technically interested scholars may also be curious to inspect MIME types such as `text/css` , `application/javascript` or `application/json` .  
  
To search for only html files, filter **MIME type** that **Contains** the expression `text/html`.  
  
For an extensive list of MIME types, consult [IANA's list of Media Types](https://www.iana.org/assignments/media-types/media-types.xhtml).[^2]  
  
### HTTP response status
**Status** refers to the HTTP response status of archived resources. This three-digit value indicates how the web server responded to our harvester’s request.  
  
If our harvester asks for an HTML file, and the server returns this successfully, it will provide the status 200, meaning “OK”. Not rarely do servers return a response with status 301, meaning “This resource has been moved; I am redirecting you to the new location of the resource”, or status 404, meaning “I could not find the resource you requested”.  
  
Mozilla is one of several that provides an overview of different HTTP Status codes.[^3]  
  
### URL
Filtering by URL allows you to locate resources containing (or not containing) a particular phrase in the URL. This can be helpful to find specific file names or paths, or to exclude such occurrences.  
  
Searching for `www.hoyre.no` as a prefix, and filtering **by URL** that **contains** the expression `skole` , will return hundreds of resources where skole is part of the URL string.  
  
### Adding filters
Remember to press the “Add filter” button to apply your filter, before you press search.  
  
It is possible to add multiple filters. If you add several filters, they will all apply to your query, returning results that matches all the filters. 


## Footnotes
[^1]: NWA’s prototype for URL Search are based on the pywb index query API. Complete technical documentation can be found in WebRecorder (2023), «Instructions», *GitHub.com*. https://github.com/webrecorder/pywb/blob/main/pywb/templates/instructions.html  
[^2]: IANA, «Media Types», *IANA.org*. Archived by Internet Archive (25.01.2023). https://web.archive.org/web/20230125022711/http://www.iana.org/assignments/media-types/media-types.xhtml  
[^3]: «HTTP response status codes», *Mozilla.org*. Archived by Internet Archive (22.01.2023). https://web.archive.org/web/20230122045630/https://developer.mozilla.org/en-US/docs/Web/HTTP/Status  

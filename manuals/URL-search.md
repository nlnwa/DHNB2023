---
title: URL search
layout: default
---

# URL search
A core function in web archives is the possibility to search for specific URLs or domain names. This is significantly different from archives with, e.g. digitised printed material, where you often would search for authors, titles or tagged topics.
Archived web resources are no longer online and are actually contained in a format called WARC. However, metadata about their original URLs makes it possible to search for all the resources that have been indexed so far.

**Table of content**
1. [URL - the address of web resources](#url–-the-address-of-web-resources)
2. [Different search modes](#different-search-modes)
  - [Default search](#default-search)
  - [Prefix search](#prefix-search)
  - [Host search](#host-search)
  - [Domain search](#domain-search)

## URL – the address of web resources
To understand how the URL query works, it is beneficial to know what a URL is.
URL is short for Uniform Resource Locator. In simple terms, this is the address of a specific resource on the web. If you visit a friend’s new apartment for the first time, you will probably navigate to her street address. Similarly, the URL tells your browser where to find the resource you want to visit.
A URL consists of several parts. In the URL Search service, it is highly beneficial to be familiar with the following terms:

## Different search modes
The URL search has four different search modes. Each of these modes provides different ways to locate resources in the archive.

### Default search
In the default mode, you can search for resources matching the exact URL you enter. This is very useful to find front pages of specific websites or to locate a specific resource (supposing that you know its URL).
To make a query, enter the desired URL and press “Search”.
The service will return the results, displayed as a list, with information about the different points of time when our harvester requested resources from the URL you search for.

### Prefix search
In the Prefix search, you search for archived resources which start with a given URL. In practice, the search engine puts a wildcard on the end of the text you enter.
If you search for `http://www.hoyre.no/1997` as a prefix, the service will return resources with a URL that begin with the given text – including images, audio, and application scripts. This is especially useful if you want to locate resources harvested from a specific web site or path. The query can also be limited further with a filter (see chapter 3.4).

### Host search
When you search in host mode, you make a query for resources from a specific host. The engine will ignore protocol, path and parameters but is sensitive to subdomains.
I.e., if you search for `vg.no` , the result will present resources matching vg.no without subdomain, but ignore resources with live.vg.no or www.vg.no in the URL.
The sensitivity for subdomains in host mode is highly beneficial if you search for resources on a specific subdomain, such as live.vg.no .

### Domain search
Domain mode is similar to host mode but has no sensitivity for subdomains. In practice, the search engine will put a wildcard before the text you enter and ignore any following path or parameter.
Searching for vg.no will return resources from this domain, including different subdomains such as live.vg.no.
Since Domain mode ignores everything before the text you enter, you can use this mode to search for resources from a specific top-level domain, such as `edu` , `co.uk` or `com` . The drawback of this strategy is that you ask the engine to search through enormous amounts of data, often causing a time out from the server and a result with 0 resources. 

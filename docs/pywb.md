---
title: URL search
layout: default
---

### Table of content
1. [The "Wayback Machine"](#the-wayback-machine)
2. [Navigation](#navigation)
3. [Play audio and video](#play-audio-and-video)
4. [Common errors](#common-error)
    - [pywb error](#"pyw)
    - [URL not found](#url)
    - [Host search](#host-search)
    - [Domain search](#domain-search)
5. [How are pages loaded and reconstructed?](#how-are-pages-loaded-and-reconstructed)


# The “Wayback Machine”
A Wayback Machine is a service that reconstructs a webpage in your browser, using resources from the web archive.  

To scholars, such reconstruction services offer opportunities as well as challenges. Their main strength is the ability to reconstruct web pages with a user experience close to how it once was read online. It also provides a well-known interface which is easy to navigate.  

However, scholarly use of such tools requires critical evaluation. When you request an online web page in your browser, the different resources are gathered and assembled in seconds, producing a document with *synchronised* elements. In contrast, a page reconstructed with archival resources may contain elements archived over an extensive period. Potentially, the resources reassembled in a Wayback Machine can be quite *diachronic*.  

For scholars interested in isolated elements of a specific kind, such as the natural language contained in HTML, or images as separate elements, this is a minor problem. But for those who want to research the web page as a unit – with text, images, etc., assembled “in-line” – there is a need to examine and analyse the timestamps of the different elements.  

From 2019, NWA introduced a self-developed harvester, aiming to harvest pages as they are loaded in a browser. This have reduced the problem of diachrony considerably, but scholars who are interested in web pages as an artefact will still need to be aware of this problem.  

## Navigation
In the top of the page, you have different navigation tools.  

![](img/navbar.png)

Pressing the left/right arrows will lead to the previous or next capture of the resource.  

The calendar symbol will expand/collapse a calendar view of indexed versions, and the bar chart will expand/collapse a timeline with different point of times of harvesting.  

You can also see information about the page URL, the document title (extracted from the HTML `<title>` tag) and the point of time for harvesting.  

![](img/capture-info.png)

## Play audio and video
If you try to open audio or video resources from a URL search result, they will not play automatically in our Wayback Machine, but rather display a blank page.  
To play audio and video in the Wayback Machine, you need to edit the URL manually, adding 
`mp_`  behind the timestamp in the URL path: “20090505133215**mp_**/http”  
(We are of course working to improve this, but ATM this is a manual fix.)


##	Common errors
At the moment, you will probably experience error messages in the replay engine. It is not always easy to estimate the reason for these errors, but here are some examples and possible explanations of different errors.  

### pywb Error 
If the replay engine displays “pywb Error” in big, red text, this is often because one or more of the requested resources is located on a sleeping disk. Reloading the page in your browser usually solve this problem.  

### URL not found 
“URL Not Found”, means the replay engine are not able to find this resource. It may be several reasons for this. For the workshop, a limited amount of resources have been indexed (56 TB of a total 1,8 PB) It might be that we didn’t harvest the resource. But it can also be that it is not indexed at the moment, or that the resource has been removed since last indexation.  

The url **http://www.nettips.co.uk/gruppe.asp%3Fsideid=1** could not be found in this collection.  

### How are pages loaded and reconstructed?
If you open a web page in the Wayback Machine, the service will request resources from our archive. These are stored in our Web Archive Collections, often on “sleeping disks”, which might cause considerable loading time.  
When the resources are returned, parts of the code are rewritten to maintain link functionality between pages, adding timestamps, etc. Further, the page source code is not provided as such, but generated within an inline frame (`<iframe>`).  
Technically interested users who want to understand the “black boxes” of replay engines will find documentation in NWA’s GitHub repositories.

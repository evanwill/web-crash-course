---
title: Web
nav: true
---

# The Web

Most of the world wide web is made up of HTML, CSS, and JS:

- HTML (Hypertext Markup Language) provides the structure and content
- CSS (Cascading Style Sheets) provides the style
- JS (JavaScript) provides the interactivity

When you access a website, the server sends your computer the code, then your browser renders it into a web page that you can view and interact with.

{% include figure.html img="nicolas-picard-241854-unsplash.jpg" alt="spider web" width="65%" %}

## View Source 

Thus, one fascinating aspect of the web is that everyone must share code to participate.

Right click on any web page and select "View page source" to see the code that is being rendered by the browser (shortcut: `Ctrl + U`). 
Or put `view-source:` in front of any URL.

Right click on any element in the page and select “Inspect” or “Inspect Element” to open your browser’s built in developer tools. This is a great way to learn about HTML and to understand how others created the sites you use.


{% include figure.html img="sai-kiran-anagani-61187-unsplash.jpg" alt="code" width="75%" %}

dev tools

# Uniform Resource Locators

Understanding the URLs in your browser address bar is the first step to using web APIs. 
So let's dissect a URL:

{% include alert.md text="`https://example.com/about?key=value#anchor`" align="center" color="success" %}

protocol `://` domain `.` top-level domain (optional port :80) `/` path and filename `?` query with parameters `#` fragment or anchor

- **Protocol:** there is actually more than 100 defined Internet Protocols, however with URLs the most common are [Hypertext Transfer Protocol (HTTP)](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol) or [File Transfer Protocol (FTP)](https://en.wikipedia.org/wiki/File_Transfer_Protocol).
- **Domain:** the [Domain Name System (DNS)](https://en.wikipedia.org/wiki/Domain_Name_System) is often described as a "phone book" that translates easy to understand web addresses into the appropriate [IP addresses](https://en.wikipedia.org/wiki/IP_address) of servers with the desired information. A subdomain can be added in front of the main domain. For example, in `lib.uidaho.edu` > `lib` is a subdomain of `uidaho`, which is a subdomain of the top-level domain `edu`. Occasionally, you may see a port number at the end of the domain which refer to specific communication endpoints that the server is listening on. For the web the standard ports are `:80` (http) and `:443` (https).
- **Path and filename:** these can be imagined like folders and files on the server (and actually are in static web sites). For example, `/about/index.html`, is the index file in the "about" folder. If no filename is given, by default the server provides the file named `index`.
- **Query string:** is added to the end of an URL following a `?` and is given in key value pairs like `key=value`. Multiple pairs can be separated by `&`. The characters must be URL encoded / escaped, since some characters such as space are not allowed in URLs. The queries are processed by the server or javascript, so what exactly they do depends on the page. For example, `/index.php?title=Query_string&action=edit` might return a wiki article in edit mode from a server running PHP.
- **Anchor:** are added to the end of a URL following a `#`. They traditionally correspond to specific element `id` on an HTML page, but are often used by javascript to add other functionality. For example, `/index.html#Chapter1` might jump to a chapter heading in the web page, or `/about.html#help` might pop up a modal.

## Static vs. Dynamic Web

Traditionally, web servers acted more or less like a read-only shared folder of files. 
You can think of a website as a folder of files.
Thus, a **static website** is a collection of HTML, CSS, JS, images, and other files that are delivered exactly as they are on the server to users. 
A URL in a static site generally represents a request for an HTML document in a specific file location.

In contrast a **dynamic website** uses a server-side scripting language to create pages on the fly when a user makes a request. 
Thus a URL represents a query, rather than an existing document on the server. Content, templates, and metadata are usually stored in a database. For example, WordPress uses the scripting language PHP and database MySQL. This enables more complex interactivity such as comments, customized views, user management, and a web-based admin interface.

This workshop focuses on static web

------------------

# Resources 

- [How Does the Internet Work?](https://youtu.be/i5oe63pOhLI) (idealistic Canadian video explains that *The internet is network of networks that connects devices.*)
- Julia Evan's [Networking Zine](https://wizardzines.com/zines/networking/)

---
title: Web
nav: true
---

# The Web

Most of the world wide web is made up of HTML, CSS, and JS:

- **HTML** (Hypertext Markup Language) provides the structure and content
- **CSS** (Cascading Style Sheets) provides the style
- **JS** (JavaScript) provides the interactivity

When you access a website, the server sends your computer the code which your browser renders into a web page that you can view and interact with.
Thus, one fascinating aspect of the web is that everyone must share code to participate.

{% include figure.html img="nicolas-picard-241854-unsplash.jpg" alt="spider web" width="65%" %}

### View Source 

**Right click** on any web page and select "**View page source**" to see the code that is being rendered by the browser (shortcut: `Ctrl + U`). 

Or put `view-source:` in front of any URL in your address bar, for example:
`view-source:https://evanwill.github.io/web-crash-course/`

Right click on any element in the page and select “Inspect” or “Inspect Element” to open your browser’s built in developer tools. This is a great way to learn about HTML and to understand how others created the sites you use.

{% include figure.html img="sai-kiran-anagani-61187-unsplash.jpg" alt="code" width="65%" %}

# Uniform Resource Locators

Of course to get that code we need an web address. 
The links in your address bar are Uniform Resource Locators, **URLs**.

Let's dissect a URL:

{% include alert.md text="`https://example.com/about?key=value#anchor`" align="center" color="success" %}

protocol `://` domain `.` top-level domain (optional port :80) `/` path and filename `?` query with parameters `#` fragment or anchor

<table class="table table-bordered table-striped">
    <tbody>
        <tr>
            <td><strong>Protocol</strong></td>
            <td>there is actually more than 100 defined Internet Protocols, however with URLs the most common is <a href="https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol">Hypertext Transfer Protocol (HTTP)</a>.</td>
        </tr>
        <tr>
            <td><strong>Domain</strong></td>
            <td>the <a href="https://en.wikipedia.org/wiki/Domain_Name_System">Domain Name System (DNS)</a> is often described as a "phone book" that translates easy to understand web addresses into the appropriate <a href="https://en.wikipedia.org/wiki/IP_address">IP addresses</a> of servers with the desired information.</td>
        </tr>
        <tr>
            <td><strong>Subdomain</strong></td>
            <td>(optional) can be added in front of the main domain. For example, in "lib.uidaho.edu" > <code>lib</code> is a subdomain of <code>uidaho</code>, which is a subdomain of the top-level domain <code>edu</code>.</td>
        </tr>
        <tr>
            <td><strong>Port</strong></td>
            <td>(optional) occasionally added at the end of the domain, referring to specific communication endpoints that the server is listening on. For the web the standard ports are <code>:80</code> (http) and <code>:443</code> (https).</td>
        </tr>
        <tr>
            <td><strong>Path + filename</strong></td>
            <td>these can be imagined like folders and files on the server (and actually are in static web sites). For example, <code>/about/index.html</code>, is the index file in the "about" folder. If no filename is given, by default the server provides the file named `index`.</td>
        </tr>
        <tr>
            <td><strong>Query string</strong></td>
            <td>(optional) added to the end of an URL following a <code>?</code> and is given in key value pairs like <code>key=value</code>. Multiple pairs can be separated by <code>&</code>. The characters must be URL encoded / escaped, since some characters such as space are not allowed in URLs. The queries are processed by the server or javascript, so what exactly they do depends on the page. For example, <code>/index.php?title=example&action=edit</code> might return a wiki article in edit mode from a server running PHP.</td>
        </tr>
        <tr>
            <td><strong>Anchor</strong></td>
            <td>(optional) added to the end of a URL following a <code>#</code>. They traditionally correspond to specific element <code>id</code> on an HTML page, but are often used by javascript to add other functionality. For example, <code>/index.html#Chapter1</code> might jump to a chapter heading in the web page, or <code>/about.html#help</code> might pop up a modal.</td>
        </tr>
    </tbody>
</table>

### Static vs. Dynamic Web

Traditionally, web servers acted more or less like a read-only shared folder of files. 
You can think of a website as a folder of files.
Thus, a **static website** is a collection of HTML, CSS, JS, images, and other files that are delivered exactly as they are on the server to users. 
A URL in a static site generally represents a request for an HTML document in a specific file location.

In contrast a **dynamic website** uses a server-side scripting language to create pages on the fly when a user makes a request. 
Thus a URL represents a query, rather than an existing document on the server. 
Think of complex sites such as social media, where users are constantly adding more data and there is no "static" documents, but streams of every changing content.

In these platforms content, templates, and metadata are usually stored in a database. 
For example, the popular [content management systems](https://en.wikipedia.org/wiki/Content_management_system) [WordPress](https://wordpress.com/) and [Drupal](https://www.drupal.org/) use the scripting language PHP and database MySQL.
This enables complex interactivity such as comments, customized views, user management, and a web-based admin interface.

Of course, all that complexity requires a lot of technical overhead... so static sites are experiencing a [renewed boom](https://www.smashingmagazine.com/2015/11/modern-static-website-generators-next-big-thing/), offering simplicity with:

- much faster performance (caching, low bandwidth, no processing time).
- low hosting requirements (simple web servers, no dependencies).
- no security vulnerabilities.
- easy version control.

------------------

# More 

- [How Does the Internet Work?](https://youtu.be/i5oe63pOhLI) (idealistic Canadian video explains that *The internet is network of networks that connects devices.*)
- Julia Evan's [Networking Zine](https://wizardzines.com/zines/networking/)
- [StaticGen](https://www.staticgen.com/) (list of static site generators)
- [Jekyll](https://jekyllrb.com/) (most popular static site generator, built into GitHub Pages)

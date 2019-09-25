---
title: HTML
nav: true
---

# Hypertext Markup Language

HTML is a ["markup language"](https://en.wikipedia.org/wiki/Markup_language) originally designed to describe structured documents for the web.

If you look at the pages of a book or the print out of your term paper, you will see a set of common conventions that we use to communicate structure and meaning.
Document features such as headings, paragraphs, lists, or italics are represented on the page by distinctive styling. 
HTML provides a way to formally mark those types of document elements, *in theory* allowing you to record the semantic structure of the text.
The markup can then be translated by the web browser into visual styles for easy reading.

Of course, as web pages become ever more complicated, HTML has gone far beyond a simple document language!

### Pointy Brackets

HTML is made up of a set of standard **elements** used to structure a web page and introduce features such as images.

Elements are represented by **tags** enclosed by pointy brackets.
Elements may have **attributes** inside the brackets that add additional data or qualifications to the tag.
Elements are hierarchical, and may enclose content, which is **nested** between the **opening** and **closing** tag.

`<tag attribute="value">content example</tag>`

Every HTML file starts with the **doctype declaration** which tells your web browser what type of file to expect:

`<!DOCTYPE html>`

After the doctype, the first tag of every web page is the **root element** `<html>`.
The rest of the content is **nested** inside the root element, so the final tag on every HTML file will be `</html>`.

{% include alert.md text="Although HTML is technically a strict standard, web browsers are very lenient. They will display markup that breaks all the rules!" color="success" %}

## Write HTML

To create a web page we will use GitHub Pages free hosting service.
Any GitHub repository can create a static website and once activated will automatically appear in the github.io domain following the pattern: 

`https://username.github.io/repositoryname/`

So let's get started!
All the GitHub steps are below for reference, with the HTML examples following.

#### 1. Create a new repository on GitHub

- Click the plus sign in the upper right
- Select "New repository"
- Give your repo a unique name (no spaces or weird characters please!)
- Check "Initialize this repository with a README"
- Click the green "Create repository" button

#### 2. Activate GitHub Pages

- Click on the repository's *Settings* tab
- Scroll down to the *GitHub Pages* options
- Click *Source*, select *Master branch*, and click *Save*
- Wait for a minute for gh-pages to build. The live link will appear in the options

#### 3. Create a new file in the repo

- Click "Create new file" button on the repository page
- Type `index.html` in the name box
- Click into the editor
- Write some HTML! (see below)
- Scroll to the bottom, add a message, and click *Commit new file* (You just used Git!)

#### 4. Keep editing!

- Click on the file name on the repository page
- Click on pencil icon on the upper left of the file
- Edit stuff
- Scroll to the bottom, add a message, and click *Commit* (You just used Git again!)

#### Basic HTML 

We will start with an `index.html` file because by default the server provides index as the home page of your site.
Our basic page, introducing head, title, body, headings, and paragraphs:

```
<!DOCTYPE html>
<html>
    <head>
        <title>Hello World!</title>
    </head>
    <body>
        <h1>Hello World!</h1>
        <p>gh-pages is great.</p>
    </body>
</html>
```

#### Add Elements 

- comment, `<!-- not displayed -->`
- inline elements, `<strong>bold</strong>` and `<em>italic</em>`
- hyperlink, `<a href="about.html">About page</a>` (note: relative vs. absolute links)
- image, `<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0b/Cat_poster_1.jpg/640px-Cat_poster_1.jpg" alt="six different cats">`
- div, `<div><p>In a div?</p></div>` (don't have specific semantic meaning, but group elements together so are often used for layout)
- lists,

```
<ul>
    <li>cats</li>
    <li>dogs</li>
    <li>muffins</li>
</ul>

<ol>
    <li>cats</li>
    <li>dogs</li>
    <li>muffins</li>
</ol>
```

{% include alert.md text="Note: Indentation is a convention to make HTML code easier to read. It can help you quickly identify how the elements are nested. However, web browsers do not care! All extra white space and line breaks are ignored when rendering." color="info" %}

---------

# Resources 

- [w3schools](https://www.w3schools.com/) (good tutorials and reference with examples)
- [MDN web docs](https://developer.mozilla.org/en-US/) (higher level tutorials and reference)
- [HTML Living Standard](https://html.spec.whatwg.org/multipage/) (official open standard)

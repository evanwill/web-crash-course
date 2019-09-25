---
title: HTML
nav: true
---

## Hypertext Markup Language

HTML is a ["markup language"](https://en.wikipedia.org/wiki/Markup_language) originally designed to describe documents for the web.
HTML is made up of a set of standard **elements** used to structure a web page and introduce features such as images.
Elements are represented by **tags** using point brackets, `<tag></tag>`.

Every HTML file starts with the *doctype declaration* `<!DOCTYPE html>` which tells your web browser what type of file it is. 
Next comes the **root element** `<html>`. 
The rest of the web page is **nested** inside the root element, so the final tag on every HTML file will be `</html>`.

## Create a web page

Create a new repository on GitHub:

- Click the plus sign in the upper right
- Select "New repository"
- Give your repo a unique name (no spaces please!)
- Check "Initialize this repository with a README"
- Click green "Create repository" button

Create a new file in the repo:

- Click "Create new file" button on the repository page
- Type `index.html` in the name box
- Click into the editor
- Write some HTML!
- Scroll to the bottom, add a message, and click *Commit new file*. (You just used Git!)

Our basic page:

```
<!DOCTYPE html>
<html>
    <head>
        <title>Hello!</title>
    </head>
    <body>
        <h1>Hello World!</h1>
        <p>gh-pages rock!</p>
        <p>See <a href="about.html">About page</a></p>
    </body>
</html>
```

Activate GitHub Pages:

- Click on the repository's *Settings* tab.
- Scroll down to the *GitHub Pages* options.
- Click *Source*, select *Master branch*, and click *Save*. 
- Wait for a minute for gh-pages to build. The live link will appear in the options.

# Resources 

- [w3schools](https://www.w3schools.com/)

---
title: CSS
nav: true
---

# Cascading Style Sheets

HTML provides content marked up with the semantic structure of the document. 
CSS is a language that provides the means to style and control the *presentation* of this content in the web browser.
Importantly, this separation of content and presentation gives web pages great flexibility to fluidly adapt to different themes (dark mode), devices (phones), or mediums (print).

CSS is written as a **selector** that targets a specific element on web page and a **property** that sets style rules for that element.
Property values end with a semicolon and are surrounded by curly braces.

`selector { property: value; }`

CSS is **cascading** because the style of each element is calculated following a hierarchy of specificity of each rule that applies.
CSS properties can be written as **inline attributes**, **internal style tags**, or in **external files**.

#### Inline Style Attribute

The most basic way to add CSS to an element is using an attribute on the tag itself.
This is the most specific possible rule, so will over ride other CSS in Internal or External sources.

`<p style="color: red;">Red text</p>`

`<p style="text-align: right; color: green;">Right green text.</p>`

Inline styles are *much* hard to write, maintain, and update than centralizing your CSS, so should be avoided in most cases.

#### Style Tag

The `<style>` element can be added to the `<head>` of your HTML file to centralize CSS rules for the page.
First, we need **selectors** that will target the correct subset of elements.
Generally, we use **id** and **class** attributes or tag names.

First, add some id's and class's to your HTML file so we can test cascading selectors in action:

```
<p>Grey</p>
<p class="warning">Blue</p>
<p id="alert" class="blue">Blue</p>
```

Now in the `<head>` of your HTML add a `<style>` element:

```
<style>
    #alert { color: yellow; }
    .warning { color: blue; }
    p { color: grey; }
</style>
```

#### External CSS 

In practice most CSS is written into an external file that is loaded by the HTML document.
This allows you to create a central location for all the CSS rules that will style all the pages of your website, enabling a consistent and easy to maintain theme.

To load the external CSS, add a `<link>` element to the `<head>` of your HTML file.

`<link rel="stylesheet" href="main.css" type="text/css">`

This external file is often a standard framework created by someone else and may be hosted in a different location than your own site.
For example, the very popular [Bootstrap](https://getbootstrap.com/) on a content delivery network (CDN):

`<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">`

External style sheets loaded further down the HTML file will over ride ones loaded earlier.

#### Fonts 

To change the fonts of a website, we need to set the `font-family` using CSS *and* provide the appropriate font files, since we can not expect users to have the desired one installed on their system.

[Google Fonts](https://fonts.google.com/) is a commonly used service to simplify loading open fonts on your website.
Search or browse Google Fonts to select the desired font(s), then click the box at the bottom left to get the code.
First, add the new style sheet to the head:

`<link href="https://fonts.googleapis.com/css?family=Press+Start+2P&display=swap" rel="stylesheet">`

Then, add the font to your CSS:

`body { font-family: 'Press Start 2P', cursive; }`

-------------

# Resources 

- CSS [Specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity), [Inheritance](https://developer.mozilla.org/en-US/docs/Web/CSS/Inheritance), and [Cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/Cascade)
- [Bootstrap docs](https://getbootstrap.com/docs/) and [Bootstrap examples](https://getbootstrap.com/docs/4.3/examples/)
- [Get Started with Google Fonts](https://developers.google.com/fonts/docs/getting_started)
- [css-tricks](https://css-tricks.com/) (helpful blog)
- [CSS Standards](https://www.w3.org/Style/CSS/)

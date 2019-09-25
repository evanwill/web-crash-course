---
title: JS
nav: true
---

# JavaScript

JavaScript is a programming language originally designed for interacting with HTML in the web browser
(note: it is *not* related to [Java](https://go.java/index.html)).
JS has evolved into a powerful, multipurpose language that enables advanced interactivity and data processing on the **client-side**, i.e. in your web browser rather than on the server.

Similar to CSS, JS can be written inline, in a script tag, or in an external file.
Building on our previous `index.html` file, lets add some JS.

#### Inline JS Attributes

Add an input button with the JS "onclick" attribute:

`<button type="button" onclick="document.getElementById('alert').innerHTML = 'Changed!'">Inline JS</button>`

Adding JS inline is simple, but has the same draw backs as inline CSS, mixing HTML semantic content with the visual presentation.

#### Script Tag

JS contained in a `<script>` element will be executed in order as the HTML loads.
Unless they are critical to immediate presentation, scripts are often added towards the bottom of the HTML file to optimize load times.

Let's add another button:

`<button type="button" id="pop">Pop Up</button>`

Then attach a function using a script tag:

```
<script>
    /* set variables */
    var btn = document.getElementById('pop');
    var message = "Hello World!";
    /* create a function */
    function myAlert () {
        alert(message);
    }
    /* add event listener to element */
    btn.addEventListener("click", myAlert);
</script>
```

#### External Files

As with CSS, JS will often be contained in a separate file that is loaded by the HTML document. 
Add a `src` attribute to a script tag to load JS:

`<script src="example.js"></script>`

Often, this will be external libraries that simplify adding advanced features to your site.
For example, [jQuery]() or Bootstrap bundle:

```
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>
```

Now, with Bootstrap CSS and JS bundle being loaded on our HTML file, try adding a [Modal](https://getbootstrap.com/docs/4.3/components/modal/):

```
<!-- Button trigger modal -->
<button type="button" class="btn btn-primary" data-toggle="modal" data-target="#exampleModal">
  Launch demo modal
</button>

<!-- Modal -->
<div class="modal fade" id="exampleModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="exampleModalLabel">Hello World</h5>
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
      </div>
      <div class="modal-body">
        A Bootstrap Modal pop up!
      </div>
    </div>
  </div>
</div>
```

Notice that we didn't have to write any JS to add the Modal example. 
Bootstrap's library takes care of it all if you follow the mark up pattern (basically adding the `data-target` attribute).

{% include alert.md text="To debug JS, be sure to open your browser's dev tools and look at the **Console**. Any error messages will appear there! You can also use `console.log()` to send debug messages from your script." color="success" %}

------------

# Resources 

- [w3schools JS](https://www.w3schools.com/js/)
- [MDN JS learning pathways](https://developer.mozilla.org/en-US/docs/Learn/JavaScript)
- [The Modern JavaScript Tutorial](https://javascript.info/)

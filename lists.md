# Slice your content

The previous chapter showed how to use `data-simply-list` to build a main menu. This chapter will show some more uses for lists.

Lists are a very powerfull feature in SimplyEdit. By using lists well, your website will be easy to edit and look good.

There are many design elements that lend themselves to lists. We've already show how to build a menu using lists. But you can also use it to show a slideshow, show a portfolio or a list of employees. Or you can even use it to create modern responsive websites using 'content slices'.

A content slice is a horizontal section of your webpage, that has its own design and responsive behaviour. These slices can be re-used on many pages and you can use many and different slices on a single page.

SimplyEdit makes editing content slices easier than ever.

The following example uses a design with three different content slices: A full width hero image, a quote and a text slice with a title.

The HTML that came from your design looks someting like this:

```html
<body>
    <header>
        <div class="constrain-width">
            <h1>Page title</h1>
        </div>
    </header>
    <div class="slices">
        <div class="hero">
            <img src="hero.jpg" alt="">
        </div>
        <div class="quote">
            <div class="constrain-width">
                <blockquote>An inspirational quote</blockquote>
            </div>
        </div>
        <div class="text">
            <div class="constrain-width">
                <h2>A subtitle</h2>
                <p>And some text</p>
            </div>
        </div>
    </div>
```
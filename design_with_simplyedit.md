# Design with SimplyEdit

In the previous chapter you created a website and made it editable with SimplyEdit. This chapter will show how you can turn your own design into a SimplyEdit website.

The first step is to open the `index.html` file. You'll need to be familiar with how HTML works, but you don't need to write HTML by hand. You can use any tool you like and are comfortable with.

HTML works by inserting tags into your content. These tags tell the browser how to render the content. In addition tags can also have attributes. These are like meta-data, telling the browser extra stuff about the tag and the content.

SimplyEdit uses '*data attributes*' to make it work. It is your job as the designer to add these at the correct spot in the HTML.

Some examples:

```html
<h1 data-simply-field="title">This is a title</h1>
```

This tells SimplyEdit that the `<h1>` tag should have the content named `title`. The text "This is a title" is only a placeholder now. SimplyEdit will get the data for this page, retrieve the field with the name 'title' and overwrite the placeholder with the fields content.

So the `index.html` is now a *template* instead of the actual webpage.

```html
<body>
    <header>
        <h1 data-simply-field="Page Title">The title goes here</h1>
    </header>
    <div id="main" data-simply-field="Page Body">
        Your page content goes here.
    </div>
</body>
```

You are not limited to predefined names for the fields. You can use as many or few as you like and name them however you like. Just remember to follow the rules for attribute values in HTML:
- don't use quotes, use &amp;quot; if you must
- don't use &lt; or &gt;
- anything else is ok 

This is it. You are done. There is no programming, no need to register fields or create specific content types. You HTML is your template. Your template is all you need.

Go ahead, edit the page and reload it. You'll see that your content is safely stored and retrieved. If you want to take a peek under the hood, you can open the `data.json` file in a text editor and you'll see something like this:

```js
{
    "/" : {
        "Page Title": "Your page title.",
        "Page Body": "<p>Your page contents.</p>"
    }
}
```


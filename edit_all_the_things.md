# Edit all the things

SimplyEdit is more than just an HTML editor. It does not limit you to a single editable page field. Instead SimplyEdit allows anything to be editable. But only if you say it is.

This means you can create complex HTML structures to create responsive designs. And then you make only those parts that have content editable.

Now the person editing the page can forget about the complex HTML and just enter a few fields. There's nothing he or she can break, because those parts are not editable:

```html
<div class="caption light animated wow fadeInDown clearfix">
    <h1 data-simply-field="title">Simply edit the web</h1>
    <p data-simply-field="subtitle">It's easy now</p>
    <hr>
</div>
```

This example has two editable fields, a title and a subtitle. The editor understands the rules of HTML. This means that the title can only contain inline elements. There is no way to insert a paragraph, div or - god forbid - a table.

The worst that can happen is that someone inserts a line break (`<br>`). The `<hr>` tag is untouchable and the classes on the `<div>` as well.

## Images

Editable fields aren't limited to HTML elements that can contain text. You can make a single image editable as well:

```html
<img src="placeholder.jpg" alt="Alternate text"
     data-simply-field="A Picture" data-simply-selectable="true">
```

In addition to the `data-simply-field` attribute, you must also set the `data-simply-selectable` attribute. The image source and the `alt` and `title` attribute are now editable.

## Links

If you need a link or button to always be there and look the same, but the target may change, you can create an editable anchor or hyperlink:

```html
<a href="link.html" class="button" title="A title"
   data-simply-field="The button">Placeholder</a>
```

The `href`, `title`, `name` attributes and the text content are editable. You can also set the `nofollow` attribute.

Again, the classes on the anchor are fixed in the design. These cannot be changed. The text content is limited to inline styles only. You can fool around with bold, italic and underline. But you can't insert a `<h1>`.

## Icons


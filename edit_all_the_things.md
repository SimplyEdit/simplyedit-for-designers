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



## Links

## Icons


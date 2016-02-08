# Working with dynamic content

If your websites look anything like ours, you're working with lots of javascript modules. These animate or update the content of the page with regularity. 

This can lead to problems when you want to edit the page. Its difficult to edit something that won't sit still.

SimplyEdit provides a few tools to help you out.

##data-simply-hidden

This attribute does one thing only: It tells the editor to hide its element when in edit mode. This is especially useful for hovering elements that get in the way of editable items.

##body[data-simply-edit]

The editor helpfully sets an attribute on the body tag whenever it is in edit mode. This means you can apply CSS only when the editor is in use.

##fixing the culprits
Some javascript components rearrange the dom willy-nilly. Especially image sliders can't keep their fingers of your content. Copying elements around, adding parent elements, etc.

Unfortunately there is no single cure for all components. The way in which they manipulate the html is too varied. But they often provide configuration options that limit this behaviour.

An example is [bxSlider](http://bxslider.com/). To make seamless loops, it will copy all slides once. This is relatively benign, but it sometimes makes editing a slide difficult. You can prevent this though:

```javascript
$("body[data-simply-edit] .js-slider").bxSlider({
    infiniteLoop: false
});
```

This disables the copying - and the looping - in editmode.

Some components are more difficult to fix and need more programming. You can read more about those in the developers manual.
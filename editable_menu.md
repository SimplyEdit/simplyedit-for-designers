# An editable menu

The previous chapter showed how to create your own design and make it editable. This chapter expands on that and shows how to make your site's menu editable as well.

Most navigation menu's look something like this, in HTML:

```html
<nav>
    <ul class="nav">
        <li>
            <a href="/index.html">Home</a>
        </li>
        <li>
            <a href="/page2.html">Page 2</a>
        </li>
    </ul>
</nav>
```

Using the same trick as in the previous chapter would turn this into:

```html
<nav>
    <ul class="nav">
        <li>
            <a href="/index.html" data-simply-field="menu1">Home</a>
        </li>
        <li>
            <a href="/page2.html" data-simply-field="menu2">Page 2</a>
        </li>
    </ul>
</nav>
```

This will work, but there is a problem: You can't remove a menu item, or add a new one. You can only change the menu items that are there.

So instead, we'll use a new trick: `data-simply-list`.

```html
<nav>
    <ul class="nav" data-simply-list="Main Menu">
        <template>
            <li>
                <a href="/index.html" data-simply-field="item">Menu item</a>
            </li>
        </template>
    </ul>
</nav>
```

The `data-simply-list` attribute tells SimplyEdit that the contents are a list of things. But SimplyEdit doesn't know what is in these things, unless you tell it. This is where the `<template>` comes in. 

SimplyEdit sees the template tag, and takes its contents and applies it to each element in the list. Just as if each element was a seperate page.

So you can use a `data-simply-field` inside a list template, just like on any other tag in the page.

If the list is empty, nothing is shown. Only when you are editing the page, you'll see a message like this in the place of the empty list:

![(Empty list)](emptylist.png)

If you click or touch it, a toolbar will appear:

![(Empty list - Add)](emptylist-add.png)

Now press the add button and you will see 'Menu item' appear and the (Empty list) message disappears.

In addition you'll see an icon above and to the left of the new menu item, like this:

![(List item)](listitem.png)

It will appear almost transparent untill you hover the mouse over the menu item, or touch it. If you press the icon, you get a new toolbar like this:

![(List item - Toolbar)](listitem-toolbar.png)

Pressing 'Add' inserts a new menu item, pressing 'Delete' removes it again. You now have a way to create as many menu items as you like, and remove them again later.

If you save the page, the `data.json` file will contain something like this:

```js
{
    "/index.html" : {
        "Page Title": "Your page title.",
        "Page Body": "<p>Your page contents.</p>",
        "Main Menu": [
            {
                "item": {
                    "href": "/index.html",
                    "contents": "Menu item 1"
                }
            }
            {
                "item": {
                    "href": "/page2.html",
                    "contents": "Menu item 2"
                }
            }
        ]
    }
}
```

SimplyEdit knows that "Main Menu" is a list. Because of the `<template>`, it also knows that each element of the list has a field called `item` and that this field is an anchor tag. So SimplyEdit stores the `href` attribute and the contents of each item as well.


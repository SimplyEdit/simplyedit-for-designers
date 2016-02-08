# Listception

Yes. Yes, you can put lists inside your lists. And lists inside those lists. There's probably a point where its no longer useful or fun, but SimplyEdit doesn't mind.

## Pulldown menu's

```html
<nav class="navbar navbar-default" role="navigation">
    <ul class="nav" data-simply-list="menu" 
    data-simply-sortable data-simply-path="/">
        <template data-simply-template="Submenu">
            <li class="submenu">
                <a data-simply-field="link" href="#">about</a>
                <ul class="submenu" data-simply-list="submenu"
                    data-simply-sortable>
                    <template>
                        <li>
                            <a data-simply-field="link"
                            href="#">bio</a>
                        </li>
                    </template>
                </ul>
            </li>
        </template>
        <template data-simply-template="Item">
            <li>
                <a data-simply-field="link" href="#">music</a>
            </li>
        </template>
    </ul>
</nav>
```

This allows you to make a menubar with optional pulldown submenu's. For a third level, just repeat the same trick in the `ul.submenu`.

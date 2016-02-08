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


## Cards in a content slice

```html
<div data-simply-list="sections" data-simply-sortable>
    ...
    <template data-simply-template="highlights">
		<div class="highlights">
			<ul data-simply-list="highlights" 
			data-simply-sortable>
				<template>
					<li>
						<i class="fa icon" data-simply-field="icon"></i>
						<h2 data-simply-field="title">Benefit 1</h2>
						<div data-simply-field="description">A description</div>
					</li>
				</template>
			</ul>
		</div>
	</template>
	...
</div>
```

This is a slightly shortened snippet from the SimplyEdit.io website itself. The highlights template is a content slice that can be placed anywhere within the sections list. Each slice is the full width of the page.

Within the highlights slice is another list, called highlights as well. Here you can add a highlight card.
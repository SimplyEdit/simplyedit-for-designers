# I want my tables back

SimplyEdit does not allow you to insert tables. That is not a bug, its a feature!

Tables and responsive websites don't mix well. There are some solutions out there, but they are all less than stellar.

Tables and WYSIWYG editors don't mix well. Again, some editors have better support than others. Most just frustrate their users.

Tables and accessibility don't mix well. Actually, they can. Its just that nobody bothers to do it.

We stopped trying to shoehorn table support into SimplyEdit and make it, well... not simple anymore. Instead we've turned to lists again, e.g:

```html
<table>
<caption>My Todo List</caption>
<thead>
    <tr>
        <th scope="col">Todo</th>
        <th scope="col">Due</th>
    <tr>
</thead>
<tbody>
    <tr>
        <td>Polish shoes</td>
        <td>Today</td>
    </tr>
</tbody>
</table>
```

To make this table editable, while keeping it accessible, we turn the body into a list!

```html
<table>
<caption data-simply-field="caption">My Todo List</caption>
<thead>
    <tr>
        <th scope="col">Todo</th>
        <th scope="col">Due</th>
    <tr>
</thead>
<tbody data-simply-list="rows">
    <template>
        <tr>
            <td data-simply-field="todo">Polish shoes</td>
            <td data-simply-field="due">Today</td>
        </tr>
    </template>
</tbody>
</table>
```

Now you can add, change and remove rows of the table. The table design won't be broken, you can't change the row-span or col-span. You can't remove the column headings or the scope attributes on them. 

Simply design the tables you need for the website you're working on and use these where needed. The table will fit perfectly with your design allways.



# WesBos | CSS Grid #

This the notes to follow along with the CSS grid course by WesBos.

## Grid Fundamental ##

* Grid is a way to divide elements inside a root container into rows and container.

```html
<div class="container">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
</div>
```

* The above HTML creates a `div` called container with multiple item `div` as its immediate child.

* The `.container` can act as a grid, and `.item` inside as the grid elements

```css
.container {
      display: grid;
      grid-template-columns: 100px 100px 100px;
      grid-gap: 20px;
    }
```

* The above CSS, makes the `.container` as a grid by just saying `display: grid`.

* The `grid-template-columns: 100px 100px 100px` divides all the `.item` into 3 columns of `100px` width.

* `grid-gap: 20px` creates a gap, between each item.

```css
.container {
      display: grid;
      grid-template-rows: 100px 100px 100px;
      grid-gap: 20px;
    }
```

* `grid-template-rows: 100px 100px 100px` : changes the item into rows, with 1 column width, since this is the default column width.

```css
.container {
      display: grid;
      grid-template-columns: auto auto auto;
      grid-template-rows: 100px 100px 100px;
      grid-gap: 20px;
    }
```

* We can use both `grid-template-columns` and `grid-template-rows`, to create an actual grid, defining 3 rows and 3 columns, and remaining elements will be implicit grid.

* We have used `auto` to automatically expand as per the total width of the browser, bringing the benefits of responsiveness immediately. 

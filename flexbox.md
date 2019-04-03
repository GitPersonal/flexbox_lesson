# Flexbox

## Level 1 — Basic

---

1. Creating a flex container

to create a flex container, you just need to add the
`display:flex;` property to an element.
By default, all direct children are considered flex items and are laid out horizontally in a single row from left to right. If the total width of the flex items is larger than the container, the items will be scaled down so that they will fit into the container.

```html
<div class="flex-container">
  <div class="flex-item"></div>
  <div class="flex-item"></div>
</div>
```

```css
.flex-container {
  display: flex;
}
```

---

---

2. Put flex items in a single column

```css
.flex-container {
  display: flex;
  flex-direction: column;
}
```

Flex items can be laid out vertically by setting flex-direction: column.

It is also possible to lay them out in reverse order by setting

`flex-direction: column-reverse` or `flex-direction: row-reverse`.

```css
.flex-container {
  display: flex;
  flex-direction: column-reverse;
}
```

## Level 2 — Beginner

---

1. Align flex items to the right

```css
.flex-container {
  display: flex;
  justify-content: flex-end;
}
```

Recall that there is flex direction for every Flexbox model. `justify-content` is used to specify where the flex items should be placed along the flex direction. In the example above, `justify-content: flex-end` means items are justified to the end of the flex container in the horizontal direction. That’s why they are placed to the right.

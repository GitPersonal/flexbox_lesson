# Flexbox

## Level 1 — Basic

---

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

---

1. Align flex items to the right

```css
.flex-container {
  display: flex;
  justify-content: flex-end;
}
```

Recall that there is flex direction for every Flexbox model. `justify-content` is used to specify where the flex items should be placed along the flex direction. In the example above, `justify-content: flex-end` means items are justified to the end of the flex container in the horizontal direction. That’s why they are placed to the right.

---

2. Center-align flex items

```css
.flex-container {
  display: flex;
  justify-content: center;
}
```

---

3. Spread out flex items

You can specify how much space should appear between items in a container by using one of three possible spacing values for the `justify-content` property:

- `space-evenly:` the space between the starting edge of the container and the first item is equal to the spacing between each item and the item adjacent to it.

- `space-between:` the space between any two adjacent items is the same, but not necessarily equal to the space between the first/last item and its closest edge; the space between the start edge and the first item is equal to the space between the end edge and the last item.

- `space-around:` the space on each side of an item is the same for each item in the container. Note that the this means the space between two adjacent items will be twice as large as the space between the first/last item and its closest edge.

---

4. Align flex items in a second direction

Usually, we would like to lay out items along the flex direction while also aligning the items in the direction perpendicular to it. By setting `justify-content: center` and `align-items: center`, flex items can be placed at the center of flex container both `horizontally` and `vertically`.

---

5. Align a particular flex item

```css
.flex-container {
  display: flex;
  align-items: center;
}
.flex-bottom {
  align-self: flex-end;
}
```

It is possible to align a particular flex item differently than the others in the container by using the `align-self` CSS property on that item.

## Level 3 — Intermediate

---

---

1. Allow flex items to wrap into other rows/columns

```css
.flex-container {
  display: flex;
  flex-wrap: wrap;
}
```

By default, flex items are not allowed to wrap and they are resized to fit into a single row or column if flex container is not large enough for all of them. By adding `flex-wrap: wrap`, flex items that would overflow the container will be wrapped into another row.

---

2.  Reverse wrapping

```css
.flex-container {
  display: flex;
  flex-wrap: wrap-reverse;
}
```

Flex items are still laid out in multiple rows `flex-wrap: wrap-reverse` but they start from the end of flex container.

---

3.Justify position of lines of elements

```css
.flex-container {
  display: flex;
  flex-wrap: wrap;
  align-content: flex-start;
}
```

By default, rows of flex items that wrapped are stretched to take up all remaining space with equal spacing between adjacent rows. You can set align-content on the flex container to determine the positioning of rows when wrapping occurs. Possible values are `flex-start`, `flex-end`, `center`, `space-between`, `space-around` and `stretch(default)`.

## Level 4 — Advanced

---

---

1. Expand elements

```css
.flex-container {
  display: flex;
}
.flex-item.nth-of-type(1) {
  flex-grow: 1;
}
.flex-item.nth-of-type(2) {
  flex-grow: 2;
}
```

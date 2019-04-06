# Flexbox

# CSS Flexbox

## Flexbox Elements

To start using the Flexbox model, you need to first define a flex container.

```html
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div>
```

---

## Parent Element (Container)

The flex container becomes flexible by setting the display property to flex:

```css
.flex-container {
  display: flex;
}
```

The flex container properties are:

- flex-direction
- flex-wrap
- flex-flow
- justify-content
- align-items
- align-content

---

## The flex-direction Property

The `flex-direction` property defines in which direction the container wants to stack the flex items.

![Alt Text](images/column.png)

The **`column`** value stacks the flex items vertically (from top to bottom):

```css
.flex-container {
  display: flex;
  flex-direction: column;
}
```

---

![Alt Text](images/column-reverse.png)
The `column-reverse` value stacks the flex items vertically (but from bottom to top):

```css
.flex-container {
  display: flex;
  flex-direction: column-reverse;
}
```

---

![Alt Text](images/row.png)
The row value stacks the flex items horizontally (from left to right):

```css
.flex-container {
  display: flex;
  flex-direction: row;
}
```

---

![Alt Text](images/row-reverse.png)
The row-reverse value stacks the flex items horizontally (but from right to left):

```css
.flex-container {
  display: flex;
  flex-direction: row-reverse;
}
```

---

## The flex-wrap Property

The `flex-wrap` property specifies whether the flex items should wrap or not.

The examples below have 12 flex items, to better demonstrate the `flex-wrap` property.

![Alt Text](images/flex-wrap.png)

The wrap value specifies that the flex items will wrap if necessary:

```css
.flex-container {
  display: flex;
  flex-wrap: wrap;
}
```

The nowrap value specifies that the flex items will not wrap (this is default):

```css
.flex-container {
  display: flex;
  flex-wrap: nowrap;
}
```

The wrap-reverse value specifies that the flexible items will wrap if necessary, in reverse order:

```css
.flex-container {
  display: flex;
  flex-wrap: wrap-reverse;
}
```

---

## The flex-flow Property

The `flex-flow` property is a shorthand property for setting both the `flex-direction` and `flex-wrap` properties.

```css
.flex-container {
  display: flex;
  flex-flow: row wrap;
}
```

---

## The justify-content Property

The `justify-content` property is used to align the flex items:

![justify-content](images/justify-content.png)

The center value aligns the flex items at the center of the container:

```css
.flex-container {
  display: flex;
  justify-content: center;
}
```

The flex-start value aligns the flex items at the beginning of the container (this is default):

```css
.flex-container {
  display: flex;
  justify-content: flex-start;
}
```

The flex-end value aligns the flex items at the end of the container:

```css
.flex-container {
  display: flex;
  justify-content: flex-end;
}
```

The space-around value displays the flex items with space before, between, and after the lines:

```css
.flex-container {
  display: flex;
  justify-content: space-around;
}
```

The _space-between_ value displays the flex items with space between the lines:

```css
.flex-container {
  display: flex;
  justify-content: space-between;
}
```

---

## The align-items Property

The `align-items` property is used to align the flex items vertically.

![justify-content](images/align-items.png)

In these examples we use a 200 pixels high container, to better demonstrate the `align-items` property.

The _center_ value aligns the flex items in the middle of the container:

```css
.flex-container {
  display: flex;
  height: 200px;
  align-items: center;
}
```

The _flex-start_ value aligns the flex items at the top of the container:

```css
.flex-container {
  display: flex;
  height: 200px;
  align-items: flex-start;
}
```

The _flex-end_ value aligns the flex items at the bottom of the container:

```css
.flex-container {
  display: flex;
  height: 200px;
  align-items: flex-end;
}
```

The stretch value stretches the flex items to fill the container (this is default):

```css
.flex-container {
  display: flex;
  height: 200px;
  align-items: stretch;
}
```

The _baseline_ value aligns the flex items such as their baselines aligns:

```css
.flex-container {
  display: flex;
  height: 200px;
  align-items: baseline;
}
```

**Note:** the example uses different font-size to demonstrate that the items gets aligned by the text baseline:
![justify-content](images/baseline.png)

---

---

---

## The align-content Property

The `align-content` property is used to align the flex lines.

![justify-content](images/align-content.png)

In these examples we use a 600 pixels high container, with the flex-wrap property set to wrap, to better demonstrate the `align-content` property.

The _space-between_ value displays the flex lines with equal space between them:

```css
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: space-between;
}
```

The *space-aroun*d value displays the flex lines with space before, between, and after them:

```css
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: space-around;
}
```

The _stretch_ value stretches the flex lines to take up the remaining space (this is default):

```css
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: stretch;
}
```

The center value displays display the flex lines in the middle of the container:

```css
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: center;
}
```

The `flex-start` value displays the flex lines at the start of the container:

```css
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: flex-start;
}
```

The _flex-end_ value displays the flex lines at the end of the container:

```css
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: flex-end;
}
```

---

---

## Perfect Centering

In the following example we will solve a very common style problem: perfect centering.

![justify-content](images/perfect-centering.png)

**SOLUTION:** Set both the `justify-content` and align-items properties to _center_, and the flex item will be perfectly centered:

```css
.flex-container {
  display: flex;
  height: 300px;
  justify-content: center;
  align-items: center;
}
```

---

---

---

## Child Elements (Items)

The direct child elements of a flex container automatically becomes flexible (flex) items.

![justify-content](images/child-elements-items.png)

```html
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div>3</div>
  <div>4</div>
</div>
```

### The flex item properties are:

- order
- flex-grow
- flex-shrink
- flex-basis
- flex
- align-self

---

## The order Property

The `order` property specifies the order of the flex items.
![justify-content](images/order.png)

The first flex item in the code does not have to appear as the first item in the layout.

The order value must be a number, default value is 0.

The order property can change the order of the flex items:

```html
<div class="flex-container">
  <div style="order: 3">1</div>
  <div style="order: 2">2</div>
  <div style="order: 4">3</div>
  <div style="order: 1">4</div>
</div>
```

---

## The flex-grow Property

The `flex-grow` property specifies how much a flex item will grow relative to the rest of the flex items.

![justify-content](images/flex-grow.png)

The value must be a number, default value is 0.

Make the third flex item grow eight times faster than the other flex items:

```html
<div class="flex-container">
  <div style="flex-grow: 1">1</div>
  <div style="flex-grow: 1">2</div>
  <div style="flex-grow: 8">3</div>
</div>
```

---

## The flex-shrink Property

The `flex-shrink` property specifies how much a flex item will shrink relative to the rest of the flex items.

![justify-content](images/flex-shrink.png)

The value must be a number, default value is 1.

Do not let the third flex item shrink as much as the other flex items:

```html
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div style="flex-shrink: 0">3</div>
  <div>4</div>
  <div>5</div>
  <div>6</div>
  <div>7</div>
  <div>8</div>
  <div>9</div>
  <div>10</div>
</div>
```

---

## The flex-basis Property

The `flex-basis` property specifies the initial length of a flex item.

![justify-content](images/flex-basis.png)

Set the initial length of the third flex item to 200 pixels:

```html
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div style="flex-basis: 200px">3</div>
  <div>4</div>
</div>
```

---

## The flex Property

The `flex` property is a shorthand property for the `flex-grow`, `flex-shrink`, and `flex-basis` properties.

Make the third flex item not growable (0), not shrinkable (0), and with an initial length of 200 pixels

```html
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div style="flex: 0 0 200px">3</div>
  <div>4</div>
</div>
```

---

## The align-self Property

The `align-self` property specifies the alignment for the selected item inside the flexible container.

The `align-self` property overrides the default alignment set by the container's `align-items` property.

![justify-content](images/align-self.png)

In these examples we use a 200 pixels high container, to better demonstrate the align-self property:

Align the third flex item in the middle of the container:

```html
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div style="align-self: center">3</div>
  <div>4</div>
</div>
```

Align the second flex item at the top of the container, and the third flex item at the bottom of the container:

```html
<div class="flex-container">
  <div>1</div>
  <div style="align-self: flex-start">2</div>
  <div style="align-self: flex-end">3</div>
  <div>4</div>
</div>
```

---

## CSS Flexbox Properties

The following table lists the CSS properties used with flexbox:

| Property        | Description                                                                                                                             |
| :-------------- | :-------------------------------------------------------------------------------------------------------------------------------------- |
| display         | Specifies the type of box used for an HTML element                                                                                      |
| flex-direction  | Specifies the direction of the flexible items inside a flex container                                                                   |
| justify-content | Horizontally aligns the flex items when the items do not use all available space on the main-axis                                       |
| align-items     | Vertically aligns the flex items when the items do not use all available space on the cross-axis                                        |
| flex-wrap       | Specifies whether the flex items should wrap or not, if there is not enough room for them on one flex line                              |
| align-content   | Modifies the behavior of the flex-wrap property. It is similar to align-items, but instead of aligning flex items, it aligns flex lines |
| flex-flow       | A shorthand property for flex-direction and flex-wrap                                                                                   |
| order           | Specifies the order of a flexible item relative to the rest of the flex items inside the same container                                 |
| align-self      | Used on flex items. Overrides the container's align-items property                                                                      |
| flex            | A shorthand property for the flex-grow, flex-shrink, and the flex-basis properties                                                      |

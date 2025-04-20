# 🧑‍🎨 CSS Basics – Quick Reference

This README covers the foundational ways to include CSS in a webpage and common selectors for targeting elements.

---

## 🎨 3 Ways To Include CSS

### ✅ Internal CSS

CSS is written inside a `<style>` tag within the `<head>` of an HTML file.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      p {
        color: blue;
      }
    </style>
  </head>
  <body>
    <p>This is a blue paragraph using internal CSS.</p>
  </body>
</html>
```

---

### ✅ Inline CSS

CSS is applied directly to HTML elements using the `style` attribute.

```html
<p style="color: blue;">This is a blue paragraph using inline CSS.</p>
```

---

### ✅ External CSS

CSS is written in a separate file and linked to the HTML file.

**index.html**

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <p>This is a blue paragraph using external CSS.</p>
  </body>
</html>
```

**style.css**

```css
p {
  color: blue;
}
```

---

## 🧩 CSS Selectors

### 🔹 Class Selector

Targets elements with a specific class name.

```css
.myClass {
  color: green;
}
```

```html
<p class="myClass">This text is green using a class selector.</p>
```

---

### 🔸 ID Selector

Targets a unique element with a specific ID.

```css
#myId {
  font-size: 20px;
}
```

```html
<p id="myId">This text uses an ID selector.</p>
```

---

### 👶 Child Selector (`>`)

Targets **direct child** elements only.

```css
div > p {
  color: red;
}
```

```html
<div>
  <p>This paragraph is a direct child and will be red.</p>
  <section>
    <p>This paragraph is not a direct child and won't be red.</p>
  </section>
</div>
```

---

### 🌳 Descendant Selector (space)

Targets **all nested** elements inside a parent, regardless of depth.

```css
div p {
  color: orange;
}
```

```html
<div>
  <p>This paragraph is orange.</p>
  <section>
    <p>This nested paragraph is also orange.</p>
  </section>
</div>
```

---

### 🌐 Universal Selector (`*`)

Applies styles to **all elements** on the page.

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

---

## 🎭 Pseudo Selectors

Used to define special states or parts of elements.

```css
/* Style when mouse hovers over link */
a:hover {
  color: red;
}

/* Style the first paragraph inside an element */
p:first-child {
  font-weight: bold;
}

/* Style visited links */
a:visited {
  color: purple;
}

/* Style input fields when focused */
input:focus {
  border-color: blue;
}
```

---

# 📦 CSS Box Model & Typography – Quick Reference

This section includes the CSS Box Model and important typography-related properties in CSS.

---

## 📦 CSS Box Model

The Box Model describes how every HTML element is represented as a rectangular box.

### 📊 Diagram of Box Model

```
+---------------------------+
|        Margin             |
|  +---------------------+  |
|  |      Border         |  |
|  |  +---------------+  |  |
|  |  |   Padding     |  |  |
|  |  |  +---------+  |  |  |
|  |  |  | Content |  |  |  |
|  |  |  +---------+  |  |  |
|  |  +---------------+  |  |
|  +---------------------+  |
+---------------------------+
```

---

## 🔠 Fonts in CSS

### Font Style

```css
font-style: italic; /* Text leans to the right */
font-style: normal; /* Default style */
font-style: oblique; /* Similar to italic with less tilt */
```

---

### Font Weight

```css
font-weight: normal; /* Default */
font-weight: bold; /* Bold text */
font-weight: 100 - 900; /* Numeric values for precision */
```

---

### Font Family

```css
font-family: 'Arial', sans-serif;
font-family: 'Times New Roman', serif;
```

---

## ✍️ Text Decoration

```css
text-decoration: overline; /* Line above the text */
text-decoration: underline; /* Line below the text */
text-decoration: line-through; /* Line through the text */
text-decoration: none; /* No decoration */
```

---

## 📐 Text Alignment

```css
text-align: left; /* Align to the left */
text-align: center; /* Align to the center */
text-align: right; /* Align to the right */
text-align: justify; /* Justify text across the line */
```

### 📊 Example

```
Left:     This is text
Center:      This is text
Right:           This is text
Justify: This   is   spaced   out   text
```

---

## 🔤 Text Transformation

```css
text-transform: uppercase; /* ALL CAPS */
text-transform: lowercase; /* all lowercase */
text-transform: capitalize; /* First Letter Capitalized */
text-transform: none; /* No transformation */
```

### 📊 Example

```
UPPERCASE -> HELLO WORLD
lowercase -> hello world
Capitalize -> Hello World
None -> Hello world
```

---

## ✨ Additional Typography Properties

### Letter Spacing

```css
letter-spacing: 2px;
```

### Example

```
Text: H  E  L  L  O
```

---

### Line Height

```css
line-height: 1.6;
```

### Example

```
Line 1: Hello

Line 2: World  <- More space between lines
```

---

### Text Shadow

```css
text-shadow: 2px 2px 5px gray;
```

(Visual effect can't be shown in )

---

### Text Overflow

```css
text-overflow: ellipsis;
text-overflow: clip;
overflow: hidden;
white-space: nowrap;
```

### 📊 Example

```
Ellipsis: This is a long text...
Clip:     This is a long text
```

---

!Important > Inline Style > ID Selector > Class or Attribute Selector > Element Selector > Universal Selector

<!-- CSS Units -->
px 
em
rem
vh
vw
vmin 
vmax
%


# 🧮 CSS Specificity & Units – Quick Reference

This section includes the **specificity hierarchy** in CSS and the **various units** used for measurements and sizing.

---

## 📊 CSS Specificity Hierarchy

When multiple CSS rules apply to the same element, the browser uses specificity to decide which one to apply. The order of precedence (from highest to lowest) is:

```
!important > Inline Style > ID Selector > Class/Attribute Selector > Element Selector > Universal Selector
```



---

## 📏 CSS Units

CSS uses various units to measure length, spacing, and sizes. They can be either **absolute** or **relative**.

### 🔹 Absolute Unit

- `px` – Pixels: Fixed unit, not responsive.

```css
font-size: 16px;
```

---

### 🔸 Relative Units

- `em` – Relative to the **font-size of the parent**.

```css
font-size: 2em; /* 2x parent size */
```

- `rem` – Relative to the **root element's font-size** (`html` tag).

```css
font-size: 1.5rem;
```

- `%` – Relative to the **parent element**.

```css
width: 50%; /* half the width of the parent */
```

- `vh` – Relative to **1% of the viewport height**.

```css
height: 50vh; /* 50% of the viewport height */
```

- `vw` – Relative to **1% of the viewport width**.

```css
width: 100vw; /* Full width of the viewport */
```

- `vmin` – Relative to the **smaller dimension** (height or width) of the viewport.

```css
font-size: 10vmin;
```

- `vmax` – Relative to the **larger dimension** of the viewport.

```css
padding: 5vmax;
```

---

> 🧠 Use relative units for responsive designs and `!important` sparingly to avoid specificity issues.



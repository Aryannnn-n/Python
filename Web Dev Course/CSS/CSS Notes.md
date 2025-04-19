
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
    <link rel="stylesheet" href="style.css">
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

<!-- Css Box Model  -->
Margin
Border
Padding 
Main Content

<!-- Fonts In CSS -->

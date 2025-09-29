## Agenda

- Precedence
- Specificity
- Inheritance
- The Cascade
- Browser Dev Tools

---

## Why this talk?

- CSS has a steep learning curve but is hard to master
- "Trial and error" often leads to frustration and bugs
- Understanding the fundamentals is key for large projects
- Become a more productive and confident frontend dev

---

## CSS is messy, isn't it?

![Frustrated CSS programming animated gif](../images/giphy.gif)

---

# Precedence

---

## What is Precedence?

- What happens if multiple CSS rules target the same element with the same properties?
- CSS precedence determines which styles are ultimately applied by the browser
- It's the process of resolving conflicting CSS declarations

---

## Precedence by Example

- See live: [CodePen](https://codepen.io/doppelmutzi/pen/yWLbbL)
- Examples help to understand the concept
```html
<h2 class="subline">subline</h2>
<aside>
  <h2>sidebar title</h2>
</aside>
```
```css
/* some styles target h2 elements */
.subline {
  font-family: serif;
}
h2 {
  font-family: sans-serif;
}
aside {
  color: red;
}
```

---

## Precedence by Example (2)

- The `subline` element has a **black serif** font.
- The `sidebar title` has a **red sans-serif** font.
- Why?
    - The `.subline` selector is more **specific** than the `h2` selector.
    - The `color: red` from the `aside` element is **inherited** by the `h2`.

---

## Key Concepts

- The **precedence algorithm** for determining the final CSS styles involves three core concepts:
    - Specificity
    - Inheritance
    - The Cascade

# CSS Structure

---

## CSS Cascade

The cascade is the algorithm that defines which CSS rules are being applied when there are
conflicting rules.

When styling an element the browser:

1. Searches for all rules with matching selectors
2. Sorts the rules by their importance taking into account:
   - Whether the declaration is followed by **!important**
   - The rule's origin (Browser stylesheet, User stylesheet, Author stylesheet)
3. Sorts rules by their [specificity](#specificity), if there are multiple rules with the same
   importance according to no. 2.
4. Chooses the last declaration over previous ones, if there are multiple rules with the same
   importance and the same specificity.

---

## Specificity

The specificity of a CSS selector tells the browser which rule is most relevant for an element. The
more specific rules win over less specific ones.

You can find a list of the specificity of different selectors on
[specifishity.com](https://specifishity.com/).

The **universal selector** is the lease specific one. It is overwritten by any other CSS rule with
any other matching CSS selector.

**type selectors** like `div` have a low specificity and can easily be overwritten.

**class selectors** like `.bright` and **attribute selectors** like `[type=checkbox]` have a higher
specificity.

---

## CSS Structure best practices

- keep your CSS consistent throughout a project. In collaborative projects, there are often coding
  style guidelines.
- separate global and local styles into different files (or sections of files)
- create multiple stylesheets for different parts of your application
  - structure your code by thinking in reusable **components**. You can write your CSS for every
    component in its own CSS file.

---

### How to import one stylesheet or multiple stylesheets into another stylesheet

You can import one stylesheet into another stylesheet using **@import**:

```css
@import "customer-card.css";
```

---

## CSS practical strategies

There is no single strategy to approach HTML and CSS cooperation, since it mostly depends on the website / application size and target.

Here we present some concrete scenarios.

---

### Highlight a product in offer

### Preventing unwanted cascading

---

### BEM

Among the various naming conventions, a popular one is [BEM][Introduction to BEM]. It suggests the concept of blocks, elements and modifiers like:

- the `<article>` is a **block**;
- the `<h2>` and `<span>` are **elements** contained in the block, and are named like `{block}__{elementName}`;
- the second `<article>` is displayed in a different way thanks to the `product--in-offer` modifier class, that is named like `{block}--{modifierName}`.

You are not required to use BEM, but you may encounter it in some challenges or examples.

---

### Kebab Case naming convention

The kebab case naming convention defines to use hyphens to separate words in variables. Many
developers use the kebab case convention to write css classes. In BEM we also use kebab case.

---

## Custom properties (CSS variables)

You can store values in custom properties, so you can use them again multiple times without having
to write the value.

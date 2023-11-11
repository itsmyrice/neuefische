# HTML BASICS

---

## HTML (Hyper Text Markup Language) 

- is used to express text in a structured way. HTML tags indicate what kind of element is displayed on the website.

---

## HTML tag attributes

- Some elements require some more information in order to work properly. This information is specified via attributes

---

## Layout of an HTML file

Every HTML document starts with a
[doctype](https://developer.mozilla.org/en-US/docs/Glossary/Doctype) followed by the `<html>`
element, which consists of two main parts:

- The `<head>` contains important meta information for the browser like
  - the charset (utf-8)
  - the favicon displayed in the tab
  - the title of the website
  - CSS and JavaScript files needed for the website
- The `<body>` contains the visible content of the website structured by html elements

---

## List of common HTML elements

| element             | meaning                                                      |
| ------------------- | ------------------------------------------------------------ |
| `<head></head>`     | only once per website, includes meta data and linked files   |
| `<body></body>`     | only once per website, includes the html website content     |
| `<h1></h1>`         | only once per website, a level one heading                   |
| `<h2></h2>`         | a level two heading                                          |
| `<p></p>`           | a paragraph                                                  |
| `<a></a>`           | an anchor (link)                                             |
| `<img>`             | an image (self-closing / empty)                              |
| `<form></form>`     | a form element                                               |
| `<input>`           | an input field (self-closing / empty)                        |
| `<button></button>` | a clickable element equipped with some kind of functionality |

---

## Structuring a Website

Developers have two main tools to express a meaningful structure in a website:

1.  Using semantic HTML elements
2.  Nesting / grouping of HTML elements

---

### Semantic HTML

Semantic HTML elements not only divide the content of the web page into distinct parts, but also
describe the function or purpose of the elements. This has two major benefits:

- The HTML becomes more understandable for other developers
- Accessibility tools and search engines can interpret the website

Therefore, one should use semantic HTML elements whenever possible.

### List of Semantic HTML elements

| element                 | meaning                                                                                                             |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `<main></main>`         | only once per website, includes the main content of the page                                                        |
| `<section></section>`   | a generic standalone section of a document                                                                          |
| `<ul></ul>`/`<ol></ol>` | a list of elements with the same structure, only has `<li>` elements as direct children                             |
| `<nav></nav>`           | a navigation bar                                                                                                    |
| `<aside></aside>`       | element representing a portion of a document whose content is only indirectly related to the main content           |
| `<article></article>`   | representing a self-containing part of the website, which is intended to be independently distributable or reusable |
| `<header></header>`     | representing introductory content, typically a group of introductory or navigational aids                           |
| `<footer></footer>`     | typically contains information about the author of the section, copyright data or links to related documents        |

---

## Nesting HTML elements

- Nesting groups elements together in a meaningful way. The element containing the other elements is called the parent element, which contains one or more child elements.

---

## Emmet

Visual Studio Code has a useful tool called Emmet which lets you autocomplete a lot of code by just
typing certain snippets and pressing the <kbd>Tab</kbd> key afterwards. Try these snippets inside an
HTML file and see what happens:

- `!`
- `.highlight`
- `button#red`
- `ul>li.card\*10`

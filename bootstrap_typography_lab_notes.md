# Bootstrap Typography, Abbreviations, Lists and Images
## Student Theory and Practice Notes

---

## 1. Introduction to Bootstrap

Bootstrap is a front-end framework used to create responsive and well-formatted web pages quickly.

It provides ready-made:

- CSS classes
- Typography styles
- Buttons
- Forms
- Tables
- Images
- Lists
- Navigation components
- Responsive layouts
- Many other UI components

Instead of writing all CSS properties ourselves, we can use Bootstrap classes.

### Basic Bootstrap page structure

For the lab shown in the question, Bootstrap can be included using the Bootstrap CDN.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Bootstrap Demo</title>

    <link rel="stylesheet"
          href="https://cdn.jsdelivr.net/npm/bootstrap@3.4.1/dist/css/bootstrap.min.css">
</head>

<body>

    <!-- Bootstrap content goes here -->

</body>
</html>
```

> **Important:** The exact class names for some image utilities depend on the Bootstrap version. The examples in this note use the Bootstrap 3 style of classes because the lab uses classes such as `img-responsive`, `pull-left`, and `pull-right`.

---

# PART A — Bootstrap Typography

Typography means the way text is displayed on a webpage.

Bootstrap provides predefined typography styles so that headings, paragraphs and other text can be displayed consistently.

---

# 2. Bootstrap Headings

HTML already provides six heading levels:

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

Bootstrap automatically gives these headings suitable font sizes, margins and font weights.

### Example

```html
<h1>Darshan University-Rajkot</h1>
<h2>Darshan University-Rajkot</h2>
<h3>Darshan University-Rajkot</h3>
```

### Important idea

The `<h1>` to `<h6>` elements are HTML elements. Bootstrap provides styling for these elements.

---

# 3. Bootstrap Paragraphs

A normal paragraph can be written using:

```html
<p>This is a paragraph.</p>
```

Bootstrap applies its default typography styling to the paragraph.

### Example

```html
<p>
    Darshan University-Rajkot is located on Rajkot-Morbi Highway.
</p>
```

---

# 4. Lead Paragraph

Bootstrap provides the `lead` class to make an introductory paragraph more prominent.

### Syntax

```html
<p class="lead">
    This is an important introductory paragraph.
</p>
```

### Why use `lead`?

A lead paragraph is generally used for:

- Introductions
- Important descriptions
- Opening text
- Short summaries

It makes the paragraph visually larger and more noticeable.

---

# 5. Bootstrap Text Formatting

Bootstrap works together with normal HTML text-formatting elements.

The following elements are commonly used in typography examples:

| HTML Element | Purpose |
|---|---|
| `<mark>` | Highlights text |
| `<del>` | Represents deleted text |
| `<s>` | Represents text that is no longer accurate/relevant |
| `<ins>` | Represents inserted text |
| `<u>` | Underlines text |
| `<small>` | Displays smaller text |
| `<strong>` | Displays important/bold text |
| `<em>` | Gives emphasis, normally italic |

---

# 6. Highlighted Text — `<mark>`

The `<mark>` element highlights text.

### Example

```html
<p>Welcome to <mark>Darshan University</mark></p>
```

The selected text appears highlighted.

### When to use it

Use `<mark>` when you want to draw attention to a particular part of text.

Examples:

- Search results
- Important words
- Matching keywords
- Important information

---

# 7. Deleted Text — `<del>`

The `<del>` element represents text that has been deleted.

### Example

```html
<p><del>Darshan Institute of Engineering and Technology</del></p>
```

The text is normally displayed with a line through it.

### Example with updated information

```html
<p>
    <del>Old University Name</del>
    New University Name
</p>
```

---

# 8. No Longer Relevant Text — `<s>`

The `<s>` element represents text that is no longer accurate or relevant.

### Example

```html
<p><s>Old Information</s></p>
```

The text appears crossed out.

### Difference between `<del>` and `<s>`

- `<del>` means the text has been deleted.
- `<s>` means the text is no longer accurate or relevant.

---

# 9. Inserted Text — `<ins>`

The `<ins>` element represents text that has been inserted into a document.

### Example

```html
<p><ins>Darshan University-Rajkot</ins></p>
```

The text is normally displayed with an underline.

---

# 10. Underlined Text — `<u>`

The `<u>` element represents text with an underline.

### Example

```html
<p>
    <u>Darshan University-Rajkot</u>
</p>
```

> Use underlining carefully because users often expect underlined text to be a link.

---

# 11. Smaller Text — `<small>`

The `<small>` element displays text smaller than the surrounding text.

### Example

```html
<p>
    Darshan University-Rajkot
    <small>Academic Information</small>
</p>
```

It can be useful for:

- Additional information
- Copyright text
- Notes
- Secondary information

---

# 12. Important / Bold Text — `<strong>`

The `<strong>` element indicates that the text has strong importance.

### Example

```html
<p>
    <strong>Darshan University-Rajkot</strong>
</p>
```

The browser normally displays it in bold.

### Important

`<strong>` is more meaningful than simply making text visually bold because it indicates importance.

---

# 13. Emphasized Text — `<em>`

The `<em>` element indicates emphasis.

### Example

```html
<p>
    <em>Darshan University-Rajkot</em>
</p>
```

The browser normally displays emphasized text in italic.

---

# 14. Understanding the Typography Example

The second typography example in the lab demonstrates different ways of displaying the same type of text.

A simplified practice example is:

```html
<p>Welcome to <mark>Darshan University</mark></p>

<p><del>Darshan Institute of Engineering and Technology</del></p>

<p><s>Darshan Institute of Engineering and Technology</s></p>

<p><u>Darshan University-Rajkot</u></p>

<p><ins>Darshan University-Rajkot</ins></p>

<p><small>Darshan University-Rajkot</small></p>

<p><strong>Darshan University-Rajkot</strong></p>

<p><em>Darshan University-Rajkot</em></p>
```

This example is useful for understanding the purpose of different text-formatting elements.

---

# PART B — Abbreviations

# 15. What is an Abbreviation?

An abbreviation is a shortened form of a word or phrase.

Examples:

- HTML — HyperText Markup Language
- CSS — Cascading Style Sheets
- HTTP — HyperText Transfer Protocol
- DBMS — Database Management System

HTML provides the `<abbr>` element for abbreviations.

---

# 16. The `<abbr>` Element

### Syntax

```html
<abbr title="Full Form">Short Form</abbr>
```

The `title` attribute contains the full meaning of the abbreviation.

### Example

```html
<p>
    <abbr title="HyperText Markup Language">HTML</abbr>
    is used to create webpages.
</p>
```

When the user places the mouse pointer over `HTML`, the full form can appear as a tooltip.

### Another example

```html
<p>
    <abbr title="Cascading Style Sheets">CSS</abbr>
    is used to style webpages.
</p>
```

---

# 17. Why Use `<abbr>`?

It provides additional information without making the paragraph longer.

It is useful when:

- An abbreviation is introduced for the first time.
- Technical terms are used.
- Short forms may not be familiar to the reader.

---

# PART C — Text Alignment

# 18. What is Text Alignment?

Text alignment controls the horizontal position of text.

Common alignments are:

- Left
- Center
- Right

Bootstrap provides utility classes for text alignment.

---

# 19. Left-Aligned Text

In Bootstrap 3:

```html
<p class="text-left">
    This text is aligned to the left.
</p>
```

### Explanation

`text-left` tells Bootstrap to align the text to the left.

---

# 20. Center-Aligned Text

```html
<p class="text-center">
    This text is centered.
</p>
```

### Explanation

`text-center` centers the text.

---

# 21. Right-Aligned Text

```html
<p class="text-right">
    This text is aligned to the right.
</p>
```

### Explanation

`text-right` aligns the text to the right.

---

# 22. Text Alignment Summary

| Class | Purpose |
|---|---|
| `text-left` | Left alignment |
| `text-center` | Center alignment |
| `text-right` | Right alignment |

### Practice example

```html
<p class="text-left">Left Text</p>

<p class="text-center">Center Text</p>

<p class="text-right">Right Text</p>
```

---

# PART D — Bootstrap Lists

# 23. What is a List?

A list is used to display multiple related items.

HTML mainly provides:

### Unordered List

```html
<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>Bootstrap</li>
</ul>
```

### Ordered List

```html
<ol>
    <li>HTML</li>
    <li>CSS</li>
    <li>Bootstrap</li>
</ol>
```

Bootstrap provides classes that can change the appearance of these lists.

---

# 24. Unstyled List

Bootstrap 3 provides the `list-unstyled` class.

### Example

```html
<ul class="list-unstyled">
    <li>HTML</li>
    <li>CSS</li>
    <li>Bootstrap</li>
</ul>
```

The default bullets are removed.

### Important

`list-unstyled` removes the default list styling. It does not mean that the list items are removed.

---

# 25. Inline List

Bootstrap 3 also provides the `list-inline` class.

It displays list items horizontally instead of vertically.

### Example

```html
<ul class="list-inline">
    <li>Home</li>
    <li>About</li>
    <li>Contact</li>
</ul>
```

This is useful for:

- Navigation items
- Small groups of links
- Menu-like lists

---

# 26. Difference Between Normal, Unstyled and Inline Lists

### Normal list

```html
<ul>
    <li>Home</li>
    <li>About</li>
    <li>Contact</li>
</ul>
```

Items normally appear vertically with bullets.

### Unstyled list

```html
<ul class="list-unstyled">
    <li>Home</li>
    <li>About</li>
    <li>Contact</li>
</ul>
```

Bullets are removed.

### Inline list

```html
<ul class="list-inline">
    <li>Home</li>
    <li>About</li>
    <li>Contact</li>
</ul>
```

Items appear horizontally.

---

# PART E — Bootstrap Responsive Images

# 27. What is a Responsive Image?

A responsive image automatically adjusts according to the available screen/container width.

This is important because a webpage may be opened on:

- Desktop
- Laptop
- Tablet
- Mobile phone

An image that looks good on a desktop should not overflow the screen on a mobile device.

---

# 28. Basic Image

The normal HTML image element is:

```html
<img src="image.jpg" alt="University">
```

Here:

- `src` specifies the image path.
- `alt` provides alternative text.

---

# 29. Bootstrap `img-responsive`

In Bootstrap 3, the `img-responsive` class is used to make an image responsive.

### Syntax

```html
<img src="image.jpg" class="img-responsive" alt="University">
```

The class makes the image scale appropriately within its containing element.

### Important idea

`img-responsive` is a Bootstrap class.

It is not an HTML attribute.

---

# 30. Why Responsive Images Are Needed

Suppose an image is wider than a mobile screen.

Without responsive behavior:

```text
+--------------------------+
| Mobile Screen            |
|                          |
|   IMAGE TOO WIDE ------->|
|                          |
+--------------------------+
```

The image may cause horizontal scrolling.

With responsive behavior:

```text
+--------------------------+
| Mobile Screen            |
|                          |
|      IMAGE               |
|   fits the screen        |
|                          |
+--------------------------+
```

Responsive design makes the webpage easier to use on different screen sizes.

---

# PART F — Image Alignment

The lab also asks to align a responsive image to:

1. Left
2. Center
3. Right

---

# 31. Left-Aligned Image

Bootstrap 3 provides `pull-left`.

### Example

```html
<img src="image.jpg"
     class="img-responsive pull-left"
     alt="University">
```

`pull-left` moves the image toward the left side.

---

# 32. Right-Aligned Image

Bootstrap 3 provides `pull-right`.

### Example

```html
<img src="image.jpg"
     class="img-responsive pull-right"
     alt="University">
```

`pull-right` moves the image toward the right side.

---

# 33. Center-Aligned Image

Bootstrap 3 provides `center-block`.

### Example

```html
<img src="image.jpg"
     class="img-responsive center-block"
     alt="University">
```

`center-block` makes the image behave as a block and centers it horizontally.

---

# 34. Image Alignment Summary

| Bootstrap class | Purpose |
|---|---|
| `pull-left` | Align image toward left |
| `center-block` | Center the image |
| `pull-right` | Align image toward right |
| `img-responsive` | Make image responsive |

### Combining classes

Bootstrap classes can be combined.

```html
<img src="image.jpg"
     class="img-responsive center-block"
     alt="University">
```

Here two classes are applied:

- `img-responsive`
- `center-block`

---

# PART G — Bootstrap Thumbnail

# 35. What is a Thumbnail?

A thumbnail is a small or visually framed representation of an image.

Bootstrap provides the `img-thumbnail` class.

### Example

```html
<img src="image.jpg"
     class="img-thumbnail"
     alt="University">
```

Bootstrap adds styling such as:

- Border
- Padding
- Rounded appearance
- Thumbnail-like presentation

---

# 36. Responsive Thumbnail

Classes can also be combined.

```html
<img src="image.jpg"
     class="img-responsive img-thumbnail"
     alt="University">
```

This combines:

- Responsive image behavior
- Thumbnail styling

---

# PART H — Understanding Bootstrap Classes

# 37. What is a Bootstrap Class?

A Bootstrap class is a predefined CSS class supplied by Bootstrap.

Example:

```html
<p class="text-center">Hello</p>
```

Here:

```text
class="text-center"
       |
       +---- Bootstrap utility class
```

Bootstrap already contains CSS rules for the class.

Therefore, we do not have to write the corresponding CSS ourselves.

---

# 38. Multiple Bootstrap Classes

More than one class can be applied to the same element.

Example:

```html
<img class="img-responsive center-block img-thumbnail"
     src="image.jpg"
     alt="University">
```

This element uses three Bootstrap classes:

```text
img-responsive
      +
center-block
      +
img-thumbnail
```

Each class provides a different type of styling/behavior.

---

# PART I — Complete Concept Practice

The following examples are intended for understanding the concepts used in the lab.

## Typography

```html
<h1>Darshan University-Rajkot</h1>

<p>
    Rajkot-Morbi Highway,<br>
    Hadala,<br>
    Email: info@darshan.ac.in,<br>
    Phone: 0281-2569612
</p>
```

---

## Text Formatting

```html
<p>Welcome to <mark>Darshan University</mark></p>

<p><del>Old Information</del></p>

<p><s>Old Information</s></p>

<p><u>Underlined Information</u></p>

<p><ins>Inserted Information</ins></p>

<p><small>Small Information</small></p>

<p><strong>Important Information</strong></p>

<p><em>Emphasized Information</em></p>
```

---

## Abbreviation

```html
<p>
    <abbr title="HyperText Markup Language">HTML</abbr>
    is a markup language.
</p>
```

---

## Text Alignment

```html
<p class="text-left">Left aligned text</p>

<p class="text-center">Center aligned text</p>

<p class="text-right">Right aligned text</p>
```

---

## Unstyled List

```html
<ul class="list-unstyled">
    <li>HTML</li>
    <li>CSS</li>
    <li>Bootstrap</li>
</ul>
```

---

## Inline List

```html
<ul class="list-inline">
    <li>Home</li>
    <li>About</li>
    <li>Contact</li>
</ul>
```

---

## Responsive Image

```html
<img src="image.jpg"
     class="img-responsive"
     alt="University">
```

---

## Left Image

```html
<img src="image.jpg"
     class="img-responsive pull-left"
     alt="University">
```

---

## Center Image

```html
<img src="image.jpg"
     class="img-responsive center-block"
     alt="University">
```

---

## Right Image

```html
<img src="image.jpg"
     class="img-responsive pull-right"
     alt="University">
```

---

## Thumbnail

```html
<img src="image.jpg"
     class="img-thumbnail"
     alt="University">
```

---

# PART J — Important Bootstrap Classes for This Lab

| Class / Element | Meaning |
|---|---|
| `lead` | Makes a paragraph more prominent |
| `text-left` | Left-aligns text |
| `text-center` | Centers text |
| `text-right` | Right-aligns text |
| `list-unstyled` | Removes default list styling |
| `list-inline` | Displays list items inline |
| `img-responsive` | Makes an image responsive in Bootstrap 3 |
| `pull-left` | Moves an element toward the left |
| `center-block` | Centers a block element |
| `pull-right` | Moves an element toward the right |
| `img-thumbnail` | Gives an image thumbnail styling |

---

# PART K — Important HTML Elements Used

| Element | Purpose |
|---|---|
| `<h1>` | Main heading |
| `<p>` | Paragraph |
| `<mark>` | Highlighted text |
| `<del>` | Deleted text |
| `<s>` | No longer relevant text |
| `<ins>` | Inserted text |
| `<u>` | Underlined text |
| `<small>` | Smaller text |
| `<strong>` | Important text |
| `<em>` | Emphasized text |
| `<abbr>` | Abbreviation |
| `<ul>` | Unordered list |
| `<ol>` | Ordered list |
| `<li>` | List item |
| `<img>` | Image |
| `src` | Image source |
| `alt` | Alternative text |
| `title` | Additional information/tooltip |

---

# PART L — Bootstrap Class vs HTML Element

Students should understand the difference between an HTML element and a Bootstrap class.

### HTML element

```html
<p>Hello</p>
```

`p` is an HTML element.

### Bootstrap class

```html
<p class="text-center">Hello</p>
```

`text-center` is a Bootstrap class.

### Both together

```html
<p class="text-center">
    Hello
</p>
```

The HTML element creates the paragraph, while Bootstrap provides the styling through the class.

---

# PART M — Combining HTML and Bootstrap

A webpage normally combines HTML elements with Bootstrap classes.

Example:

```html
<ul class="list-inline">
    <li>Home</li>
    <li>About</li>
    <li>Contact</li>
</ul>
```

Here:

- `<ul>` creates the unordered list.
- `<li>` creates each list item.
- `list-inline` changes the Bootstrap styling of the list.

Another example:

```html
<img src="image.jpg"
     class="img-responsive center-block"
     alt="University">
```

Here:

- `<img>` creates the image.
- `img-responsive` makes it responsive.
- `center-block` centers it.
- `src` specifies the image.
- `alt` provides alternative text.

---

# PART N — Lab Part C: Designing Your Own Page

The final part of the lab asks students to design a page of their choice using the concepts learned above.

The purpose is to combine multiple Bootstrap concepts into one webpage.

Possible page themes include:

- University information page
- Student profile
- Course information page
- College department page
- Technology information page
- Personal introduction page

A student-designed page could contain:

```text
Page
 |
 +-- Heading
 |
 +-- Paragraph
 |
 +-- Highlighted text
 |
 +-- Text formatting
 |
 +-- Abbreviation
 |
 +-- List
 |
 +-- Image
 |
 +-- Image alignment
 |
 +-- Thumbnail
```

The important goal is to understand how the individual concepts can be combined.

---

# PART O — Common Mistakes

## Mistake 1: Forgetting Bootstrap

This will not apply Bootstrap styling:

```html
<p class="text-center">Hello</p>
```

if Bootstrap CSS has not been included.

Always include Bootstrap CSS in the `<head>`.

---

## Mistake 2: Misspelling class names

Incorrect:

```html
<p class="text-centre">Hello</p>
```

Correct:

```html
<p class="text-center">Hello</p>
```

Bootstrap class names must be written correctly.

---

## Mistake 3: Confusing `class` with `id`

Bootstrap utility classes are normally applied using:

```html
class="text-center"
```

not:

```html
id="text-center"
```

---

## Mistake 4: Forgetting `alt` on images

Prefer:

```html
<img src="image.jpg" alt="University">
```

rather than:

```html
<img src="image.jpg">
```

The `alt` attribute provides alternative text for the image.

---

## Mistake 5: Using the wrong Bootstrap version

Some Bootstrap classes differ between versions.

For example, Bootstrap 3 uses:

```html
<img class="img-responsive">
```

Newer Bootstrap versions use different responsive-image utilities.

Therefore, always check which Bootstrap version is being used in the lab.

---

# PART P — Quick Revision

## Typography

```text
<h1> ... <h6>   → Headings
<p>              → Paragraph
<mark>           → Highlight
<del>            → Deleted text
<s>              → No longer relevant text
<ins>            → Inserted text
<u>              → Underline
<small>          → Smaller text
<strong>         → Important text
<em>             → Emphasis
```

## Abbreviation

```html
<abbr title="Full Form">Short Form</abbr>
```

## Text Alignment

```text
text-left
text-center
text-right
```

## Lists

```text
list-unstyled
list-inline
```

## Images

```text
img-responsive
pull-left
center-block
pull-right
img-thumbnail
```

---

# Final Learning Checklist

Before attempting the lab, students should be able to explain:

- What Bootstrap is.
- Why Bootstrap is used.
- How Bootstrap CSS is included.
- What typography means.
- How Bootstrap styles headings and paragraphs.
- What the `lead` class does.
- What `<mark>` does.
- Difference between `<del>` and `<s>`.
- What `<ins>` does.
- What `<u>` does.
- What `<small>` does.
- What `<strong>` does.
- What `<em>` does.
- What an abbreviation is.
- How `<abbr>` and `title` work together.
- How to align text using Bootstrap classes.
- What an unordered list is.
- What `list-unstyled` does.
- What `list-inline` does.
- What a responsive image is.
- What `img-responsive` does in Bootstrap 3.
- How to align an image left, center and right.
- What `pull-left` does.
- What `center-block` does.
- What `pull-right` does.
- What `img-thumbnail` does.
- How multiple Bootstrap classes can be applied to one element.
- Why the Bootstrap version matters.

---

# One-Line Revision

> **Bootstrap provides ready-made CSS classes that help us style typography, align text, format lists, make images responsive, align images and create thumbnail-style images without writing all the CSS ourselves.**

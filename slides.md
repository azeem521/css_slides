# Introduction to CSS

## What is CSS?

- **CSS** stands for **Cascading Style Sheets**.
- It is responsible for the appearance of a webpage.
- CSS controls the layout, colors, fonts, and overall appearance of web pages.

---

## How CSS Works with HTML

- HTML provides the structure of the page (elements, content).
- CSS applies styles to these HTML elements, determining how they should look.
- Example:

  <!-- HTML -->

  `<h1>Hello, World!</h1>`

  <!-- CSS -->

````md magic-move {lines: true}
```ts
`selector {

 }`;
```

```ts
`h1 {

 }`;
```

```ts
`h1 {
       color
 }`;
```

```ts
`h1 {
       color:
 }`;
```

```ts
`h1 {
       color:blue
 }`;
```

```ts
`h1 {
      color:blue;
}`;
```

```ts
`h1 {
     color:blue;
     font-size: 24px;
}`;
```
````

---

# Inline, Internal, and External CSS

<v-click>
Inline CSS: Added directly to an HTML element using the style attribute.
</v-click>

<v-click>
```html
<p style="color: green;" >This is an inline styled paragraph.</p>
```
</v-click>

---

# Internal CSS: Written inside a `<style>` tag in the HTML `<head>`

<v-click>
Inline CSS: Added directly to an HTML element using the style attribute.
</v-click>
<v-click>
```ts
<!doctype html>
<html lang="en">
  <head>
    <title>Document</title>
    <style>
      p {
        color: orange;
      }
      h1 {
        color: blue;
        text-align: center;
      }
    </style>
  </head>
  <body>
    <h1>Hello, World!</h1>
    <p>This is a paragraph with internal CSS styling.</p>
  </body>
</html>
```
</v-click>

---

# External CSS: Saved in a separate file and linked to the HTML.

<v-click>
Create a CSS file (e.g., styles.css).
</v-click>
<v-click>
```ts
<!doctype html>
<html lang="en">
  <head>
    <title>Document</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <h1>Hello, World!</h1>
    <p>This is a paragraph with external CSS styling.</p>
  </body>
</html>
```
</v-click>

---

## What is a CSS Selector?

CSS selectors are used to "select" HTML elements you want to style. Selectors define which elements the CSS rules apply to.

## How to Use Selectors

- **Syntax**: A CSS selector is followed by a declaration block.
- **Example**:

  ```css
  selector {
    property: value;
  }
  ```

---

# CSS Basic Selectors

Fundamental Building Blocks of Styling

1. Universal Selector
2. Type Selector (Element Selector)
3. Class Selector
4. ID Selector

---

# Universal Selector

- Selects all elements on the page
- Denoted by an asterisk (\*)
- Use with caution as it affects every element

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

---

# Type Selector (Element Selector)

- Selects all instances of a specific HTML element
- Simply use the element name

```css
p {
  color: #333;
  line-height: 1.6;
}

h1 {
  font-size: 2em;
  margin-bottom: 20px;
}
```

---

# Class Selector

- Selects elements with a specific class attribute
- Denoted by a dot (.) followed by the class name
- Can be applied to multiple elements

```html
<p class="highlight">This is a highlighted paragraph.</p>
<button class="btn">Click Me</button>
```

```css
/* css styling */
.highlight {
  background-color: yellow;
}

.btn {
  padding: 10px 15px;
  border-radius: 5px;
}
```

---

# ID Selector

- Selects a single element with a specific id attribute
- Denoted by a hash (#) followed by the id name
- Should be unique within a page

```html
<div id="header">
  <nav id="main-navigation">
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#services">Services</a>
    <a href="#contact">Contact</a>
  </nav>
</div>
```

```css
#header {
  background-color: #f0f0f0;
  padding: 20px;
}
#main-navigation {
  display: flex;
  justify-content: space-between;
}
```

---

# Specificity of Basic Selectors

- ID Selector (Most specific)
- Class Selector
- Type Selector
- Universal Selector (Least specific)

```html
<header id="header" class="header">Hello, World!</header>
```

```css
* {
  color: red;
} /* Lowest specificity */
header {
  color: green;
} /* Lower specificity */
#header {
  color: black;
} /* Highest specificity */
.header {
  color: blue;
} /* Medium specificity */
```

---

# Best Practices

<v-click>
- Use type selectors for broad styles<br>
</v-click>

<v-click>
- Prefer class selectors for reusable styles<br>
</v-click>

<v-click>
- Use ID selectors sparingly<br>
</v-click>

<v-click>
- Avoid overusing the universal selector<br>
</v-click>

<v-click>
- Combine selectors to increase specificity when needed<br>
</v-click>

---

# Task 1

## Requirements:

1. **Title**: Set the document title to "CSS Demonstration".

2. **HTML Structure**:

```
   - Include the following elements in your HTML document:
     - A heading with the text "CSS Demonstration".
     - Three paragraphs:
       - The first paragraph should have the class `highlight` and the text "This is a highlighted paragraph."
       - The second paragraph should have the ID `main` and the text "This is the main paragraph."
       - The third paragraph should be a normal paragraph without any class or ID and the text "This is a normal paragraph."

```

---

# CSS Demonstration

```

 Inline CSS

- Add inline CSS: Change the color of one paragraph to green using inline CSS.

Internal CSS

- Add internal CSS: Use a `<style>` tag in the HTML `<head>` to apply the following styles:
  - All paragraphs (`<p>`) should have a font size of 16px.
  - The paragraph with the class `highlight` should have a background color of yellow.
  - The paragraph with the ID `main` should have a background color of lightgray and a font style of italic.

External CSS

- Create an external CSS file: Create a file named `styles.css`.
- Add styles in `styles.css`:
  - Set the color of all headings (`<h1>`) to blue.
  - Center-align the text of all headings (`<h1>`).

Link External CSS

- Link `styles.css` to your HTML document**: Use a `<link>` tag inside the `<head>` of your HTML document to link the external CSS file (`styles.css`).
```

---

# Task 2

## Requirements:

1. **Title**: Set the document title to "CSS Demonstration".

2. **HTML Structure**:

```
   - Include the following elements in your HTML document:
     - A heading with the text "HTML and CSS Practice".
     - Three paragraphs:
       - The first paragraph should have the class `note` and the text "This is a note."
       - The second paragraph should have the ID `important` and the text "This is an important message."
       - The third paragraph should be a normal paragraph without any class or ID and the text "This is a general message."

```

# [Output should be like this](https://drive.google.com/file/d/1j6Xzv3hXeaxngLHriZB2bAc5Q-QcVzMU/view?usp=sharing)

---

# CSS Demonstration

```

 Inline CSS

- Add inline CSS: Change the color of the first paragraph to blue using inline CSS.

Internal CSS

- Add internal CSS: Use a `<style>` tag in the HTML `<head>` to apply the following styles:
  - All paragraphs (`<p>`) should have a font size of 18px.
  - The paragraph with the class `note` should have a background color of lightblue.
  - The paragraph with the ID `important` should have a background color of pink and a font weight of bold.

External CSS

- Create an external CSS file: Create a file named `styles.css`.
- Add styles in `styles.css`:
  - Set the color of all headings (`<h1>`) to green.
  - Center-align the text of all headings (`<h1>`).

Link External CSS

- Link `styles.css` to your HTML document: Use a `<link>` tag inside the `<head>` of your HTML document to link the external CSS file (`styles.css`).
```

---

## What is the CSS Box Model?

- Fundamental concept in CSS
- Describes how elements are rendered on a web page
- Consists of four parts: Content, Padding, Border, and Margin

## Visual Representation

```ts
+-------------------------------------------+
|                  Margin                   |
|    +-----------------------------------+  |
|    |             Border                |  |
|    |    +--------------------------+   |  |
|    |    |         Padding          |   |  |
|    |    |    +--------------+      |   |  |
|    |    |    |              |      |   |  |
|    |    |    |   Content    |      |   |  |
|    |    |    |              |      |   |  |
|    |    |    +--------------+      |   |  |
|    |    |                          |   |  |
|    |    +--------------------------+   |  |
|    |                                   |  |
|    +-----------------------------------+  |
|                                           |
+-------------------------------------------+
```

---

## Box Sizing

- Default: `box-sizing: content-box`
  - Width and height apply to content area only
- Alternative: `box-sizing: border-box`
  - Width and height include padding and border

```css
* {
  box-sizing: border-box;
}
```

---

# Margin

## Margin Properties

- Creates space around elements
- Transparent area outside the border
- Can have negative values

```css
.element {
  margin-top: 10px;
  margin-right: 20px;
  margin-bottom: 10px;
  margin-left: 20px;
}
```

---

Margin Shorthand

```css
/* Apply to all sides */
margin: 10px;

/* vertical | horizontal */
margin: 10px 20px;

/* top | horizontal | bottom */
margin: 10px 20px 15px;

/* top | right | bottom | left */
margin: 10px 20px 15px 25px;
```

---

# Margin Collapse

- Vertical margins of adjacent elements can collapse
- The larger margin "wins"

```css
.top-element {
  margin-bottom: 20px;
}
.bottom-element {
  margin-top: 30px;
}
/* Resulting gap: 30px, not 50px */
```

---

# Border Properties

- Can have width, style, and color

```css
.element {
  border-width: 2px;
  border-style: solid;
  border-color: #000;
}
```

<v-click>
Border Styles

`solid`<br>
`dashed`<br>
`dotted`<br>
`double`<br>
`groove`<br>
`ridge`<br>
`inset`<br>
`outset`<br>
`none`<br>
`hidden`<br>
</v-click>

---

# Border Radius

## Creates rounded corners

```css
.rounded {
  border-radius: 10px;
}

.circle {
  border-radius: 50%;
}

/* Individual corners */
.custom {
  border-top-left-radius: 5px;
  border-top-right-radius: 10px;
  border-bottom-right-radius: 15px;
  border-bottom-left-radius: 20px;
}
```

---

# Padding Properties

- Creates space inside the element, between content and border
- Cannot have negative values

```css
.element {
  padding-top: 10px;
  padding-right: 20px;
  padding-bottom: 10px;
  padding-left: 20px;
}
```

```css
/* Apply to all sides */
padding: 10px;

/* vertical | horizontal */
padding: 10px 20px;

/* top | horizontal | bottom */
padding: 10px 20px 15px;

/* top | right | bottom | left */
padding: 10px 20px 15px 25px;
```

---

# Padding and Box Sizing

- With `box-sizing: content-box`, padding increases element size
- With `box-sizing: border-box`, padding squeezes content area

```css
.content-box {
  box-sizing: content-box;
  width: 100px;
  padding: 20px;
  /* Total width: 140px */
}

.border-box {
  box-sizing: border-box;
  width: 100px;
  padding: 20px;
  /* Total width: 100px */
}
```

---

# Content Area

- The inner-most part of the box
- Where text and images appear
- Dimensions set by width and height properties

```css
.element {
  width: 300px;
  height: 200px;
}
```

---

# Inline vs Block Elements

## Inline elements:

- Only occupy necessary width
- Don't force new lines
- width and height properties have no effect

## Block elements:

- Occupy full width available
- Force new lines before and after

```css
.inline {
  display: inline;
}

.block {
  display: block;
}
```

---

# Task 1

## Requirements:

1. **Title**: Set the document title to "CSS Box Model Example.

2. **HTML Structure**:

```
   - Include the following elements in your HTML document:
     - A heading (<h1>) with the text "CSS Box Model Example".
     - A container <div> with the class box-model containing a paragraph with the text "This is an example of the CSS Box Model.
       - Apply box-sizing: border-box to all elements using the universal selector.
       - Add margin to the container element to create space around it.
       - Add padding to the container element to create space inside it.
       - Add a border to the container element to visualize its boundary.
       - Apply a border radius to the container element to create rounded corners.

```

---

# Task 2

## Requirements:

1. **Title**: Set the document title to "CSS Box Model Example.

2. **HTML Structure**:

```
   - Include the following elements in your HTML document:
     - A heading (<h1>) with the text "Box Model Practice".
     - A container <div> with the class box-example containing a paragraph with the text "Exploring the CSS Box Model with different styles."
       - Apply box-sizing: content-box to all elements using the universal selector.
       - Add margin to the container element to create space around it.
       - Add padding to the container element to create space inside it.
       - Add a border to the container element to visualize its boundary.
       - Apply a border radius to the container element to create rounded corners.

```

# [Output should be like this](https://drive.google.com/file/d/1suhnOYZ5yQaCMKhhC9vPEhac8fwpzNvN/view?usp=sharing)

---

# Typography

## 1. Font Properties

- `font-family`: Defines the font of text
- `font-size`: Sets the size of the font
- `font-weight`: Specifies the thickness of the font (e.g., normal, bold)

<v-click>

## 2. Text Properties

 </v-click>
  <v-click>
color: Sets the color of text <br>
text-align: Aligns text horizontally (left, center, right, justify) <br>
text-indent: Indents the first line of text <br>
  </v-click>

---

## 3. Line Height

- `line-height`: Controls the height of lines of text
- Ensures proper vertical spacing and readability

<v-click>
Text Alignment <br>
</v-click>
<v-click>
text-align: Aligns text horizontally within its container <br>
Options: left, center, right, justify <br>
</v-click>
<v-click>
Text Decoration

text-decoration: Adds visual effects to text (underline, overline, line-through)
</v-click>
<v-click>
Text Transformation <br>
</v-click>
<v-click>
text-transform: Transforms text appearance (uppercase, lowercase, capitalize)
</v-click>

---

## Letter Spacing

- `letter-spacing`: Adjusts spacing between characters in text
- Useful for fine-tuning typography

<v-click>
Word Spacing <br>
</v-click>

<v-click>
word-spacing: Sets the spacing between words in text <br>
Enhances readability and visual appeal
</v-click>

---

# Color in CSS

<v-click>

Different ways to represent colors! <br>

</v-click>

<v-click>
1. Named Colors <br>
```css
color: red;
background-color: skyblue;
border-color: orange;
```
</v-click>

<v-click>
2. Hexadecimal Colors <br>
```css
color: #FF0000; /* Red */
background-color: #00FF00; /* Green */
border-color: #0000FF; /* Blue */
```
</v-click>

<v-click>
3. RGB/RGBA Colors <br>
```css
color: rgb(255, 0, 0); /* Red */
background-color: rgba(0, 255, 0, 0.5); /* Semi-transparent Green */
```
</v-click>

<!-- <v-click>
4. HSL/HSLA Colors <br>
```css
color: hsl(0, 100%, 50%); /* Red */
background-color: hsla(120, 100%, 50%, 0.5); /* Semi-transparent Green */
```
</v-click> -->

---

# Background Properties in CSS

<v-clicks>
Background Color
</v-clicks>
<v-clicks>

- Sets the background color of an element
- Can use various color formats (named, hex, RGB, HSL)
- Applies to the entire element including padding

</v-clicks>

<v-clicks>
```css
.element {
  background-color: #3498db;
}
```
</v-clicks>

---

# Background Image

<v-clicks>

- Adds an image as the background of an element
- Can use local files or URLs

</v-clicks>

<v-clicks>
```css
.element {
  background-image: url('path/to/image.jpg');
}
```
</v-clicks>

---

# Background Repeat

<v-clicks>

- Controls how background images are repeated
- Options: repeat, repeat-x, repeat-y, no-repeat, space, round
- Useful for creating patterns or single image backgrounds

</v-clicks>

<v-clicks>
```css
.element {
  background-image: url('pattern.png');
  background-repeat: repeat-x;
}
```
</v-clicks>

---

# Background Position

<v-clicks>

- Specifies the starting position of a background image
- Can use keywords (top, bottom, left, right, center) or specific values
- Allows fine-tuning of image placement

</v-clicks>

<v-clicks>
```css
.element {
  background-image: url('sprite.png');
  background-position: center top;
}
```
</v-clicks>

---

# Background Size

<v-clicks>

- Controls the size of background images
- Options: auto, cover, contain, or specific dimensions
- Useful for responsive designs and image scaling

</v-clicks>

<v-clicks>
```css
.element {
  background-image: url('large-image.jpg');
  background-size: cover;
}
```
</v-clicks>

---

## Putting It All Together

<v-clicks>
```css
.hero-section {
  background-color: #f1c40f;
  background-image: url('overlay.png'), url('main-bg.jpg');
   <!-- When specifying multiple background images, they are listed in a comma-separated list. The first image listed
   is on top, and each subsequent image is layered beneath the previous one. -->
  background-repeat: repeat, no-repeat;
  background-position: center;
  background-size: auto, cover;
}
```
</v-clicks>

---

# Borders and Shadows in CSS

<v-clicks>

border-width <br>

</v-clicks>
<v-clicks>

border-style <br>

</v-clicks>
<v-clicks>

border-color <br>

</v-clicks>
<v-clicks>

Border Radius <br>

</v-clicks>

<v-clicks>
```css
.box {
  border-width: 2px 3px 2px 3px;
  border-style: solid dashed solid dashed;
  border-color: #3498db #e74c3c #3498db #e74c3c;
}
.rounded-box {
  border-radius: 10px;
}
.custom-shape {
  border-top-left-radius: 20px;
  border-bottom-right-radius: 50%;
}
```
</v-clicks>

---

# Borders and Shadows in CSS

<v-clicks>

Box Shadow

</v-clicks>

<v-clicks>

Adds shadow effects to elements <br>
Can create multiple shadows <br>
Properties: x-offset, y-offset, blur-radius, spread-radius, color <br>

</v-clicks>

<v-clicks>
```css
.shadowed-box {
  box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.3);
}
.multi-shadow {
  box-shadow: 
    0 0 10px rgba(0, 0, 0, 0.1),
    0 0 20px rgba(0, 0, 0, 0.1),
    0 0 30px rgba(0, 0, 0, 0.1);
}
```
</v-clicks>

---

# Borders and Shadows in CSS

<v-clicks>

Text Shadow

</v-clicks>

<v-clicks>

Adds shadow effects to text <br>
Similar to box-shadow, but without spread-radius <br>
Can create multiple shadows for complex effects <br>

</v-clicks>

<v-clicks>
```css
.shadowed-text {
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}
.glow-text {
  color: #ffffff;
  text-shadow: 
    0 0 5px #fff,
    0 0 10px #fff,
    0 0 15px #fff,
    0 0 20px #ff00de,
    0 0 35px #ff00de,
    0 0 40px #ff00de;
}
```
</v-clicks>

---

# Borders and Shadows in CSS

<v-clicks>

Combining Effects

</v-clicks>

<v-clicks>
```css
.fancy-button {
  background-color: #3498db;
  border: 2px solid #2980b9;
  border-radius: 10px;
  box-shadow: 
    0 5px 15px rgba(0, 0, 0, 0.1),
    0 0 0 1px rgba(255, 255, 255, 0.2) inset;
  color: white;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
}
```
</v-clicks>

---

# Task 1

## Title: Set the document title to "Typography and Color Practice".

```
- Include the following elements in your HTML document:

  - A heading (<h1>) with the text "Typography and Color Practice".
  - A container <div> with the class `text-box` containing the following elements:
    - A paragraph with the class `highlight` and the text "This is a highlighted text with specific font properties."
    - A paragraph with the class `important` and the text "This is an important message with different text properties."
    - A paragraph with the class `info` and the text "This is a general information text with adjusted line height and spacing."
```

---

# CSS Instructions

```
- Global Styles:

  - Universal Selector:
  - Apply box-sizing: content-box to all elements. This ensures that padding and border are not included in the width and height calculations.

- Container (.text-box):

      - Margin: Add 20px margin to create space around the container.
      - Padding: Add 20px padding inside the container for internal spacing.
      - Border: Add a 1px solid border with color #ddd (light grey) to visualize the container boundary.
      - Border Radius: Apply 8px border-radius to create rounded corners.
      - Background Color: Set the background color to #f9f9f9 (very light grey).
```

---

```
- Highlighted Text (.highlight):

      - Font Family: Set the font family to Arial, sans-serif.
      - Font Size: Set the font size to 20px.
      - Font Weight: Set the font weight to bold.
      - Text Color: Set the text color to #ff6347 (Tomato).
      - Text Alignment: Align the text to center.
      - Text Indent: Add a 10px indent to the first line.
      - Line Height: Set the line height to 1.5 for improved readability.
      - Letter Spacing: Set the letter spacing to 0.5px.
```

---

```
- Important Message (.important):

      - Font Family: Set the font family to Georgia, serif.
      - Font Size: Set the font size to 18px.
      - Font Weight: Set the font weight to bold.
      - Text Color: Set the text color to #2e8b57 (SeaGreen).
      - Text Alignment: Align the text to left.
      - Text Indent: Add a 20px indent to the first line.
      - Line Height: Set the line height to 1.8 for extra spacing between lines.
      - Letter Spacing: Set the letter spacing to 1px.
```

---

```
- General Information (.info):

      - Font Family: Set the font family to 'Courier New', monospace.
      - Font Size: Set the font size to 16px.
      - Font Weight: Set the font weight to normal.
      - Text Color: Set the text color to #4682b4 (SteelBlue).
      - Text Alignment: Align the text to justify.
      - Text Indent: Add a 15px indent to the first line.
      - Line Height: Set the line height to 1.6.
      - Letter Spacing: Set the letter spacing to 0.8px.
      - Word Spacing: Add 2px spacing between words for better readability.
```

---

# Task 2

## Title: Set the document title to "Typography and Background Styles"

```
- Include the following elements in your HTML document:

  - A heading (<h1>) with the text "Typography and Background Styles".
  - A container <div> with the class `box-container` containing the following elements:
    - A paragraph with the class `featured` and the text "This is a featured paragraph with custom styling."
    - A paragraph with the class `standard` and the text "This paragraph is styled with standard text properties."
    - A paragraph with the class `basic` and the text "This is a basic paragraph with minimal styling."

```

---

# CSS Instructions

```
- Global Styles:

  - Universal Selector:
  - Apply box-sizing: border-box to all elements. This ensures that padding and border are included in the width and height calculations.

- Container (.box-container):

      - Margin: Add 30px margin to create space around the container.
      - Padding: Add 10px padding inside the container for internal spacing.
      - Border: Add a 3px solid border with color #999 (medium gray) to visualize the container boundary.
      - Border Radius: Apply 12px border-radius to create rounded corners.
      - Background Color: Set the background color to #fafafa (off-white).
```

---

```
- Featured Text (.featured):

      - Font Family: Set the font family to 'Helvetica', sans-serif.
      - Font Size: Set the font size to 24px.
      - Font Weight: Set the font weight to bold.
      - Text Color: Set the text color to #ff1493 (DeepPink).
      - Text Alignment: Align the text to left.
      - Text Indent: Add a 15px indent to the first line.
      - Line Height: Set the line height to 1.6 for better readability.
      - Letter Spacing: Set the letter spacing to 0.4px.

```

---

```
- Standard Text (.standard):

      - Font Family: Set the font family to 'Georgia', serif.
      - Font Size: Set the font size to 18px.
      - Font Weight: Set the font weight to normal.
      - Text Color: Set the text color to #4169e1 (RoyalBlue).
      - Text Alignment: Align the text to right.
      - Line Height: Set the line height to 1.5.
      - Letter Spacing: Set the letter spacing to 0.6px.

```

---

```
- Basic Text (.basic):

      - Font Family: Set the font family to 'Lucida Console', monospace.
      - Font Size: Set the font size to 15px.
      - Font Weight: Set the font weight to normal.
      - Text Color: Set the text color to #808080 (Gray).
      - Text Alignment: Align the text to center.
      - Line Height: Set the line height to 1.4.
      - Letter Spacing: Set the letter spacing to 0.3px.
      - Word Spacing: Add 1px spacing between words.

```

# [Output should be like this](https://drive.google.com/file/d/1SC_pUMlMSytlUPelUR8dNOo6rPEClNHx/view?usp=sharing)

---

# Layout Techniques

## What is the Display Property?

- Specifies how an element should be displayed
- Determines the layout behavior of the element
- Affects how the element interacts with other elements

## Common Display Values

1. `block`
2. `inline`
3. `inline-block`
4. `none`
5. `flex`
6. `grid`

---

## Display: Block

- Takes up the full width available
- Starts on a new line
- Can have margin and padding on all sides

```css
.block-element {
  display: block;
  width: 50%;
  margin: 10px;
  padding: 10px;
}
```

---

# Display: Inline

- Takes up only as much width as necessary
- Does not start on a new line
- Cannot have width and height set
- Vertical margin and padding are not respected

```css
.inline-element {
  display: inline;
  margin: 10px; /* Only horizontal margins apply */
  padding: 10px; /* Only horizontal padding applies */
}
```

---

# Display: Inline-Block

- Combines features of both block and inline
- Flows with text (inline)
- Can have width, height, margins, and padding (block)

```css
.inline-block-element {
  display: inline-block;
  width: 100px;
  height: 100px;
  margin: 10px;
  padding: 10px;
}
```

---

# Display: None

- Removes the element from the document flow
- Element is not visible and does not take up space

```css
.hidden-element {
  display: none;
}
```

---

# Task 1

## Requirements:

1. **Title**: Set the document title to "Display Property Example".

2. **HTML Structure**:

```
   - Include the following elements in your HTML document:
     - A heading (<h1>) with the text "Display Property Example".
     - Three container <div> elements with different classes to demonstrate the display properties:
       - A <div> with the class block-element containing a paragraph with the text "This is a block element".
       - A <div> with the class inline-element containing a paragraph with the text "This is an inline element".
       - A <div> with the class inline-block-element containing a paragraph with the text "This is an inline-block element".
       - A <div> with the class hidden-element containing a paragraph with the text "This element is hidden".
       - Apply a border radius to the container element to create rounded corners.
  - CSS:
      - Apply display: block to the element with the class block-element.
      - Set the width, margin, and padding for the block element.
      - Apply display: inline to the element with the class inline-element.
      - Set horizontal margin and padding for the inline element.
      - Apply display: inline-block to the element with the class inline-block-element.
      - Set width, height, margin, and padding for the inline-block element.
      - Apply display: none to the element with the class hidden-element.

```

---

# Task 2

## Requirements:

1. **Title**: Set the document title to "Text Alignment and Decoration Example".

2. **HTML Structure**:

```
   - Include the following elements in your HTML document:
     - A heading (<h1>) with the text "Text Alignment and Decoration Example".
     - Three container <div> elements with different classes to demonstrate text alignment and decoration:
       - A <div> with the class text-left containing a paragraph with the text "This text is aligned to the left".
       - A <div> with the class text-center containing a paragraph with the text "This text is centered".
       - A <div> with the class text-right containing a paragraph with the text "This text is aligned to the right".
       - A <div> with the class underline-text containing a paragraph with the text "This text has an underline".
       - A <div> with the class line-through-text containing a paragraph with the text "This text has a line through it".
       - Apply a border radius to the container element to create rounded corners.
```

---

```
   - CSS:
      - Apply text-align: left to the element with the class text-left.
      - Set padding and background color for the text-left element.
      - Apply text-align: center to the element with the class text-center.
      - Set padding and background color for the text-center element.
      - Apply text-align: right to the element with the class text-right.
      - Set padding and background color for the text-right element.
      - Apply text-decoration: underline to the element with the class underline-text.
      - Set padding and background color for the underline-text element.
      - Apply text-decoration: line-through to the element with the class line-through-text.
      - Set padding and background color for the line-through-text element.

```

# [Output should be like this](https://drive.google.com/file/d/18o3eOtcge5g1ADw1ePRn1dQlIoPT4-Yo/view?usp=sharing)

---

# Display: Flex

- Creates a flex container
- Allows for flexible alignment and distribution of space

```css
.flex-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

### Flex Direction

#### The flex-direction property defines the direction of the main axis.

`row (default)`<br>
`row-reverse`<br>
`column`<br>
`column-reverse`<br>

---

# CSS Flexbox

## Flexbox Container Properties

- `display: flex` - Defines a flex container
- `flex-direction` - Sets the main axis (row, column, row-reverse, column-reverse)
- `flex-wrap` - Controls wrapping of flex items (nowrap, wrap, wrap-reverse)
- `justify-content` - Aligns items along the main axis
- `align-items` - Aligns items along the cross axis
- `align-content` - Aligns flex lines when there's extra space in the cross-axis

```css
.flex-container {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  gap: 10px;
}
```

---

# Task 1

## Requirements:

1. **Title**: Set the document title to "Flexbox Example".

2. **HTML Structure**:

```
   - Include the following elements in your HTML document:
     - A heading (<h1>) with the text "Flexbox Example".
     - A container <div> with the class flex-container that contains the following child elements:
       - Three <div> elements with the class flex-item, each containing a paragraph with the text "Item 1", "Item 2", and "Item 3" respectively.

  - CSS:
      - Apply display: flex to the element with the class flex-container
      - Set justify-content: space-between to distribute space between the items.
      - Set align-items: center to center the items vertically within the container

```

---

# Task 2

## Requirements:

1. **Title**: Set the document title to "Flexbox Layout Example".

2. **HTML Structure**:

```
   - Include the following elements in your HTML document:
     - A heading (<h1>) with the text "Flexbox Layout Example".
     - A container <div> with the class flex-container that contains the following child elements:
       - Four <div> elements with the class flex-item, each containing a paragraph with the text "Box 1", "Box 2", "Box 3", and "Box 4" respectively.

  - CSS:
      - Apply display: flex to the element with the class flex-container.
      - Set flex-wrap: wrap to allow items to wrap onto multiple lines if necessary.
      - Set justify-content: space-around to distribute space evenly around the items.
      - Set align-items: flex-start to align items at the start of the container vertically.
      - Set gap: 10px to add spacing between the flex items.

```

# [Output should be like this](https://drive.google.com/file/d/1e9uAmNjAIfkrWsI2oDmITISFMg37OHia/view?usp=sharing)

---

# Display: Grid

- Creates a grid container
- Allows for complex two-dimensional layouts

```css
.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
}
```

---

# CSS Grid Layout

- Modern layout system in CSS
- Allows defining complex layouts with rows and columns

## Basic Concepts

### Grid Container

- Parent element with `display: grid;`
- Contains grid items

### Grid Items

- Children of grid container
- Positioned within grid cells

---

## Creating a Grid

### Defining Rows and Columns

```css
.container {
  display: grid;
  grid-template-rows: 100px 200px;
  grid-template-columns: 1fr 2fr 1fr;
}
```

```css
.container {
  display: grid;
  justify-items: center;
  align-items: center;
}
```

---

# Task 1

## Requirements:

1. **Title**: Set the document title to "CSS Grid Layout Example".

2. **HTML Structure**:

```
   - Include the following elements in your HTML document:
     - A heading (<h1>) with the text "CSS Grid Layout Example".
     - A container <div> with the class grid-container that contains the following child elements:
       - Nine <div> elements with the class grid-item, each containing a paragraph with the text "Item 1" through "Item 9".


  - CSS:
      - Apply display: grid to the element with the class grid-container.
      - Use grid-template-columns to create a grid with three equal-width columns
      - Use gap to set a gap of 10px between grid items.

```

---

# Task 2

## Requirements:

1. **Title**: Set the document title to "CSS Grid Layout Example".

2. **HTML Structure**:

```
   - Include the following elements in your HTML document:
     - A heading (<h1>) with the text "CSS Grid Layout Practice".
     - A container <div> with the class grid-container that contains the following child elements:
       - Eight <div> elements with the class grid-item, each containing a paragraph with the text "Box 1" through "Box 8".


  - CSS:
      - Apply display: grid to the element with the class grid-container.
      - Use grid-template-columns to create a grid with four equal-width columns.
      - Use grid-template-rows to create a grid with two equal-height rows.
      - Use gap: 20px to set a gap of 20px between grid items.
      - Set grid-auto-rows to 100px to specify the height of the rows.

```

# [Output should be like this](https://drive.google.com/file/d/1rDW4KgirQJqEqXH2pZL1IHRYlyqOohJR/view?usp=sharing)

---

# What is CSS Positioning?

- Determines how an element is positioned in a document
- Affects the layout of the page and the element's relation to other elements
- Controlled by the position property

## ## Common Position Values

1. `Static`
2. `Relative`
3. `Absolute`
4. `Fixed`
5. `Sticky`

---

# Position: Static

- Default positioning
- Element follows the normal document flow
- top, right, bottom, left, and z-index have no effect

```css
.static-element {
  position: static;
}
```

---

# Position: Relative

- Positioned relative to its normal position
- Still occupies space in normal flow
- Can use top, right, bottom, left to offset

```css
.relative-element {
  position: relative;
  top: 10px;
  left: 20px;
}
```

---

# Position: Absolute

- Removed from the normal document flow
- Positioned relative to nearest positioned ancestor (or initial containing block)
- Can use top, right, bottom, left for positioning

```css
.container {
  position: relative;
}

.absolute-element {
  position: absolute;
  top: 50px;
  right: 20px;
}
```

---

# Position: Fixed

- Removed from the normal document flow
- Positioned relative to the viewport
- Stays in place during scrolling

```css
.fixed-header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  height: 60px;
  background-color: #333;
}
```

---

# Position: Sticky

- Hybrid of relative and fixed positioning
- Behaves like relative positioning until it crosses a specified threshold
- Then behaves like fixed positioning

```css
.sticky-nav {
  position: sticky;
  top: 0;
  background-color: #f1f1f1;
  padding: 10px;
}
```

---

# Task 1

## Requirements:

1. **Title**: Set the document title to "CSS Positioning Example".

2. **HTML Structure**:

```
   - Include the following elements in your HTML document:
     - A heading (<h1>) with the text "CSS Positioning Practice".
     - A container <div> with the class `position-container` that contains:
       - A <p> element with the class `static-text` and the text "Static positioned text".
       - A <p> element with the class `relative-text` and the text "Relative positioned text".
       - A nested <div> within the container with the class `inner-container`, containing:
          - A <p> element with the class `absolute-text` and the text "Absolute positioned text".
          - A <div> element with the class `fixed-banner` containing a paragraph with the text "Fixed positioned banner".
          - A <p> element with the class `sticky-footer` and the text "Sticky positioned footer. Scroll to see it stick."

```

---

## CSS:

```
      - Apply position: static to the element with the class `static-text`.
      - Apply position: relative to the element with the class `relative-text`.
      - Use top: 20px and left: 20px to offset the element.
      - Apply position: relative to the `position-container` and position: absolute to the element with the class `absolute-text`.
      - Use top: 40px and left: 50px to position the element.
      - Apply position: fixed to the element with the class `fixed-banner`.
      - Use top: 0, left: 0, and right: 0 to fix the element at the top of the viewport.
      - Apply position: sticky to the element with the class `sticky-footer`.
      - Use bottom: 0 to specify the threshold for when the element should become sticky.

```

---

# Task 2

## Requirements:

1. **Title**: Set the document title to "CSS Positioning Example".

2. **HTML Structure**:

```
   - Include the following elements in your HTML document:
     - A heading (<h1>) with the text "CSS Positioning Example".
     - A container <div> with the class container that contains:
       - A <p> element with the class static-element and the text "This is a static positioned element".
       - A <p> element with the class relative-element and the text "This is a relative positioned element."
       - A nested <div> within the container with the class nested-container, containing:
          - A <p> element with the class absolute-element and the text "This is an absolute positioned element."
          - A <div> element with the class fixed-header containing a paragraph with the text "This is a fixed positioned element."
          - A <p> element with the class sticky-nav and the text "This is a sticky positioned element. Scroll to see it in action."

```

# [Output should be like this](https://drive.google.com/file/d/1z-lInzGHD3f40GaDTouM8EYNN9SktITu/view?usp=sharing)

---

## CSS:

```
      - Apply position: static to the element with the class static-element.
      - Apply position: relative to the element with the class relative-element.
      - Use top: 15px and left: 25px to offset the element.
      - Apply position: relative to the container and position: absolute to the element with the class absolute-element.
      - Use top: 30px and right: 40px to position the element.
      - Apply position: fixed to the element with the class fixed-header.
      - Use top: 0, left: 0, and right: 0 to fix the element at the top of the viewport.
      - Apply position: sticky to the element with the class sticky-nav.
      - Use top: 0 to specify the threshold for when the element should become sticky.

```

---

# Z-Index and Stacking Context

- Controls the stacking order of elements
- Only works on positioned elements (not static)
- Higher values appear on top of elements with lower values

```css
.back-element {
  position: absolute;
  z-index: 1;
}

.front-element {
  position: absolute;
  z-index: 2;
}
```

---

# Float Property

- Allows text and inline elements to wrap around it
- Removes the element from the normal document flow

## Float Values

- `left`: Floats the element to the left
- `right`: Floats the element to the right
- `none`: Default value, element does not float

```css
.float-left {
  float: left;
}

.float-right {
  float: right;
}

.no-float {
  float: none;
}
```

---

## Introduction to Transitions and Animations

CSS Transitions and Animations allow you to create dynamic effects and smooth transitions between states in your web designs.

```css
.box {
  width: 100px;
  height: 100px;
  background-color: blue;
  transition: background-color 0.5s ease;
}
.box:hover {
  background-color: red;
}
```

<v-click>
The ease keyword is a value for the transition-timing-function property. It defines the speed curve of a
transition effect. The speed curve determines how the intermediate values of the CSS properties being animated are calculated.

</v-click>

---

# Available Options for transition-timing-function

<v-click>

ease: Starts slow, then fast, then ends slow (default).

</v-click>

<v-click>

linear: Maintains a constant speed from start to end.

</v-click>

<v-click>

ease-in: Starts slow and speeds up towards the end.

</v-click>

<v-click>

ease-out: Starts fast and slows down towards the end.

</v-click>

<v-click>

ease-in-out: Starts slow, speeds up in the middle, then slows down at the end.

</v-click>

---

# CSS Animations

## Keyframes

- Keyframes define the intermediate steps in an animation sequence.

````md magic-move {lines: true}
```css
@keyframes animation-name {
  from {
    property: value;
  }
  to {
    property: value;
  }
}
```

```css
@keyframes changeColor {
  from {
    background-color: blue;
  }
  to {
    background-color: red;
  }
}
```

```css
.box {
  width: 100px;
  height: 100px;
  background-color: blue;
  animation: changeColor 2s infinite alternate;
}
@keyframes changeColor {
  from {
    background-color: blue;
  }
  to {
    background-color: red;
  }
}
```

```css
.box {
  width: 100px;
  height: 100px;
  background-color: blue;
}
.box:hover {
  animation: changeColor 2s infinite alternate;
}
@keyframes changeColor {
  from {
    background-color: blue;
  }
  to {
    background-color: red;
  }
}
```

```css
/* with percentages */
@keyframes animation-name {
  0% {
    property: value;
  }
  50% {
    property: value;
  }
  100% {
    property: value;
  }
}
```

```css
@keyframes pulse {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(1.5);
    opacity: 0.5;
  }
  100% {
    transform: scale(1);
    opacity: 1;
  }
}
```

```css
.box {
  width: 100px;
  height: 100px;
  background-color: blue;
  position: relative;
  margin: 50px auto;
  animation: pulse 2s infinite;
}
@keyframes pulse {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(1.5);
    opacity: 0.5;
  }
  100% {
    transform: scale(1);
    opacity: 1;
  }
}
```
````

---

# Task 1

## Requirements:

1. **Title**: Set the document title to "CSS Effects and Animations".

2. **HTML Structure**:

```
   - Include the following elements in your HTML document:
     - A heading (<h1>) with the text "CSS Effects and Animations".
     - A container <div> with the class `effect-container` that contains:
       - A <div> with the class `back-item` and a paragraph with the text "Background Item".
       - A <div> with the class `front-item` and a paragraph with the text "Front Item".
       - A <div> with the class `float-item` and a paragraph with the text "Floated Item".
       - A <div> with the class `no-float-item` and a paragraph with the text "Non-floated Item".
       - A <div> with the class `transition-box` containing a paragraph with the text "Hover over me!".
       - A <div> with the class `animation-box` containing a paragraph with the text "I pulse!".
```

---

```
   - CSS:
      - Apply the following styles to `.back-item`:
        - Set position: absolute.
        - Set z-index: 1 to ensure it's behind other elements.

      - Apply the following styles to `.front-item`:
        - Set position: absolute.
        - Set z-index: 2 to ensure it's in front of `.back-item`.

      - Apply the following styles to `.float-item`:
        - Set float: left to float the element to the left of its container.

      - Apply the following styles to `.no-float-item`:
        - Set float: none to ensure the element does not float.

      - Apply the following styles to `.transition-box`:
        - Set width: 150px, height: 150px, and background-color: blue.
        - Set transition: background-color 0.5s ease to create a smooth color transition on hover.
      - On hover, change the background-color to red.

      - Apply the following styles to `.animation-box`:
        - Set width: 100px, height: 100px, background-color: blue, and margin: 50px auto.
        - Set animation: pulse 2s infinite to create a pulsing effect.
      - Define the `pulse` keyframes:
        - At 0% and 100%, set transform: scale(1) and opacity: 1.
        - At 50%, set transform: scale(1.5) and opacity: 0.5.

```

---

# Task 2

## Requirements:

1. **Title**: Set the document title to "Positioning and Transitions Example".

2. **HTML Structure**:

```
   - Include the following elements in your HTML document:
     - A heading (<h1>) with the text "Positioning and Transitions Example".
     - A container <div> with the class `position-container` that contains:
       - A <div> with the class `relative-box` and a paragraph with the text "Relative Box".
       - A <div> with the class `absolute-box` and a paragraph with the text "Absolute Box".
       - A <div> with the class `fixed-box` and a paragraph with the text "Fixed Box".
       - A <div> with the class `transition-box` and a paragraph with the text "Transition Effect".
```

---

```
   - CSS:
      - Apply the following styles to `.relative-box`:
        - Set position: relative.
        - Set top: 20px and left: 20px to offset the element from its normal position.
        - Set background-color: lightblue and padding: 10px for visual clarity.

      - Apply the following styles to `.absolute-box`:
        - Set position: absolute.
        - Set top: 50px and right: 50px to position the element relative to its first positioned (non-static) ancestor.
        - Set background-color: lightcoral and padding: 10px for visual clarity.

      - Apply the following styles to `.fixed-box`:
        - Set position: fixed.
        - Set top: 0, left: 0, and right: 0 to fix the element to the top of the viewport.
        - Set background-color: lightgreen and padding: 10px for visual clarity.

      - Apply the following styles to `.transition-box`:
        - Set width: 150px, height: 150px, and background-color: blue.
        - Set transition: transform 0.5s ease-in-out to animate changes in transform property.
      - On hover, apply transform: scale(1.2) to enlarge the box and change background-color to orange.

```

---

# What are Media Queries?

Media queries are a key component of responsive web design, allowing you to apply different styles based on the characteristics of the device, such as its width, height, or orientation.

### Basic Syntax

```css
@media only screen and (max-width: 600px) {
  body {
    background-color: lightblue;
  }
  .navbar {
    display: none;
  }
  .container {
    display: flex;
    flex-direction: column;
  }
}
/* Resize the browser window to see the stylling when the width is 600px or less. */
```

---

# Design Replication Challenges

## In this module, you will practice your HTML and CSS skills by replicating provided designs.

- The goal is to create an exact copy of the given designs, paying close attention to details such as layout, colors, typography, and spacing.

[challenge 1](https://drive.google.com/uc?id=11yzKn76MafHgqQqE7J2LcJkqRPDptk2n)

[challenge 2](https://drive.google.com/file/d/1gWh-x_MaLLSeUexLSuQNtzo80u7sGnj_/view?usp=sharing)

[challenge 3](https://drive.google.com/file/d/1HL_uO46IU6buxRMXG6R8fcm3Lz7-jb8i/view?usp=sharing)

[challenge 4](https://drive.google.com/file/d/1mrwkOoZx5XAbgFOgg2zuFdNDnulEzjYZ/view?usp=sharing)

[challenge 5](https://drive.google.com/file/d/1pQYw1fa_0jNab8wERoRJqK1MhxW6w_BK/view?usp=sharing)

[challenge 6](https://drive.google.com/file/d/1DQW8lwxqNKBpIUJ7hsTDCHa8BbqPDPqa/view?usp=sharing)

[challenge 7](https://drive.google.com/file/d/1AAcLIadgSSiqf66ssEXkmhhTt97i-lJx/view?usp=sharing)

---

# Introduction to Tailwind CSS

## Benefits of using Tailwind CSS

<v-click>

# Setting Up Tailwind CSS

## Using CDN

</v-click>

<v-click>

## Default colors

</v-click>

<v-click>

```txt
Default colors
  white, black, red, green, blue, orange, yellow, purple, lime, emerald, teal, cyan, indigo, violet, fuchsia, pink, rose, sky, gray, slate, zinc, neutral, stone, amber
```

</v-click>

---

## Text Colors

<v-click>

```html
<p class="text-black">Tailwind css</p>
<p class="text-red-50">Tailwind css</p>
<p class="text-red-100">Tailwind css</p>
<p class="text-red-200">Tailwind css</p>
<p class="text-red-300">Tailwind css</p>
<p class="text-red-400">Tailwind css</p>
<p class="text-red-500">Tailwind css</p>
<p class="text-red-600">Tailwind css</p>
<p class="text-red-700">Tailwind css</p>
<p class="text-red-800">Tailwind css</p>
<p class="text-red-900">Tailwind css</p>
```

</v-click>

---

## Background Colors

<v-click>

```html
<div class="bg-slate-600">
  <p class="text-white">Tailwind css</p>
</div>
<div class="bg-zinc-400">
  <p class="text-white">Tailwind css</p>
</div>
<div class="bg-emerald-600">
  <p class="text-white">Tailwind css</p>
</div>
```

</v-click>

<v-click>

## Text Underline

</v-click>

<v-click>

```html
<p class="underline text-red-700 decoration-red-700">Tailwind css</p>
<p class="underline text-blue-700 decoration-blue-700">Tailwind css</p>
```

</v-click>

<v-click>

## Border Colors

</v-click>

<v-click>

```html
<input class="border-2 border-rose-500" />
<input class="border-2 border-blue-300" />
<input class="border-2 border-purple-900" />
<input class="border-2 border-yellow-500" />
```

</v-click>

---

## Divide Colors

<v-click>

```html
<div class="divide-y divide-blue-200">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 4</div>
  <div>Item 5</div>
  <div>Item 6</div>
</div>
```

</v-click>

<v-click>

## Outline Colors

</v-click>

<v-click>

```html
<button class="outline outline-blue-500">Button</button>
<button class="outline outline-purple-300">Button</button>
<button class="outline outline-gray-500">Button</button>
```

</v-click>

<v-click>

## Box Shadow

</v-click>

<v-click>

```html
<button class="bg-cyan-500 shadow-lg shadow-cyan-500">Button</button>
<button class="bg-blue-500 shadow-lg shadow-blue-500/50">Button</button>
<button class="bg-indigo-500 shadow-lg shadow-indigo-500/50">Button</button>
```

</v-click>

---

## Accent Colors

<v-click>

```html
<input type="checkbox" class="accent-purple-500" checked /> Option 1
<input type="checkbox" class="accent-pink-500" checked /> Option 2
<input type="checkbox" class="accent-red-300" checked /> Option 3
```

</v-click>

<v-click>

## Arbitrary Colors

</v-click>

<v-click>

```html
<div class="bg-[#427fab] h-10">Hello</div>
<div class="text-[#427fab] h-10">Hello</div>
<div class="border border-[#427fab] h-10">Hello</div>
```

</v-click>

---

<v-click>

## Margin

</v-click>

<v-click>

```txt
m-0 margin: 0px; m-1 margin: 0.25rem; /* 4px */
m-2 margin: 0.5rem; /* 8px */
m-3 margin: 0.75rem; /* 12px */
m-4 margin: 1rem; /* 16px */
m-5 margin: 1.25rem; /* 20px */ m-6 margin: 1.5rem; /* 24px */
```

</v-click>

<v-click>

## Padding

</v-click>

<v-click>

```txt
p-0       padding: 0px;
p-1       padding: 0.25rem; /* 4px */
p-2       padding: 0.5rem; /* 8px */
p-3       padding: 0.75rem; /* 12px */
p-4       padding: 1rem; /* 16px */
p-5       padding: 1.25rem; /* 20px */
p-6       padding: 1.5rem; /* 24px */
```

</v-click>

---

<v-click>

## Spacing

</v-click>

<v-click>

```txt
mx-0       margin-left: 0px; margin-right: 0px;
mx-1       margin-left: 0.25rem; /* 4px */ margin-right: 0.25rem; /* 4px */
mx-2       margin-left: 0.5rem; /* 8px */ margin-right: 0.5rem; /* 8px */
mx-3       margin-left: 0.75rem; /* 12px */ margin-right: 0.75rem; /* 12px */
mx-4       margin-left: 1rem; /* 16px */ margin-right: 1rem; /* 16px */
mx-5       margin-left: 1.25rem; /* 20px */ margin-right: 1.25rem; /* 20px */
mx-6       margin-left: 1.5rem; /* 24px */ margin-right: 1.5rem; /* 24px */
```

</v-click>

<v-click>

```txt
my-0       margin-top: 0px; margin-bottom: 0px;
my-1       margin-top: 0.25rem; /* 4px */ margin-bottom: 0.25rem; /* 4px */
my-2       margin-top: 0.5rem; /* 8px */ margin-bottom: 0.5rem; /* 8px */
my-3       margin-top: 0.75rem; /* 12px */ margin-bottom: 0.75rem; /* 12px */
my-4       margin-top: 1rem; /* 16px */ margin-bottom: 1rem; /* 16px */
my-5       margin-top: 1.25rem; /* 20px */ margin-bottom: 1.25rem; /* 20px */
my-6       margin-top: 1.5rem; /* 24px */
```

</v-click>

<v-click>

## Horizontal Spacing (space-x)

</v-click>

<v-click>

```txt
space-x-1     margin-right: 0.25rem; /* 4px */
space-x-2     margin-right: 0.5rem; /* 8px */
space-x-3     margin-right: 0.75rem; /* 12px */
space-x-4     margin-right: 1rem; /* 16px */
space-x-5     margin-right: 1.25rem; /* 20px */
space-x-6     margin-right: 1.5rem; /* 24px */
```

</v-click>

---

<v-click>

## Vertical Spacing (space-y)

</v-click>

<v-click>

```txt
space-y-1     margin-bottom: 0.25rem; /* 4px */
space-y-2     margin-bottom: 0.5rem; /* 8px */
space-y-3     margin-bottom: 0.75rem; /* 12px */
space-y-4     margin-bottom: 1rem; /* 16px */
space-y-5     margin-bottom: 1.25rem; /* 20px */
space-y-6     margin-bottom: 1.5rem; /* 24px */
```

</v-click>

<v-click>

## Font Family

</v-click>

<v-click>

```txt
  font-sans
  font-family: ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans", sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";

  font-serif
  font-family: ui-serif, Georgia, Cambria, "Times New Roman", Times, serif;

  font-mono
  font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
```

</v-click>

---

<v-click>

## Font Size

</v-click>

<v-click>

```txt
  text-xs	    font-size: 0.75rem; /* 12px */
  text-sm	    font-size: 0.875rem; /* 14px */
  text-base	  font-size: 1rem; /* 16px */
  text-lg	    font-size: 1.125rem; /* 18px */
  text-xl	    font-size: 1.25rem; /* 20px */
  text-2xl	  font-size: 1.5rem; /* 24px */
  text-3xl	  font-size: 1.875rem; /* 30px */
  text-4xl	  font-size: 2.25rem; /* 36px */
  text-5xl	  font-size: 3rem; /* 48px */
  text-6xl	  font-size: 3.75rem; /* 60px */
  text-7xl	  font-size: 4.5rem; /* 72px */
  text-8xl	  font-size: 6rem; /* 96px */
  text-9xl	  font-size: 8rem; /* 128px */
```

</v-click>

---

<v-click>

## Font Weight

</v-click>

<v-click>

```txt
  font-thin	      font-weight: 100;
  font-extralight	font-weight: 200;
  font-light	    font-weight: 300;
  font-normal	    font-weight: 400;
  font-medium	    font-weight: 500;
  font-semibold	  font-weight: 600;
  font-bold	      font-weight: 700;
  font-extrabold	font-weight: 800;
  font-black	    font-weight: 900;
```

</v-click>

---

<v-click>

## Letter Spacing

</v-click>

<v-click>

```txt
  tracking-tighter	letter-spacing: -0.05em;
  tracking-tight	  letter-spacing: -0.025em;
  tracking-normal	  letter-spacing: 0em;
  tracking-wide	    letter-spacing: 0.025em;
  tracking-wider	  letter-spacing: 0.05em;
  tracking-widest	  letter-spacing: 0.1em;
```

</v-click>

---

<v-click>

## Text Alignment

</v-click>

<v-click>

```txt
  text-left	    text-align: left;
  text-center	  text-align: center;
  text-right	  text-align: right;
  text-justify	text-align: justify;
```

</v-click>

---

<v-click>

## Text Transform

</v-click>

<v-click>

```txt
  uppercase	  text-transform: uppercase;
  lowercase	  text-transform: lowercase;
  capitalize	text-transform: capitalize;
  normal-case	text-transform: none;
```

</v-click>

---

<v-click>

## Text Decoration

</v-click>

<v-click>

```txt
  decoration-auto	      text-decoration-thickness: auto;
  decoration-from-font	text-decoration-thickness: from-font;
  decoration-0	        text-decoration-thickness: 0px;
  decoration-1	        text-decoration-thickness: 1px;
  decoration-2	        text-decoration-thickness: 2px;
  decoration-4	        text-decoration-thickness: 4px;
  decoration-8	        text-decoration-thickness: 8px;
```

</v-click>

---

<v-click>

## Position Classes

</v-click>

<v-click>

```txt
static	    position: static;
fixed	      position: fixed;
absolute	  position: absolute;
relative	  position: relative;
sticky	    position: sticky;
```

</v-click>

---

<v-click>

## Display Classes

</v-click>

<v-click>

```txt
block	            display: block;
inline-block	    display: inline-block;
inline	          display: inline;
flex	            display: flex;
inline-flex	      display: inline-flex;
table	            display: table;
grid	            display: grid;
inline-grid	      display: inline-grid;
contents	        display: contents;
list-item	        display: list-item;
hidden	          display: none;
```

</v-click>

---

<v-click>

## Z-Index

</v-click>

<v-click>

```txt
z-0	    z-index: 0;
z-10	  z-index: 10;
z-20	  z-index: 20;
z-30	  z-index: 30;
z-40	  z-index: 40;
z-50	  z-index: 50;
z-auto	z-index: auto;
```

</v-click>

---

<v-click>

## Float

</v-click>

<v-click>

```txt
float-right	  float: right;
float-left	  float: left;
float-none	  float: none;
```

</v-click>

---

<v-click>

## Background Size

</v-click>

<v-click>

```txt
bg-auto	    background-size: auto;
bg-cover	  background-size: cover;
bg-contain	background-size: contain;
```

</v-click>

---

<v-click>

## Background Repeat

</v-click>

<v-click>

```txt
bg-repeat	      background-repeat: repeat;
bg-no-repeat	  background-repeat: no-repeat;
bg-repeat-x	    background-repeat: repeat-x;
bg-repeat-y	    background-repeat: repeat-y;
bg-repeat-round	background-repeat: round;
bg-repeat-space	background-repeat: space;
```

</v-click>

---

<v-click>

## Breakpoint Classes

</v-click>

<v-click>

```txt
    sm	640px	  @media (min-width: 640px) { ... }
    md	768px	  @media (min-width: 768px) { ... }
    lg	1024px	@media (min-width: 1024px) { ... }
    xl	1280px	@media (min-width: 1280px) { ... }
    2xl	1536px	@media (min-width: 1536px) { ... }
```

</v-click>

---

# Getting Started with Bootstrap

<v-click>

**Include Bootstrap via CDN:**
</v-click>

<v-click>

```html
<link
  rel="stylesheet"
  href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css"
/>
<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.3/dist/umd/popper.min.js"></script>
```

</v-click>

---

# Project 1: Recreate a Website from Figma Design

`Your task for Project 1 is to create a comprehensive website based on a provided Figma design using HTML and Tailwind CSS. You will use the images provided and refer to the Figma link for detailed design specifications. The website should include the following components:`

```
1. Navigation Bar
2. Main Section
3. About Section
4. Product Section
5. Pricing Page
6. Footer
```

## Resources Provided:

[Figma Design](https://www.figma.com/design/ZEB6hIiCcJGzQpHcywNYgH/Landing-page-theme?node-id=0-1&t=vtFN1AnNR5QqH23C-0)

[Images](https://drive.google.com/drive/folders/1wRTdDsV0S6g4qPVjocizhm5b8SYWpacy)

---

# Project 2: Recreate a Website from Figma Design

`Your task for Project 2 is to create a comprehensive website based on a provided Figma design using HTML and Tailwind CSS. You will use the images provided and refer to the Figma link for detailed design specifications. The website should include the following components:`

```
1. Navigation Bar
2. Main Section
3. Popular Products
4. Services
5. About Us Section
6. Our Product Section
7. Testimonial
8. Footer
```

## Resources Provided:

[Figma Design](https://www.figma.com/design/geGbJQFx6ExChbFxKe4Bzx/theme_2_landing_page?t=QgP19TpKbpCB6fqf-0)

[Images](https://drive.google.com/drive/folders/1u9n93rNRpCd30U6Xw5h0in7xYgA512um)

---

# Challenge: Recreate a Website Using HTML and Tailwind CSS

<v-click>

Recreate the landing page as it is using HTML and Tailwind CSS. Pay close attention to the layout, styling, and responsiveness of the page.

[Theme 1](https://demo.olivethemes.com/gokyo-fse/).

[Theme 2](https://bazaar.ui-lib.com/furniture-2).

</v-click>

---

# Introduction to ChatGPT

<v-click>

## ChatGPT is like a very smart robot that talks with you. It can answer questions, tell stories, and help you learn coding by answering questions, providing code examples, and offering explanations.

</v-click>

<v-click>

## You can type messages to ChatGPT on a computer or a phone. It will read your message and then reply back to you, just like a friend.

</v-click>

---

# What is a Prompt?

<v-click>

### A prompt is a question or instruction that you give to ChatGPT to get a specific response.

</v-click>

<v-click>

# Example Prompt:

## **I get an error message in JavaScript. How do I fix it?** <hr>

</v-click>

<v-click>

## Generate a horizontal navigation bar with Tailwind CSS that includes evenly spaced links, white text, and underline effects on hover.

</v-click>

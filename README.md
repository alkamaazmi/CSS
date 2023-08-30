# CSS Interview Questions

### [What is CSS](https://www.w3schools.com/css/)

* CSS stands for Cascading Style Sheets.
* It is a style sheet language used for describing the presentation of a document written in a markup language such as HTML or XML.

### How can you integrate CSS on a web page?

There are three methods to integrate CSS on web pages:
* External CSS
* Internal CSS
* Inline CSS

1. External CSS : Create a separate `.css` file that contains all your CSS rules. To link the external stylesheet to your HTML document, use the `<link>` element in the `<head>` section of your HTML:

```html
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" type="text/css" href="styles.css">
</head>
<body>
    <!-- Your HTML content here -->
</body>
</html>
```

2. Internal Stylesheet : Internal CSS is defined inside an HTML document using `<style>` element in the `<head>` section of your HTML:

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        /* Your CSS rules here */
    </style>
</head>
<body>
    <!-- Your HTML content here -->
</body>
</html>
```
3. Inline Styles : Inline styles are applied directly to individual HTML elements using the `style` attribute. 

```html
<!DOCTYPE html>
<html>
<body>
    <p style="color: blue; font-size: 16px;">This is a blue text.</p>
</body>
</html>
```
### CSS Selectors

* CSS selectors are used to "find" (or select) the HTML elements you want to style.

#### The CSS element Selector

* The element selector selects HTML elements based on the element name.

```css
p {
  text-align: center;
  color: red;
}
```

#### The CSS id Selector

* The id selector uses the id attribute of an HTML element to select a specific element.

* The id of an element is unique within a page, so the id selector is used to select one unique element!

* To select an element with a specific id, write a hash (#) character, followed by the id of the element.

```css
#para1 {
  text-align: center;
  color: red;
}
```

#### The CSS class Selector

* The class selector selects HTML elements with a specific class attribute.

* To select elements with a specific class, write a period (.) character, followed by the class name.

```css
.center {
  text-align: center;
  color: red;
}
```
#### The CSS Universal Selector

* The universal selector (*) selects all HTML elements on the page.

```css
* {
  text-align: center;
  color: blue;
}
```

### CSS Colors

* Colors are specified using predefined color names, or RGB, HEX, HSL, RGBA, HSLA values.

#### CSS RGB Colors

* An RGB color value represents RED, GREEN, and BLUE light sources.
* rgb(red, green, blue)
* Each parameter (red, green, and blue) defines the intensity of the color between 0 and 255.

#### RGBA Value

* RGBA color values are an extension of RGB color values with an alpha channel - which specifies the opacity for a color.
* rgba(red, green, blue, alpha)
* The alpha parameter is a number between 0.0 (fully transparent) and 1.0 (not transparent at all)

#### CSS HEX Colors

* A hexadecimal color is specified with: #RRGGBB, where the RR (red), GG (green) and BB (blue) hexadecimal integers specify the components of the color

#### CSS HSL Colors

* HSL stands for hue, saturation, and lightness.
* Hue is a degree on the color wheel from 0 to 360. 0 is red, 120 is green, and 240 is blue.
* Saturation is a percentage value. 0% means a shade of gray, and 100% is the full color.
* Lightness is also a percentage. 0% is black, 50% is neither light or dark, 100% is white.

#### HSLA Value

* HSLA color values are an extension of HSL color values with an alpha channel - which specifies the opacity for a color.

### CSS Backgrounds

* The CSS background properties are used to add background effects for elements.

#### CSS background-color

* The background-color property specifies the background color of an element.

```css
body {
  background-color: lightblue;
}
```
#### CSS background-image

* The background-image property specifies an image to use as the background of an element.

* By default, the image is repeated so it covers the entire element.

```css
body {
  background-image: url("paper.gif");
}
```

#### CSS background-repeat

* The background-repeat CSS property sets how background images are repeated.

```
background-repeat: repeat-x;
background-repeat: repeat-y;
background-repeat: repeat;
background-repeat: space;
background-repeat: round;
background-repeat: no-repeat;
```
#### CSS background-position

* The background-position property is used to specify the position of the background image.

#### CSS background-attachment

* The background-attachment property specifies whether the background image should scroll or be fixed (will not scroll with the rest of the page)

#### CSS background - Shorthand property

When using the shorthand property the order of the property values is:
* background-color
* background-image
* background-repeat
* background-attachment
* background-position

### CSS Box Model

* Everything in CSS has a box around it.The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content.

![](data:image/png;base64,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)

* Content - The content of the box, where text and images appear.
* Padding -This is the space between the content and the border.
* Border - This is the line that surrounds the content and padding.
* Margin - This is the space between the border of the element and the surrounding elements.


#### Margin - Shorthand Property
The margin property is a shorthand property for the following individual margin properties:

* margin-top
* margin-right
* margin-bottom
* margin-left

#### If the margin property has four values:

`margin: 25px 50px 75px 100px;`
* top margin is 25px
* right margin is 50px
* bottom margin is 75px
* left margin is 100px

#### All the margin properties can have the following values:

* auto - the browser calculates the margin.
* length - specifies a margin in px, pt, cm, etc.
* % - specifies a margin in % of the width of the containing element.
* inherit - specifies that the margin should be inherited from the parent element.

#### The auto Value

* You can set the margin property to `auto` to horizontally center the element within its container.
* The element will then take up the specified width, and the remaining space will be split equally between the left and right margins.

#### CSS Margin Collapse

Top and bottom margins of elements are sometimes collapsed into a single margin that is equal to the largest of the two margins.

#### CSS Border - Shorthand Property

The `border` property is a shorthand property for the following individual border properties:

* border-width
* border-style (required)
* border-color

```css
p {
  border: 5px solid red;
}
```

### Important : 
When you set the width and height properties of an element with CSS, you just set the width and height of the content area. To calculate the full size of an element, you must also add padding, borders and margins.

### CSS Box Sizing

The CSS `box-sizing` property allows us to include the padding and border in an element's total width and height.

If you set `box-sizing: border-box;` on an element, padding and border are included in the width and height

### The display Property

* The CSS `display` property is used to control how an HTML element is rendered on a web page.

* Every HTML element has a default display value depending on what type of element it is. The default display value for most elements is `block` or `inline`.

Here are some of the most common values of the display property:

* `display: block;` element always starts on a new line and takes up the full width available.
* `display: inline` element does not start on a new line and only takes up as much width as necessary. Setting height, width, margins and padding is not allowed.
* `display: inline-block` similar to inline but setting height, width, margins and padding is allowed.
* `display: none;` CSS property specifies that an element should not be displayed. The element will not take up any space in the document, and it will not be accessible to users.
* `display: flex;` This value makes the element a flex container,The children of the flex container become flex items,  and the container provides a flexible layout model for arranging these items  along a main axis and a cross axis.
* `display: grid;`  create a grid container. The container's direct children become grid items, and you can define rows and columns to arrange these items in a grid-like structure.

### The position Property

The position CSS property sets how an element is positioned in a document. The top, right, bottom, and left properties determine the final location of positioned elements. It can have one of five values:
* static
* relative
* fixed
* absolute
* sticky

* `position: static;` The element is positioned according to the normal flow of the document. The top, right, bottom, left, and z-index properties have no effect. This is the default value. 

* `position: relative;` The element is positioned according to the normal flow of the document, and then offset relative to itself based on the values of top, right, bottom, and left.The offset does not affect the position of any other elements.

* `position: absolute;` The element is removed from the normal document flow, and no space is created for the element in the page layout.  The element is positioned relative to its closest positioned ancestor (if any). However if an absolute positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling.Its final position is determined by the values of top, right, bottom, and left.

* `position: fixed;` The element is removed from the normal document flow, and no space is created for the element in the page layout.  The element is positioned fixed to the viewport, which means it always stays in the same place even if the page is scrolled.

* `position: sticky;` An element with position: sticky; is positioned based on the user's scroll position.
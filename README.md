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
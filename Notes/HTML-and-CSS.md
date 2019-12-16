# HTML and CSS
## HTML
* gives web pages structure and content
* introductory terms:
  * elements: designators that define the structure and content of objects within a page
  Ex: ```<h1>``` - ```<h6>``` headings, paragraph ```<p>``` element, anchor ```<a>```
element, ```<div>```, ```<span>```, etc.
  * tags: designating the beginning and end of an element, they enclose an element's
  content. Ex: opening anchor tag ```<a>```, closing anchor tag ```</a>```
  * attributes: properties used to provide additional information about an element.
  Ex: ```id``` attribute identifies an element, ```href``` attribute hyperlink references
  a resource, ```class``` attribute classifies an element, etc.
    * declared within an element's opening tag after element name
    i.e. ```<a href="http://launchschool.com"```
    * consist of a name and value i.e. ```href="http://launchschool.com/"```

### Setting Up the HTML Document Structure
* HTML documents are plain text documents saved with a .html file extension
* All HTML documents have a required structure that includes the ```<!DOCTYPE html>```
declaration and the ```<html>```, ```<head>```, and ```body``` elements.
  * ```<!DOCTYPE html>``` declaration specifies the version of html on the page
  * ```head``` inside of ```<html>``` tag contains non visible metadata
  * visible content goes inside of ```body``` tags

## CSS
* changes the appearance of content on a website  
* introductory terms:
  * selectors: designate exactly which elements styles are applied to. Selectors
  target elements by the type of element such as all paragraph or h1 elements, and
  by attribute values such as an ```id``` or ```class``` value. Selectors are followed
  by curly brackets in which styles are specified. Ex: selector targeting all paragraph elements: ``` p {} ```
  * properties: held within the curly brackets immediately after a selector, properties
  specify the styles that will be applied to the selected elements. Property names
  are followed by a colon and the values for that property.
  Ex: ```background```, ```color```, ```font-size```,```height```, ```width```, etc.
  * values: determine the behavior of a property. Identified as the text between the
  colon and semicolon following a property name. Ex: a color property with a value of orange:
```css
p {
  color: orange;
}
```

### Working With Selectors
* The most common selectors in CSS are the type, class, and id selectors though many more
advanced selectors exist.
  * type selectors are the least specific selector as they target any and all elements of
  a certain type
  * class selectors are more specific than type selectors. They target elements of any type
  that have a specific value for the class attribute. Class selectors are preceded by a period.
  Ex: selector targeting all elements with a class attribute value of "awesome
```css
.awesome { ... }
```
  * id selectors are the most specific of the selectors. They target one element based
  on the value of its id property which must be unique across all elements. Id selectors
  are preceded by a #. Ex: id selector targeting the element with id value "cristian":
```css
#cristian { ... }
```

### Referencing CSS
In order for an HTML page to render CSS styles, the CSS styles must be referenced in the HTML file.
The preferred method of referencing CSS styles in an HTML file is to put our CSS styles in a single
external file(ending in a .css extension) and reference this file from within the HTML document.

* external CSS files should be referenced within a ```link``` element inside of the ```head``` element
  * ```rel``` attribute should have a value of "stylesheet" to define the relationship between the HMTL file and CSS stylesheet
  * ```href``` attribute should provide the path to the CSS stylesheet.
  * Ex:
```html
<head>
  <link rel="stylesheet" href="main.css">
</head>
```

### Using CSS Resets
Browsers differ on how they render HTML elements. In order to ensure the consistency of a website
across all browsers, we can use CSS resets. Different CSS reset techniques exist which manipulate
margins, padding, etc. so that all browsers display elements from a common CSS starting point.
Because CSS cascades from top to bottom, resets must be applied at the very top of a stylesheet.

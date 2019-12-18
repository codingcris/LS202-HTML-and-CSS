# Getting to Know HTML
  These are my personal notes from part 2 of Shay Howe's Learn to Code: HTML & CSS tutorial.
  You can view the tutorial [here](https://learn.shayhowe.com/html-css/getting-to-know-html/)

## Semantics Overview
**semantics:** in HTML, semantics involves giving content value based on the type of element
used to hold the content. Using semantic elements makes code easier to manage and understand
as well as allowing screen readers, search engines, and other devices to accurately interpret our page.
Examples of semantic elements include ```header```, ```footer```, and ```paragraph``` elements among others.
Non semantic elements include ```div``` and ```span``` elements among others.

## Using Text Based Elements

### Headings
* Heading elements come in six different rankings ```<h1>``` - ```<h6>``` and serve to
divide and bring hierarchy to a page's content.
* Heading elements should be used in an order that is relevant to the page's content i.e.
an ```<h1>``` element should be used for the content's primary heading and subsequent headings
should use the subsequent heading elements.
* Search engines use heading elements to index and determine the content on a page.
* Heading elements are semantic elements

### Paragraphs
Paragraph elements are defined with the ```<p>``` element and serve to add long
textual content to a page. Paragraphs are semantic elements.

### Bold Text
* bold text can be achieved through the use of the  ```<strong>``` and ```<b>``` elements.
* ```<strong>``` has semantic value and should be used for text of strong importance.
* ```<b>``` may be used for the stylistic purpose of making text bold.

### Italicized Text
* Italicized text can be achieved through the use of the ```<em>``` and ```<i>``` elements.
* ```<em>``` has semantic value and signifies text with stressed emphasis
* ```<i>``` has semantic value used to convey text in an alternative voice ex: foreign words, technical terms, typographically italicized text

## Building Structure
Before the introduction of structural elements, a web page was given structure through divisions
i.e. the ```<div>``` element. Because ```<div>``` elements are non semantic, it was difficult to
interpret the intention of divisions. Today it is preferred that we use semantic structurally based elements such as ```<header>```, ```<nav>```, ```<article>```, etc. to give structure to a page.

### Identifying Divisions & Spans
* ```<div>``` and ```<span>``` elements act as containers for styling purposes. They hold no semantic value.
    * Usually given an ```id``` or ```class``` value. This value should reflect the content within the element.
    * Useful for applying styles to a contained group of elements

### Header
The ```<header>``` element identifies the top of a page, article, or section of a page. It may contain a heading, introductory text, and even navigation. The ```<header>``` element falls within the ```<body>``` element. It should not be confused with the ```<head>``` element which is used to contain metadata and is not visible on a page or the heading elements which are text based rather than structural elements.

### Navigation
The ```<nav>``` element is used to identify a group of site navigational links such as a website directory, table of contents, previous/next links, etc. Miscellaneous links should be wrapped within an anchor (```<a>```) element and not within a ```<nav>``` element.

### Article
The ```<article>``` element should contain content that is independently meaningful. If this content were replicated somewhere else, the content should make sense outside of the original web page. Ex: blog posts, user submitted content, news articles, etc.

### Section
The ```<section>``` element is used to thematically divide content. All content within a section should be related. This element provides structure and hierarchy to a page.

### Aside
The ```<aside>``` element holds content such as inserts or brief explanations that is tangentially related to the content surrounding it.

### Footer
The ```<footer>``` element identifies the end of a section in a page. It may hold relevant closing information.

## Creating Hyperlinks
* Hyperlinks can be added to a page using the anchor(```<a>```) element. The ```href``` attribute specifies the path for the link.
    * a relative path can be used if the link leads to a page on the same website. In this case we point to the html file for that page. Ex: a link to the about page of the same website. 
    
        ```html
        <a href="about.html">About Me</a>
        ```
    * an absolute path must be used if the link leads to another website. Ex: a link to google

        ```html
        <a href="http://www.google.com">Google</a>
        ```
    * we can link to a specific element on the same page by using the value of its ```id``` attribute prepended by #. Ex:

        ```html
        <body id="top">
          <a href="top">Back to top</a>
        </body>
        ```

    * if link should open in a new tab/window set the ```target``` attribute of the anchor element to a value of ```"_blank"```

* Email adresses can be linked to within an anchor element.
    * href attribute value must start with ```mailto:``` followed by the email address
    * subject, body text, and other fields may be populated by setting the values of different query parameters. Ex: 

        ```html
        <a href="mailto:code@awesome.com?subject=Github">Email<\a>
        ```
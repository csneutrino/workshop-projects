# Summary of Day 5

> By Gaurav Shah

## CSS Introduction

- CSS stands for Cascading Style Sheets.
- CSS describes how HTML elements are to be displayed on screen.
- CSS is used to define styles for your web pages, including the design, layout and variations in display for different devices and screen sizes.
  <br/>
  <br/>

## CSS syntax and linking

<br/>

![CSS Syntax](https://www.w3schools.com/css/img_selector.gif)

Above is the syntax of CSS (Internal and External).

Selector is used to point to the element in the HTML document you want to style.

Declaration Box consists of properties and values for styling. Multiple properties are seperated by a semicolon '`;`'. Property defines the type of CSS styling for the selected element and value is set.

Internal CSS is enclosed within `<style></style>` tag, inside the head element.
External CSS is linked to the HTML document by using `<link></link>` tag.

However in inline CSS. '`style`' attribute is used within the element for styling.

![Inline CSS](https://lucidar.me/en/web-dev-class/files/en-inline-css-syntax.png)

```HTML
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
        <link rel="stylesheet" href="link to CSS file"> <!-- Linking External CSS file -->
        <style>
            <!-- Adding Internal CSS -->
            p{
                color:red;
            }
        </style>
    </head>
    <body>
        <p style="color: red">Hello World</p> <!-- Inline CSS Example -->
    </body>
    </html>
```

Inline CSS and Internal CSS are not preferred much as they make HTML document too big and confusing. So using external CSS file is reccomended.

Priroty of CSS files is Inline CSS has higher priority over Internal CSS have higher priority over External CSS.
(i.e Inline CSS > Internal CSS > External CSS).

Higher priority can overwrite lower priority CSS style if there are confliciting elements and property styles.
<br/>
<br/>

## CSS Selectors

<br/>
Selectors are used to point to the element in the HTML document you want to style.

Types of CSS selectors:

- Simple Selectors (tag, id, class).
- Combinator selectors (select elements based on a specific relationship between them)
- Pseudo-class selectors (select elements based on a certain state)
- Pseudo-elements selectors (select and style a part of an element)
- Attribute selectors (select elements based on an attribute or attribute value)

Simple selectors are tags, classes and id.

Tags are reffered by simply tagnames on CSS file.

```CSS
p{ color: red; font-size: 30px}
```

For example, paragraph element in HTML document is referred by `p` tag only.
However, using only tagname to select HTML elements can produce unexpected results. So, Classes and IDs should be used.

Class is reffered by using full-stop sign '`.`' .

```HTML
<body>
    <p class="first-class">
        Hello World
    </p>
</body>
```

```CSS
.first-class{
    color:red;
    font-size:30px;
}
```

Here, a paragraph element with class name 'first-class' exists in HTML document.So to select the class, we use '`.first-class`' in CSS file.
Multiple elements can have same class and one element can also have multiple classes.
Concept of class is to add appriopriate styling to same type of elements in the design layout of the page.
Using multiple classes in a single element is done by simply seperating two classes name with a space.

```HTML
<p class="first-class border-class">Hello World</p>
```

Here, paragraph elements has two classes `first-class` and `border-class` seperated by space. Both of the classes apply their own styling on the element but if there are same style properties then the properties appearing later in the CSS document takes over the previous one.

IDs are reffered in the CSS document by '`#`' number sign.

```HTML
<body>
    <p id="element-1">
        Hello World
    </p>
</body>
```

```CSS
#element-1{
    color:red;
    font-size:30px;
}
```

Here, paragraph element has `element-1` ID and it is selected by number sign `#` in CSS document.
One element can only have one unique ID.
IDs have higher priority over classes. Therefore ID are used for applying unique styles to the elements.

Priority order of ID is over classes and classes is over tagname. (i.e ID > class > tagname).

## Colors and Measurement units

Color in HTML and CSS are taken in multiple formats.

<details>
    <summary>
      Color name
    </summary>

    Color pallet can be accessed by their itself. for example, red for red color and so on.

But the names of color are limited so other approach are required for more complex shades.

</details>
<details>
    <summary>
        RGB
    </summary>

    RGB (Red Green Blue) uses three values of RGB colors each ranging form 0-255. Different combination of these numbers create colors. for example, RGB(0,0,0) is for black color.

</details>
<details>
    <summary>
        HEX
    </summary>

    HEXadecimal color coding is in format of number sign `#` follwed by six characters of hexadecimal number system. for example, #ffffff is HEX color code for white color.

</details>
<details>
    <summary>
        HSL
    </summary>

    HSL (Hue Saturation Light) uses three different values of HSL in percentage from 0% to 100%. For example, HSL(0%,0%,0%) is HSL color code for black.

</details>
<details>
    <summary>
    Opacity
    </summary>

    Opacity of colors can be changed by the different color code itself excluding 'color name'.
    In RGB and HSL, 'a' is introduced for controlling opacity. Value of `a` ranges from 0(transparent) to 1(opaque).

    for example, RGBa(255,255,255,0.5), HSLa(0%,0%,0%,0.5).
    For HEX color code, extra two characters are added after the six characters. for example, #00000000 (total eight).

</details>  
   <br/>

Measurement units in CSS:
px, rem, em, vh, vw are used in CSS. But SI units can also be used for this purpose.
<br/>

<details>
  <summary>
  EM
  </summary>
    Relative to the font-size of the element (2em means 2 times the size of the current font)	
    
```HTML
    <!DOCTYPE html>
    <html>
    <head>
    <style>
    p {
        font-size: 16px;
        line-height: 2em;
    }

    div {
    font-size: 30px;
    border: 1px solid black;
    }

    span {
    font-size: 0.5em;
    }
    </style>

    </head>
    <body>

    <p>These paragraphs have a calculated line-height of: 2x16px = 32px.</p>
    <p>These paragraphs have a calculated line-height of: 2x16px = 32px.</p>
    <p>These paragraphs have a calculated line-height of: 2x16px = 32px.</p>
    <div>The font-size of the div element is set to 30px. <span>The span element inside the div element has a font-size of 0.5em, which equals to 0.5x30 = 15px</span>.</div>

    </body>
    </html>

````
</details>

<details>
<summary>
    REM
</summary>
    <br/>
    Relative to font-size of the root element

```HTML
    <!DOCTYPE html>
    <html>
    <head>
    <style>
    html {
    font-size:16px;
    }

    div {
    font-size: 3rem;
    border: 1px solid black;
    }

    #top-div {
    font-size: 2rem;
    border: 1px solid red;
    }
    </style>
    </head>
    <body>

    <p>The font-size of this document is 16px.</p>

    <div id="top-div">
    The font-size of this div element is 2rem, which translates to 2 x the browser's font size.
    <div>The font-size of this div element is 3rem. It also shows that it does not inherit from its parent element font size.</div>
    </div>

    <p>The rem unit sets the font-size relative to the browsers base font-size, and will not inherit from its parents.</p>

    </body>
    </html>
````

</details>

<details>
    <summary>
        VW
    </summary>
        Relative to 1% of the width of the viewport. Viewport = the browser window size. If the viewport is 50cm wide, 1vw = 0.5cm.

```HTML
    <!DOCTYPE html>
    <html>
    <head>
    <style>
    h1 {
    font-size: 20vw;
    }
    </style>
    </head>
    <body>

    <h1>Hello</h1>

    <p>Resize the width of the browser window to see how the font-size of h1 changes.</p>
    <p>1vh = 1% of viewport height.</p>
    <p>The vw unit is not supported in IE8 and earlier.</p>

    </body>
    </html>
```

</details>

<details>
    <summary>
        VH
    </summary>
  Relative to 1% of the height of the viewport. Viewport = the browser window size. If the viewport is 50cm high, 1vh = 0.5cm.

```HTML

    <!DOCTYPE html>
    <html>
    <head>
    <style>
    h1 {
    font-size: 20vh;
    }
    </style>
    </head>
    <body>
    <h1>Hello</h1>
    <p>Resize the height of the browser window to see how the font-size of h1 changes.</p>
    <p>1vh = 1% of viewport height.</p>
    <p>The vh unit is not supported in IE8 and earlier.</p>
    </body>
    </html>
```

</details>
<br/>
<br/>

## CSS Background

<br/>

The CSS background properties are used to add background effects for elements.

- background-color
- background-image
- background-repeat
- background-attachment
- background-position
- background (shorthand property)
  <br/>
  <br/>

## CSS Borders

<br/>

The CSS border properties allow you to specify the style, width, and color of an element's border.

```HTML
   <!DOCTYPE html>
   <html>
   <head>
   <style>
   p {
   border: 5px solid red;
   }
   </style>
   </head>
   <body>

   <h2>The border Property</h2>

   <p>This property is a shorthand property for border-width, border-style, and border-color.</p>

   </body>
   </html>
```

<br/>
<br/>

## CSS Margins and Paddings

<br/>
    Margins are used to create space around elements, outside of any defined borders.
<details>
    <summary>
            Margin Properties
    </summary>

- margin-top
- margin-right
- margin-bottom
- margin-left

</details>

<br/>
Padding is used to create space around an element's content, inside of any defined borders.

<details>
    <summary>
            Padding Properties
    </summary>

- padding-top
- padding-right
- padding-bottom
- padding-left

</details>
<br/>
<br/>

## CSS Box Model

In CSS, the term "box model" is used when talking about design and layout.

The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content. The image below illustrates the box model:
<br/>

![Box Model](https://www.kasandbox.org/programming-images/misc/boxmodel.png)

```HTML
    <!DOCTYPE html>
    <html>
    <head>
    <style>
    div {
    background-color: lightgrey;
    width: 300px;
    border: 15px solid green;
    padding: 50px;
    margin: 20px;
    }
    </style>
    </head>
    <body>

    <h2>Demonstrating the Box Model</h2>

    <p>The CSS box model is essentially a box that wraps around every HTML element. It consists of: borders, padding, margins, and the actual content.</p>

    <div>This text is the content of the box. We have added a 50px padding, 20px margin and a 15px green border. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</div>

    </body>
    </html>

```

Here, total width of div is equal to 300px + 15px * 2(border) + 20px *2(margin) + 50px \*2(padding).
<br/>
<br/>

## CSS Links

<br/>
Links can be styled with any CSS property (e.g. color, font-family, background, etc.).
In addition, links can be styled differently depending on what state they are in.
The four links states are:

- a:link - a normal, unvisited link
- a:visited - a link the user has visited
- a:hover - a link when the user mouses over it
- a:active - a link the moment it is clicked

```HTML
    <!DOCTYPE html>
    <html>
    <head>
    <style>
    /* unvisited link */
    a:link {
    color: red;
    }

    /* visited link */
    a:visited {
    color: green;
    }

    /* mouse over link */
    a:hover {
    color: hotpink;
    }

    /* selected link */
    a:active {
    color: blue;
    }
    </style>
    </head>
    <body>

    <h2>CSS Links</h2>
    <p><b><a href="default.asp" target="_blank">This is a link</a></b></p>
    <p><b>Note:</b> a:hover MUST come after a:link and a:visited in the CSS definition in order to be effective.</p>
    <p><b>Note:</b> a:active MUST come after a:hover in the CSS definition in order to be effective.</p>

    </body>
    </html>

```

<br/>
<br/>

## CSS Lists

In HTML, there are two main types of lists:

unordered lists (`<ul>`) - the list items are marked with bullets
ordered lists (`<ol>`) - the list items are marked with numbers or letters
The CSS list properties allow you to:

- Set different list item markers for ordered lists
- Set different list item markers for unordered lists
- Set an image as the list item marker
- Add background colors to lists and list items

```HTML
    <!DOCTYPE html>
    <html>
    <head>
    <style>
    ul.a {
    list-style-type: circle;
    }

    ul.b {
    list-style-type: square;
    }

    ol.c {
    list-style-type: upper-roman;
    }

    ol.d {
    list-style-type: lower-alpha;
    }
    </style>
    </head>
    <body>

    <h2>Lists</h2>
    <p>Example of unordered lists:</p>
    <ul class="a">
    <li>Coffee</li>
    <li>Tea</li>
    <li>Coca Cola</li>
    </ul>

    <ul class="b">
    <li>Coffee</li>
    <li>Tea</li>
    <li>Coca Cola</li>
    </ul>

    <p>Example of ordered lists:</p>
    <ol class="c">
    <li>Coffee</li>
    <li>Tea</li>
    <li>Coca Cola</li>
    </ol>

    <ol class="d">
    <li>Coffee</li>
    <li>Tea</li>
    <li>Coca Cola</li>
    </ol>

    </body>
    </html>

```

<br/>
<br/>

## CSS Display

The display property is the most important CSS property for controlling layout.

The display property specifies if/how an element is displayed.

Every HTML element has a default display value depending on what type of element it is. The default display value for most elements is block or inline.

<details>
<summary>
    Block-level Elements
</summary>

![Block-level Elements](https://static.javatpoint.com/htmlpages/images/html-block-level-and-inline-elements.png)

A block-level element always starts on a new line and takes up the full width available (stretches out to the left and right as far as it can).

Examples of block-level elements:

```HTML
    <div>
    <h1> - <h6>
    <p>
    <form>
    <header>
    <footer>
    <section>
```

</details>

<details>
<summary>Inline Elemets</summary>

![Inline Elements](https://media.geeksforgeeks.org/wp-content/uploads/span_js_after.jpg)

An inline element does not start on a new line and only takes up as much width as necessary.

Examples of inline elements:

```HTML
<span>
<a>
<img>
```

</details>

<details>
<summary>
Inline-Block
</summary>
Compared to display: inline, the major difference is that display: inline-block allows to set a width and height on the element.

Also, with display: inline-block, the top and bottom margins/paddings are respected, but with display: inline they are not.

Compared to display: block, the major difference is that display: inline-block does not add a line-break after the element, so the element can sit next to other elements.

```HTML
    <!DOCTYPE html>
    <html>
    <head>
    <style>
    span.a {
    display: inline; /* the default for span */
    width: 100px;
    height: 100px;
    padding: 5px;
    border: 1px solid blue;
    background-color: yellow;
    }

    span.b {
    display: inline-block;
    width: 100px;
    height: 100px;
    padding: 5px;
    border: 1px solid blue;
    background-color: yellow;
    }

    span.c {
    display: block;
    width: 100px;
    height: 100px;
    padding: 5px;
    border: 1px solid blue;
    background-color: yellow;
    }
    </style>
    </head>
    <body>

    <h1>The display Property</h1>

    <h2>display: inline</h2>
    <div>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum consequat scelerisque elit sit amet consequat. Aliquam erat volutpat. <span class="a">Aliquam</span> <span class="a">venenatis</span> gravida nisl sit amet facilisis. Nullam cursus fermentum velit sed laoreet. </div>

    <h2>display: inline-block</h2>
    <div>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum consequat scelerisque elit sit amet consequat. Aliquam erat volutpat. <span class="b">Aliquam</span> <span class="b">venenatis</span> gravida nisl sit amet facilisis. Nullam cursus fermentum velit sed laoreet. </div>

    <h2>display: block</h2>
    <div>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum consequat scelerisque elit sit amet consequat. Aliquam erat volutpat. <span class="c">Aliquam</span> <span class="c">venenatis</span> gravida nisl sit amet facilisis. Nullam cursus fermentum velit sed laoreet. </div>

    </body>
    </html>

```

</details>
<br/>
<br/>

## CSS Positions

<br/>
The position property specifies the type of positioning method used for an element (static, relative, fixed, absolute or sticky).
<br/>
<br/>

### The position Property

<br/>

The `position` property specifies the type of positioning method used for an element.

There are five different `position` values:

<details>
<summary>
static
</summary>
HTML elements are positioned static by default.

Static positioned elements are not affected by the top, bottom, left, and right properties.

An element with position: static; is not positioned in any special way; it is always positioned according to the normal flow of the page:

```HTML
    <!DOCTYPE html>
    <html>
    <head>
    <style>
    div.static {
    position: static;
    border: 3px solid #73AD21;
    }
    </style>
    </head>
    <body>

    <h2>position: static;</h2>

    <p>An element with position: static; is not positioned in any special way; it is
    always positioned according to the normal flow of the page:</p>

    <div class="static">
    This div element has position: static;
    </div>

    </body>
    </html>
```

</details>

<details>
<summary>
relative
</summary>
An element with position: relative; is positioned relative to its normal position.

Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position. Other content will not be adjusted to fit into any gap left by the element.

```HTML
    <!DOCTYPE html>
    <html>
    <head>
    <style>
    div.relative {
    position: relative;
    left: 30px;
    border: 3px solid #73AD21;
    }
    </style>
    </head>
    <body>

    <h2>position: relative;</h2>

    <p>An element with position: relative; is positioned relative to its normal position:</p>

    <div class="relative">
    This div element has position: relative;
    </div>

    </body>
    </html>

```

</details>

<details>
<summary>
fixed
</summary>
An element with position: fixed; is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled. The top, right, bottom, and left properties are used to position the element.

A fixed element does not leave a gap in the page where it would normally have been located.

```HTML
    <!DOCTYPE html>
    <html>
    <head>
    <style>
    div.fixed {
    position: fixed;
    bottom: 0;
    right: 0;
    width: 300px;
    border: 3px solid #73AD21;
    }
    </style>
    </head>
    <body>

    <h2>position: fixed;</h2>

    <p>An element with position: fixed; is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled:</p>

    <div class="fixed">
    This div element has position: fixed;
    </div>

    </body>
    </html>

```

</details>

<details>
<summary>
absolute
</summary>
An element with position: absolute; is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed).

However; if an absolute positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling.

<b>Note</b> : A "positioned" element is one whose position is anything except static.

```HTML
    <!DOCTYPE html>
    <html>
    <head>
    <style>
    div.relative {
    position: relative;
    width: 400px;
    height: 200px;
    border: 3px solid #73AD21;
    }

    div.absolute {
    position: absolute;
    top: 80px;
    right: 0;
    width: 200px;
    height: 100px;
    border: 3px solid #73AD21;
    }
    </style>
    </head>
    <body>

    <h2>position: absolute;</h2>

    <p>An element with position: absolute; is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed):</p>

    <div class="relative">This div element has position: relative;
    <div class="absolute">This div element has position: absolute;</div>
    </div>

    </body>
    </html>

```

</details>
<details>
<summary>
sticky
</summary>

An element with `position: sticky;` is positioned based on the user's scroll position.

A sticky element toggles between `relative` and `fixed`, depending on the scroll position. It is positioned relative until a given offset position is met in the viewport - then it "sticks" in place (like `position:fixed`).

```HTML
    <!DOCTYPE html>
    <html>
    <head>
    <style>
    div.sticky {
    position: -webkit-sticky;
    position: sticky;
    top: 0;
    padding: 5px;
    background-color: #cae8ca;
    border: 2px solid #4CAF50;
    }
    </style>
    </head>
    <body>

    <p>Try to <b>scroll</b> inside this frame to understand how sticky positioning works.</p>

    <div class="sticky">I am sticky!</div>

    <div style="padding-bottom:2000px">
    <p>In this example, the sticky element sticks to the top of the page (top: 0), when you reach its scroll position.</p>
    <p>Scroll back up to remove the stickyness.</p>
    <p>Some text to enable scrolling.. Lorem ipsum dolor sit amet, illum definitiones no quo, maluisset concludaturque et eum, altera fabulas ut quo. Atqui causae gloriatur ius te, id agam omnis evertitur eum. Affert laboramus repudiandae nec et. Inciderint efficiantur his ad. Eum no molestiae voluptatibus.</p>
    <p>Some text to enable scrolling.. Lorem ipsum dolor sit amet, illum definitiones no quo, maluisset concludaturque et eum, altera fabulas ut quo. Atqui causae gloriatur ius te, id agam omnis evertitur eum. Affert laboramus repudiandae nec et. Inciderint efficiantur his ad. Eum no molestiae voluptatibus.</p>
    </div>

    </body>
    </html>

```

</details>

</details>

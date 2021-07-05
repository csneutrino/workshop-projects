# Day 2

- DOCTYPE

  Html document starts with document type declaration.

  `<!DOCTYPE>` declaration represents the document type, and helps browsers to display web pages correctly.

  It's not a html tag but a information to the browser about what type of document to expect.

  Doctype for HTML 5 is:

  ```html
  <!DOCTYPE html>
  ```

  Similarly doctypes for HTML 4 and XHTML 1.1 are:

  ```html
  <!-- HTML 4 -->
  <!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">

  <!-- XHTML 1.1 -->
  <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
  ```

- `html` , `head` , `title` & `body` tag

  - html

    `html` tag represents the root of HTML document. It is a container to all html elements.

  - head

    Contains meta information about the webpage

  - title

    specifies a title for the HTML page (which is shown in the browser's title bar or in the page's tab)

  - body

    element defines the document's body, and is a container for all the visible contents, such as headings, paragraphs, images, hyperlinks, tables, lists, etc.

  ```html
  <!DOCTYPE html>
  <html>
    <head>
      <title>Hello</title>
    </head>
    <body>
      Hello World
    </body>
  </html>
  ```

- Comments

  HTML comments are not displayed in the browser, but they can help document your HTML source code.

  ```html
  <!-- This is a comment -->
  ```

- Headings

  Search engines use the headings to index the structure and content of your web pages.

  Use HTML headings for headings only. Don't use headings to make text BIG or bold.

  - Heading 1

    ```html
    <h1>This is a heading 1</h1>
    ```

  - Heading 2

    ```html
    <h2>This is a heading 2</h2>
    ```

  - Heading 3

    ```html
    <h3>This is a heading 3</h3>
    ```

  - Heading 4

    ```html
    <h4>This is a heading 4</h4>
    ```

  - Heading 5

    ```html
    <h5>This is a heading 5</h5>
    ```

  - Heading 6

    ```html
    <h6>This is a heading 6</h6>
    ```

- Paragraphs

  A paragraph always starts on a new line, and is usually a block of text.

  The HTML <p> element defines a paragraph.

  A paragraph always starts on a new line, and browsers automatically add some white space (a margin) before and after a paragraph.

  ```html
  <p>Hello, I am a paragraph</p>
  <p>Hello, I am another paragraph</p>
  ```

- `hr` & `br`

  - hr

    The `<hr>` tag is used to define thematic changes in the content:

    `<hr>` the thematic break (Horizontal Rule) (a scene change in a story, or a transition to another topic within a section of a reference book).

    ```html
    <p>The first rule of Fight Club is: You do not talk about Fight Club.</p>

    <hr />

    <p>The second rule of Fight Club is: Always bring cupcakes.</p>
    ```

  - br

    The `<br>` ( line breaks tag )HTML element produces a line break in text. It is useful for writing a poem or an address, where the division of lines is significant.

    ```html
    <p>
      O’er all the hilltops<br />
      Is quiet now,<br />
      In all the treetops<br />
      Hearest thou<br />
      Hardly a breath;<br />
      The birds are asleep in the trees:<br />
      Wait, soon like these<br />
      Thou too shalt rest.
    </p>
    ```

- Attributes

  HTML attributes provide additional information about HTML elements.

  ```html
  <tagname attrname="attrvalue"></tagname>
  ```

  HTML allows attribute values without quotes.

  ```html
  <tagname attrname="attrvalue"></tagname>
  ```

  However, we recommend quoting attribute values. Also, it will not work when the value has space. Only `attrvalue` will be taken as a value. `attrvalue2` will be taken as another attribute.

  ```html
  <tagname attrname="attrvalue1" attrvalue2></tagname>
  ```

  Correct way will be

  ```html
  <tagname attrname="attrvalue1 attrvalue2"></tagname>
  ```

- Some global attributes

  - title

    The `title` attribute specifies extra information about an element. The information is most often shown as a tooltip text when the mouse moves over the element.

    ```html
    <h1 title="Roshan Acharya">Roshan</h1>
    ```

  - hidden

    The `hidden` attribute will hide a html element from document.

    ```html
    <h1 hidden>I am no longer useful</h1>
    ```

  - class

    `class` attribute is used to specify a class for an HTML element. Multiple elements can have same class.

    ```html
    <p class="color-red">Css will style me</p>
    ```

    Mostly used to access html elements from `css` and `javascript` .

  - id

    `id` attribute is used to specify a unique id for an HTML element. Multiple elements can't have same id.

    ```html
    <h1 id="maintitle">I am The Main Title</h1>
    ```

  - style

    `style` attribute is used to add styles to an element, such as color, font, size, and more.

    ```html
    <p style="color:red;">I am red</p>
    <p style="color:green;font-family:monospace;">
      I am blue in monospace font
    </p>
    ```

    We will learn about `style` attribute later.

- Formatting Elements

  HTML contains several elements for defining text with a special meaning.

  - `<b>` & `<strong>`

    `b` element defines bold text, without any extra importance.

    `strong` element defines text with strong importance. The content inside is typically displayed in bold.

    ```html
    <b>I am bold</b> <strong>I am bold and important</strong>
    ```

  - `<i>` & `<em>`

    `i` element defines italic text.

    `<em>` element defines emphasized text `(force wa importance diyera padhne khalko)`. The content inside is typically displayed in italic.

    ```html
    <i>I am italic</i> <em>I am italic and emphasized text</em>
    ```

  - `<sub>`

    `sub` element defines subscript text.

    ```html
    The molecular formaula of water is H<sub>2</sub>O
    ```

  - `<sup>`

    `sup` element defines superscript text.

    ```html
    Two to the power 2 is written as 2<sup>2</sup>.
    ```

- Links

  `<a>` (anchor) tag with `href` attribute can be used to navigate between documents.

  ```html
  <a href="https://www.facebook.com/csneutrino">Follow Us On Facebook</a>
  <a href="about.html">About</a>
  <a href="../admin/login.html">Login</a>

  <!--
    ./ => this folder 
    ../ => one folder back 
    .../ => two folders back // confusing hunxa hai yesto 
    ../../ => two folders back
  -->

  <!-- scroll to the element with id "footer" -->
  <a href="#footer">Footer</a>
  ```

- Images

  `img` tag is used to embed an image in a web page. It's a self closing tag.

  ```html
  <img src="url-to-image" alt="text-about-image" />

  <img src="./cat.png" alt="Laughing cat" height="500" width="500" />

  <!-- Image as a link -->
  <!-- Image ma click garesi wikipedia khulxa hai -->
  <a href="https://en.wikipedia.org/wiki/Gautama_Buddha">
    <img
      src="../gautam-buddha.jpeg"
      alt="Gautam Buddha"
      height="100"
      width="100"
    />
  </a>
  ```

- Lists

  HTML lists allow web developers to group a set of related items in lists.

  - Unordered Lists

    Unordered lists is used to group items having no numerical order.

    ```html
    <ul>
      <li>This is a list item</li>
      <li>This is another list item</li>
      <li>This is one more list item</li>
    </ul>
    ```

    - This is a list item
    - This is another list item
    - This is one more list item

  - Ordered Lists

    Ordered list is used for listing items with numerical order

    ```html
    <ol>
      <li>This is List item number 1</li>
      <li>This is List item number 2</li>
      <li>This is List item number 3</li>
    </ol>
    ```

    1. This is List item number 1
    2. This is List item number 2
    3. This is List item number 3

  - Description Lists

    ( teti sarai use chai hudaina hai )

    ```html
    <dl>
      <dt>Coffee</dt>
      <dd>- black hot drink</dd>
      <dt>Milk</dt>
      <dd>- white cold drink</dd>
    </dl>
    ```

- Quotations & Citation

  - blockquote

    The `<blockquote>` HTML element indicates that the enclosed text is an extended quotation.

    A URL for the source of the quotation may be given using the `cite` attribute.

    ```html
    <blockquote cite="https://www.huxley.net/bnw/four.html">
      Words can be like X-rays, if you use them properly—they’ll go through
      anything. You read and you’re pierced.
    </blockquote>
    ```

  - q

    The `<q>` HTML element indicates that the enclosed text is a short inline quotation.

    Most modern browsers implement this by surrounding the text in quotation marks.

    This element is intended for short quotations that don't require paragraph breaks; for long quotations use the `<blockquote>` element.

    ```html
    <p>
      WWF's goal is to:
      <q>Build a future where people live in harmony with nature.</q>
    </p>
    ```

  - abbr

    The HTML tag `<abbr>` defines an abbreviation or an acronym, like "HTML", "CSS", "Mr.", "Dr.", "ASAP", "ATM".

    Marking abbreviations can give useful information to browsers, translation systems and search-engines.

    The optional `title` attribute can provide an expansion or description for the abbreviation. If present, title must contain this full description and nothing else.

    ```html
    <abbr title="Hyper Text Markup Language">HTML</abbr>
    ```

  - cite

    The `<cite>` HTML element is used to describe a reference to a cited creative work, and must include the title of that work. The reference may be in an abbreviated form according to context-appropriate conventions related to citation metadata.

    ```html
    <p><cite>Harry Potter</cite> by British author J. K. Rowling.</p>
    ```

- Iframe

  An HTML `iframe` is used to display a web page within a web page.

  It is a good practice to always include a title attribute for the `<iframe>`. This is used by screen readers to read out what the content of the `iframe` is.

  ```html
  <iframe
    src="another-page.html"
    height="200"
    width="300"
    title="Another Page"
  ></iframe>
  ```

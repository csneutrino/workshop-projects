# Summary of Day 4

> By Roshan Acharya

- Video

  The HTML `<video>` element is used to show a video on a web page.

  Provide path to video in `src` attribute. If browser doesn't support `video` tag then show text inside video tag.

  ```html
  <video width="50%" src="./videos/flower.mp4" controls autoplay muted>
    Your browser doesn't support video tag.
    <a href="./videos/flower.mp4">Click here to see video.</a>
  </video>
  ```

  Browser may support video tag but may not support all the formats.
  <br />
  You can provide more than one source to display the one that is supported.

  `poster` attribute is a thumbnail of the video. Initially when video is not played poster is shown.

  ```html
  <video poster="./images/logo.png" controls>
    <source src="./videos/flower.mp4" type="video/mp4" />
    <source src="./videos/flower.webm" type="video/webm" />
    Your browser doesn't support video tag.
  </video>
  ```

- Audio

  The HTML `<audio>` element is used to play an audio file on a web page.

  ```html
  <audio src="./audios/roar.mp3" controls></audio>
  ```

  `audio` tag also supports fallback and multiple sources like in `video` tag.

- Computer Code

  HTML contains several elements for defining user input and computer code.

  ```html
  <code> int x = 45; </code>

  <kbd>Ctrl + S</kbd>

  <pre>
      <code>
        int x = 5, i;
        
        for(i = 0; i < 50; i ++){
          if(i % 10 == 0){
            printf("%d", i);
          }else {
            printf("hehe");
          }
        }
      </code>
  </pre>

  Area of Reactangle:
  <var>l</var> * <var>b</var>
  ```

- Semantics

  A semantic element clearly describes its meaning to
  both the browser and the developer.

  Semantic html tags = ( tags with a meaning )

  Semantic: `form`, `table`, `input`, `article`

  Non Semantic: `div`, `span`

- Entites, meta utf-8, emojis

  ```html
  <pre>
    &lt;p&gt;Hello World&lt;/p&gt;
  </pre>

  <div>Hello&nbsp;&nbsp;&nbsp;World.</div>

  <!-- &nbsp; // non breaking space <br />
    &lt; // less than <br />
    &gt; // greater than <br />
    &amp; // ampersand <br /> -->
  ```

  ```html
  <head>
    <!-- replace utf-8 with acii -->
    <meta charset="UTF-8" />
  </head>

  <body>
    <p>&#128525;</p>
    <p>😍</p>

    <p>مدى الحياة من التوفيق إذا قمت بترجمة هذا</p>

    <!-- <p>&#128525;</p>
      <p>😍 </p>
  
      <p>&#128516;</p>
      <p>😄</p>
  
      <meta charset="UTF-8">
   مدى الحياة من التوفيق إذا قمت بترجمة هذا
  
      https://www.w3schools.com/charsets/ref_emoji.asp -->
  </body>
  ```

- Remaining basic tags

  ```html
  <a target="_blank" href="https://google.com">Go to google.</a>

  <a href="mailto:csneutrino@gmail.com">Mail Us</a>

  <form>
    <input type="color" />
    <input type="range" />
    <input type="reset" />

    <label for="fav">Your Fav. Programming Language</label>
    <select name="select" id="fav">
      <option value="js">Javascript</option>
      <option value="python">Python</option>
      <option value="c++">C++</option>
      <option value="php">PHP</option>
    </select>
  </form>

  <small>I am small.</small>
  <p>I am normal.</p>

  <button>Click Me</button>

  <figure>
    <img src="./images/logo.png" alt="csneutrino" />
    <figcaption>Logo Of CSneutrino</figcaption>
  </figure>

  <img src="./this is invalid image.png" alt="Logo of csneutrino" />

  <mark>I am highlighted</mark> <br />
  ```

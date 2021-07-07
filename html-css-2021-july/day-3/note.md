# Summary of Day 3

> By Roshan Acharya

- Table
  `<table>` tag defines an HTML table.<br />
  `<tr>` tag defines table row.<br />
  `<th>` tag defines table header. <br />
  `<td>` tag defines table data. <br />

  ```html
  <table border="1">
    <tr>
      <th>Name</th>
      <th>Age</th>
    </tr>
    <tr>
      <td>Roshan Acharya</td>
      <td>21</td>
    </tr>
    <tr>
      <td>John Doe</td>
      <td>22</td>
    </tr>
  </table>
  ```

  <details>
      <summary>
        colspan
      </summary>
  colspan allows a single table cell to span the width of more than one cell or column.

  ```html
  <table border="1" width="500">
    <tr>
      <th colspan="2">Men</th>
      <th colspan="2">Women</th>
    </tr>
    <tr>
      <td>20-30</td>
      <td>30-40</td>
      <td>20-30</td>
      <td>30-40</td>
    </tr>
    <tr>
      <td>5</td>
      <td>5</td>
      <td>5</td>
      <td>5</td>
    </tr>
    <tr>
      <td>5</td>
      <td>5</td>
      <td>5</td>
      <td>5</td>
    </tr>
  </table>
  ```

  </details>

  <details>
    <summary>
      rowspan
    </summary>
    rowspan allows a single table cell to span the height of more than one cell or row.

  ```html
  <table width="50%" border="1">
    <tr>
      <th rowspan="2">Men</th>
      <th>20-30</th>
      <td>1</td>
      <td>2</td>
      <td>7</td>
    </tr>
    <tr>
      <th>30-40</th>
      <td>2</td>
      <td>6</td>
      <td>8</td>
    </tr>
    <tr>
      <th rowspan="2">Women</th>
      <th>20-30</th>
      <td>3</td>
      <td>4</td>
      <td>9</td>
    </tr>
    <tr>
      <th>30-40</th>
      <td>4</td>
      <td>9</td>
      <td>4</td>
    </tr>
  </table>
  ```

  </details>

- Forms
  An HTML form is used to collect user input. The user input is most often sent to a server for processing.

  ```html
  <form>
    <!-- text input -->
    <input type="text" />

    <!-- email input -->
    <input type="email" />

    <!-- checkbox -->
    <input type="checkbox" />

    <!-- radio -->
    <input type="radio" />
    <!-- submit input -->
    <input type="submit" />

    <!-- submit input -->
    <input type="submit" />
  </form>
  ```

  <details>
    <summary>Label</summary>
    <ul>
    <li>
    The <code>&lt;label&gt;</code> tag defines a label for many form elements. 
    </li>
    <li>
    The <code>&lt;label&gt;</code> element is useful for screen-reader users, because the screen-reader will read out loud the label when the user focus on the input element. 
    </li>
    <li>
    The <code>&lt;label&gt;</code> element also help users who have difficulty clicking on very small regions (such as radio buttons or checkboxes) - because when the user clicks the text within the <code>&lt;label&gt;</code> element, it toggles the radio button/checkbox. 
    </li>
    <li>
    The for attribute of the <code>&lt;label&gt;</code> tag should be equal to the id attribute of the <code>&lt;input&gt;</code> element to bind them together. 
    </li>
    </ul>
  </details>

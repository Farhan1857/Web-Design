# HTML notes

### HTML

- div element, used as a container to group other elements, will share CSS styles
- **id** attributes are unique, **classes** are not
- SEO optimize webpages to make them more visible and rank higher on search engines
- Open graph protocol allows you to control how the website’s content apprears

### Audio & Video:

- audio element supports mp3, wav, ogg
    - ‘controls’ attribute: adjust vol, pause, resume
    - ‘loop’ attribute: makes the audio replay
    - ‘muted’
- video element supports mp4, ogg, webm formats
    - same attributes as audio
    - can add width
    - ‘poster’ attribute unique to video
    
    ## Sample code:
    

```
<body>
  <h1>HTML Audio and Video Lab</h1>
  <section>
    <h2>What is the video and how I got this</h2>
    <video
    controls
    width="640">
    <source src="https://cdn.freecodecamp.org/curriculum/labs/what-is-the-map-method-and-how-does-it-work.mp4"/ type="video/mp4">
    </video>
  </section>
  <section>
    <h2>Sailing Away</h2>
    <audio
    controls
    loop
    src="https://cdn.freecodecamp.org/curriculum/js-music-player/sailing-away.mp3"/>

    </audio>
  </section>
</body>
```

### Images

- Three tools: size, format, compression
- SVG - Scalable Vector Graphic
    - track data based on paths and equations to plot points, lines, and curves.
    - can be scaled to any size w/o impacting quality

### Sample Code:

```html
<svg width="24" height="24" viewBox="0 0 24 24" fill="red">
      <path
        d="M12 21s-6-4.35-9.33-8.22C-.5 7.39 3.24 1 8.4 4.28 10.08 5.32 12 7.5 12 7.5s1.92-2.18 3.6-3.22C20.76 1 24.5 7.39 21.33 12.78 18 16.65 12 21 12 21z"
      ></path>
    </svg>
```

- A r**eplaced element** is an element whose content is determined by an external resource rather than by CSS
    - e.g. images, iframes, and video
    - in an ‘iframe’ when you want to embed direct HTML, you have to use ‘srcdoc’ instead of src
    - accelerometer lets the iframe use motion sensors so it can detect things like device tilting and rotation. autoplay lets the video start playing automatically, and clipboard-write lets the iframe write data to the user’s clipboard.
    - the target attribute used to open links in a diff web page

### Path & File Links

- **An absolute path is a complete link to a resource.**
- **A relative path specifies the location of a file relative to the directory of the current file. It does not include the protocol or the domain name**
- The slash is known as the "path separator”
- A single dot points to the current directory, and two dots point to the parent directory.

### Semantics

- The semantic meaning of an element refers to what special information that element conveys.
    - Search engines can easily understand your website when you use semantic HTML.
- Presentational HTML focuses on the appearance and style of the content.
- The idiomatic text element, ‘i’, was originally used for presentational purposes to display the text in italics.
    - em specifies importance but ‘i’ does not
- Header element: used to define the header of a document or section.
- The "bring attention to" element, `b`, is commonly used to highlight keywords in summaries
- The `cite` element is an HTML element that you can use to mark up the title of a referenced creative work
- `abbr`: indicates an abbreviation or acronym
    - Sample code:

```jsx
<p></p>

<abbr title="HyperText Markup Language">HTML</abbr> is the foundation of the web.
```

- `address` element: Use it to build a website’s contact list
- The `time` element is used to represent a specific moment in time.
- the  `q` element is used to distinguish quoted text from the surrounding content.
- The inline `code` element is used to represent short snippets of code inside text.
    - the default format: monospaced font
- `u` element for short, is used to represent inline text that has non-textual annotation applied.
    - In HTML, the u element should only be used to indicate that text has non-textual annotation applied. To style a piece of text with an underline, you should use CSS instead of HTML.
- The `ruby` element represents small text shown above or below the main text
- The `nav` element is used to provide navigation links to other sections in the document
    - used for menus, table of contents
- The `article` element represents self contained content on a web page.
- The `form` element in HTML is used to gather user information, such as names and email addresses
- `input` is a void element
    - `form, label` are not
- Sample code using buttons, input, form, label:

```jsx
<form action="">
<label for="email">Email address:</label>
<input type="email" id="email" name="email" />
<button type="submit">Submit form</button>
</form>
```

- Button types: button, reset, submit
- The `required` attribute specifies that the user needs to fill out that portion of the form before it gets submitted
- Form controls, like inputs, can be in different stages or conditions like a `focused` state,  `readonly` state, or `disabled` state
- The `action` attribute is used to specify where the form data should be sent when the form is submitted.
- The `method` attribute is used to specify the HTTP method to use when sending the form data. The most common methods are GET and POST.
- You can group related inputs together using the `fieldset` element.
- The `for` attribute on the `label` element should match the `id` attribute on the `input` element. This is known as an explicit association.
- Example of using radio button:

```
<input id="yes-option" type="radio" name="hotel-stay" />
<label for="yes-option">Yes</label>
<input id="no-option" type="radio" name="hotel-stay" />
<label for="no-option">No</label>
```

### Tables in HTML:

Sample code:

```html
<table id="quickfacts">
  <thead>
    <tr>
      <th colspan="2">Quick Facts: Software Developers, Quality Assurance Analysts, and Testers</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2023 Median Pay</th>
      <td>
        $130,160 per year
        <br>$62.58 per hour
      </td>
    </tr>
    <tr>
      <th>Typical Entry-Level Education</th>
      <td>Bachelor's degree</td>
    </tr>
    <tr>
      <th>Work Experience in a Related Occupation</th>
      <td>None</td>
    </tr>
    <tr>
      <th>On-the-job Training</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Number of Jobs, 2022</th>
      <td>1,795,300</td>
    </tr>
    <tr>
      <th>Job Outlook, 2022-32</th>
      <td>25% (Much faster than average)</td>
    </tr>
    <tr>
      <th>Employment Change, 2022-32</th>
      <td>451,200</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th>If this table had a footer, it would be here.</th>
    </tr>
  </tfoot>
</table>
```

- Some use `div` to build tables instead of the `table` element
- The `colspan` attribute specifies the number of columns a cell should span.
- The `caption` element is used to write the title of the table
- The `scope` attribute determines if a header is a row header or a column header.
- Another value for the `scope` attribute is row, which indicates that a header cell is a header for its entire row

### **Working with HTML Tools**

- **HTML validator**: a tool that checks the syntax of HTML code to ensure it is valid.
- **DOM inspector**: a tool that allows you to inspect and modify the HTML structure of a web page.
- **Devtools**: a set of web developer tools built directly into the browser that helps you debug, profile, and analyze web pages.
- aria-hidden attribute: Used to hide an element from assistive technologies such as screen readers. For example, this can be used to hide decorative images that do not provide any meaningful content.
- aria-describedby attribute: Used to provide additional information about an element by associating it with another element that contains the information. This helps assistive technologies understand the purpose of the element.
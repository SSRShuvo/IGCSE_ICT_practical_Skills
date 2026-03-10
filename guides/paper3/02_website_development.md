# Paper 3 Task B — Website Development with Microsoft Expression Web

Microsoft Expression Web is used in Paper 3 for **creating and editing web pages** using HTML and CSS. You will be given content and asked to build a multi-page website to an exact specification.

---

## 1. Setting Up the Website

### 1.1 Creating a New Website
1. Open Expression Web → **File** → **New** → **Web Site…**
2. Choose **Empty Web Site**.
3. Set the location to a folder with the **exact name** given in the question.
4. Click **OK**.

### 1.2 Opening an Existing Website Folder
1. **File** → **Open Site…**
2. Navigate to the folder and click **Open**.

### 1.3 Creating a New Web Page
1. **File** → **New** → **Page…** (or **Ctrl + N**).
2. Choose **HTML** → **General** → **HTML** → **OK**.
3. Save with the **exact filename** from the question (e.g. `index.htm`, `contact.htm`).

### 1.4 The Expression Web Interface

| Panel | Purpose |
|---|---|
| Folder List | Shows all files in the website |
| Code view | Edits raw HTML/CSS |
| Design view | Visual WYSIWYG editor |
| Split view | Shows Design and Code side-by-side |
| CSS Properties | Manages CSS rules and values |
| Tag Properties | Shows properties of the selected HTML element |

> **Tip:** Use **Split view** (View → Split) so you can see the HTML code and the visual result at the same time.

---

## 2. Basic HTML Structure

Every web page must have this basic HTML structure:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Page Title Here</title>
    <link rel="stylesheet" type="text/css" href="stylesheet.css">
  </head>
  <body>

    <!-- Page content goes here -->

  </body>
</html>
```

- `<!DOCTYPE html>` — declares this as an HTML document.
- `<head>` — contains metadata, title, and links to CSS files.
- `<title>` — text shown in the browser tab.
- `<body>` — all visible content goes inside here.

---

## 3. Common HTML Tags

### 3.1 Headings and Paragraphs

| Tag | Purpose |
|---|---|
| `<h1>…</h1>` | Level 1 heading (largest) |
| `<h2>…</h2>` | Level 2 heading |
| `<h3>…</h3>` | Level 3 heading |
| `<p>…</p>` | Paragraph |
| `<br>` | Line break (no closing tag needed) |
| `<hr>` | Horizontal rule / dividing line |

### 3.2 Text Formatting Tags

| Tag | Purpose |
|---|---|
| `<strong>…</strong>` | Bold (semantic) |
| `<b>…</b>` | Bold (presentational) |
| `<em>…</em>` | Italic (semantic) |
| `<i>…</i>` | Italic (presentational) |
| `<u>…</u>` | Underline |

### 3.3 Lists

**Unordered (bulleted) list:**
```html
<ul>
  <li>Item one</li>
  <li>Item two</li>
  <li>Item three</li>
</ul>
```

**Ordered (numbered) list:**
```html
<ol>
  <li>First item</li>
  <li>Second item</li>
</ol>
```

### 3.4 Division and Span

| Tag | Purpose |
|---|---|
| `<div>…</div>` | Block-level container — groups other elements |
| `<span>…</span>` | Inline container — styles part of a line |

---

## 4. Hyperlinks

### 4.1 Linking to Another Page in the Website
```html
<a href="contact.htm">Contact Us</a>
```

### 4.2 Linking to an External Website
```html
<a href="https://www.example.com">Visit Example</a>
```

### 4.3 Opening a Link in a New Window/Tab
```html
<a href="https://www.example.com" target="_blank">Visit Example</a>
```

### 4.4 Email Link
```html
<a href="mailto:info@example.com">Email us</a>
```

### 4.5 Anchor (Jump to a Section on the Same Page)
First, create the anchor target:
```html
<h2 id="section2">Section 2</h2>
```
Then link to it:
```html
<a href="#section2">Jump to Section 2</a>
```

### 4.6 Creating a Hyperlink in Expression Web Design View
1. Select the text or image to turn into a link.
2. **Insert** menu → **Hyperlink…** (or **Ctrl + K**).
3. In the dialog, choose:
   - **Existing File or Web Page** — browse or type the URL.
   - **E-mail Address** — type the email address.
   - **Bookmark** — link to an anchor on the page.
4. Set **Target frame** if the link should open in a new window (`_blank`).
5. Click **OK**.

---

## 5. Images

### 5.1 Inserting an Image in HTML
```html
<img src="images/photo.jpg" alt="Description of the image" width="300" height="200">
```

- `src` — path to the image file (relative to the current page).
- `alt` — alternative text (displayed if the image cannot be loaded; important for accessibility).
- `width` and `height` — dimensions in pixels (can also be set in CSS).

### 5.2 Inserting an Image in Expression Web Design View
1. Place the cursor where the image should appear.
2. **Insert** menu → **Picture** → **From File…**
3. Navigate to the image file and click **Insert**.
4. Fill in the **Accessibility Properties** dialog (alt text) → **OK**.

### 5.3 Resizing an Image
- In Design view: drag the image handles, or
- Right-click the image → **Picture Properties** → **Appearance** tab → set Width and Height in pixels.
- In Code view: set `width` and `height` attributes or use CSS `width` and `height` properties.

### 5.4 Image as a Hyperlink
```html
<a href="page2.htm"><img src="button.png" alt="Go to Page 2"></a>
```

---

## 6. Tables

Tables organise data into rows and columns. Do **not** use tables for page layout — use CSS for that.

### 6.1 Basic Table Structure
```html
<table border="1">
  <tr>
    <th>Heading 1</th>
    <th>Heading 2</th>
  </tr>
  <tr>
    <td>Data 1</td>
    <td>Data 2</td>
  </tr>
  <tr>
    <td>Data 3</td>
    <td>Data 4</td>
  </tr>
</table>
```

- `<table>` — the table container.
- `<tr>` — table row.
- `<th>` — table header cell (bold and centred by default).
- `<td>` — table data cell.

### 6.2 Spanning Columns or Rows
```html
<td colspan="2">This cell spans 2 columns</td>
<td rowspan="3">This cell spans 3 rows</td>
```

### 6.3 Adding a Table in Expression Web Design View
1. **Table** menu → **Insert Table…**
2. Set the number of rows and columns.
3. Set border size, padding, and spacing.
4. Click **OK**.

---

## 7. CSS (Cascading Style Sheets)

CSS controls the visual appearance of the website. In IGCSE, you will create an **external stylesheet** (.css file) that links to all pages.

### 7.1 Creating an External CSS File
1. **File** → **New** → **Page…** → **CSS** → **OK**.
2. Save as the filename given in the question (e.g. `styles.css` or `stylesheet.css`).

### 7.2 Linking the CSS File to an HTML Page
Add this line inside the `<head>` section of every HTML page:
```html
<link rel="stylesheet" type="text/css" href="styles.css">
```

### 7.3 CSS Syntax
```css
selector {
    property: value;
    property: value;
}
```

Example:
```css
body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    margin: 0;
    padding: 0;
}

h1 {
    color: #003366;
    font-size: 24px;
}

p {
    color: #333333;
    line-height: 1.6;
}
```

### 7.4 CSS Selectors

| Selector | Example | Selects |
|---|---|---|
| Element | `p` | All `<p>` elements |
| Class | `.highlight` | All elements with `class="highlight"` |
| ID | `#header` | The element with `id="header"` |
| Descendant | `nav a` | All `<a>` inside `<nav>` |
| All | `*` | Every element |

### 7.5 Common CSS Properties

**Text and Fonts:**
| Property | Example | Purpose |
|---|---|---|
| `font-family` | `Arial, sans-serif` | Font name (always provide a fallback) |
| `font-size` | `16px` or `1.2em` | Text size |
| `font-weight` | `bold` or `400` | Bold/normal weight |
| `font-style` | `italic` | Italic text |
| `color` | `#ff0000` or `red` | Text colour |
| `text-align` | `left`, `center`, `right`, `justify` | Horizontal alignment |
| `text-decoration` | `none`, `underline` | Removes or adds underline |
| `text-transform` | `uppercase`, `capitalize` | Text case |
| `line-height` | `1.5` | Space between lines |
| `letter-spacing` | `2px` | Space between characters |

**Background:**
| Property | Example | Purpose |
|---|---|---|
| `background-color` | `#ffffff` | Solid background colour |
| `background-image` | `url('bg.jpg')` | Background image |

**Box Model (spacing):**
| Property | Example | Purpose |
|---|---|---|
| `width` | `200px` or `50%` | Element width |
| `height` | `100px` | Element height |
| `margin` | `10px` or `10px 20px` | Space outside the border |
| `padding` | `10px` | Space inside the border |
| `border` | `1px solid #000` | Border shorthand |
| `border-width` | `2px` | Border thickness |
| `border-color` | `#333` | Border colour |
| `border-style` | `solid`, `dashed`, `dotted` | Border style |

**Display and Positioning:**
| Property | Example | Purpose |
|---|---|---|
| `display` | `block`, `inline`, `none` | How element is displayed |
| `float` | `left`, `right` | Float element |
| `clear` | `both` | Clear floated elements |

### 7.6 Colour Values in CSS
- **Named colours**: `red`, `blue`, `green`, `white`, `black`
- **Hex**: `#ff0000` (red), `#00ff00` (green), `#0000ff` (blue), `#ffffff` (white), `#000000` (black)
- **RGB**: `rgb(255, 0, 0)` (red)

### 7.7 Styling Hyperlinks with CSS
```css
a {
    color: #003366;
    text-decoration: none;
}

a:hover {
    color: #cc0000;
    text-decoration: underline;
}
```

### 7.8 Applying CSS Classes and IDs in HTML
```html
<!-- Class applied to multiple elements -->
<p class="highlight">This paragraph is highlighted.</p>
<span class="highlight">This span is also highlighted.</span>

<!-- ID applied to one unique element -->
<div id="header">This is the header.</div>
```

---

## 8. Navigation Bar

A navigation bar links to all pages in the website.

```html
<nav>
  <a href="index.htm">Home</a>
  <a href="about.htm">About</a>
  <a href="contact.htm">Contact</a>
</nav>
```

CSS for the navigation bar:
```css
nav {
    background-color: #003366;
    padding: 10px;
}

nav a {
    color: white;
    text-decoration: none;
    padding: 5px 15px;
    display: inline-block;
}

nav a:hover {
    background-color: #cc0000;
}
```

---

## 9. Page Structure Best Practice

A typical IGCSE web page structure:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>My Page Title</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
  </head>
  <body>
    <div id="header">
      <h1>Website Name</h1>
    </div>

    <nav>
      <a href="index.htm">Home</a>
      <a href="page2.htm">Page 2</a>
    </nav>

    <div id="content">
      <h2>Page Heading</h2>
      <p>Paragraph text here.</p>
    </div>

    <div id="footer">
      <p>© 2024 My Website</p>
    </div>
  </body>
</html>
```

---

## 10. Checking Your Work in a Browser

1. In Expression Web, press **F12** or go to **File** → **Preview in Browser** → choose your browser.
2. Check that:
   - All text appears correctly.
   - Images are displayed (check the `src` path if they are not).
   - All hyperlinks work when clicked.
   - The stylesheet is applied (fonts, colours, spacing).
   - The page looks correct in both **Internet Explorer** and another browser (e.g. Chrome).
3. Use **View → Source** in the browser to check the HTML if needed.

---

## 11. Saving and File Management

- Keep all website files in the **same folder** (or use an `images` subfolder for images).
- Image file paths must be correct relative to the HTML file:
  - Same folder: `src="photo.jpg"`
  - In a subfolder: `src="images/photo.jpg"`
- Never use absolute paths like `C:\Users\...` — they won't work on another computer.
- Save the CSS file with the exact name you used in the `<link>` tag.

---

## 12. Common HTML Entities

When you need to display special characters in HTML, use these entities:

| Character | Entity Code |
|---|---|
| `&` (ampersand) | `&amp;` |
| `<` (less than) | `&lt;` |
| `>` (greater than) | `&gt;` |
| `"` (quotation mark) | `&quot;` |
| `©` (copyright) | `&copy;` |
| `®` (registered) | `&reg;` |
| non-breaking space | `&nbsp;` |

---

## Common Mistakes to Avoid

| Mistake | How to Avoid |
|---|---|
| Missing `<link>` tag for CSS | Check that every HTML file links to the stylesheet in its `<head>` |
| Images not showing | Check the `src` path and filename (case-sensitive on some servers) |
| Missing `alt` attribute on images | Always include a descriptive `alt` attribute |
| Hyperlinks not working | Check `href` for correct filename and extension; test in a browser |
| CSS not applying | Verify the stylesheet filename in the `<link>` tag matches the .css file |
| Using absolute file paths | Always use relative paths (e.g. `images/photo.jpg`) |
| Not closing HTML tags | Every opening tag needs a matching closing tag (e.g. `<p>…</p>`) |
| Wrong background or text colour | Copy hex values carefully; use `#` prefix |
| Table structure wrong | Every `<tr>` must be inside `<table>`; every `<td>` inside `<tr>` |
| Page title missing or wrong | Check the `<title>` tag in `<head>` matches the question |

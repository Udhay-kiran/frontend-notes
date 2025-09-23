# HTML Notes

## HTML Document Structure

Every HTML5 page follows a standard structure. It tells the browser how to interpret the content.

---

### Basic Skeleton

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Page Title</title>
</head>
<body>
  <h1>Hello, World!</h1>
  <p>This is my first HTML page.</p>
</body>
</html>
```


1. `<!DOCTYPE html>` - Declares that this is an HTML5 documents and is always the first line.
2. `<html lang="en">` - Root element of the page, `lang="en"` specifies the language
3. `<head>` - Contains metadata (information about the page, invisible to the users)

    Common elements include:
        a. `<meta charset="UTF-8">` - character encoding (it supports all languages)

        b. `<meta name="viewport" content="width=device-width, initial-scale=1.0">` - makes pages responsive on mobile devices.

        c. `<title>` - the title shown on browser tab.

4. `<body>` section - Contains all the visible content (text, images, buttons, forms, etc.). Users also inteact with what is contained within the body.

## HTML Text Tags

### Example Code

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Text Tags Example</title>
</head>
<body>
  <h1>Main Heading</h1>
  <p>This is a <strong>very important</strong> paragraph. Please <em>read carefully</em>.</p>
  
  <p>Line one.<br>Line two (after a line break).</p>
  
  <hr>
  
  <pre>
  Preformatted text keeps
      spaces and line breaks
  exactly as typed.
  </pre>
  
  <p>Run <code>git status</code> in your terminal.</p>
</body>
</html>
```
1. `<h1>.....</h1>` - Heading. Defines the most important title on the page. They range from `<h1>` to `<h6>`
2. `<p>.....</p>` - Paragraph. Wraps blocks of text into paragraphs. Browsers add space above/below automatically.
3. `<strong> ... </strong>` - Highlights text that has strong importance (bold + semantic meaning).
4. `<em> ... </em>` - Adds emphasis (italic + semantic meaning). Screen readers stress the word.
5. `<br>`- Break.  No closing tag. Inserts a line break inside text without starting a new paragraph.
6. `<hr>` - No closing tag. Creates a horizontal line dividing sections.
7. `<pre>....</pre>` -  Preserves whitespace and line breaks exactly as typed. Useful for code or text like poetry.
8. `<code>......</code>` - Marks text as inline code and uses monospace font. 



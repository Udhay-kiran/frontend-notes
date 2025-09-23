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

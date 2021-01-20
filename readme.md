# Protocol
Use HTTPS for embedded resources where possible.

## HTML
``` html 
<!-- Recommended -->
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.0/jquery.min.js"></script>
```

## CSS
``` css
/* Recommended */
@import 'https://fonts.googleapis.com/css?family=Open+Sans'; 
```

# Formatting Rules
## Indentation
Indent by 2 spaces at a time.


``` html
<ul>
  <li>Fantastic
  <li>Great
</ul>
```

``` css
.example {
  color: blue;
} 
```
## Capitalization
All code has to be lowercase
* HTML element names, attributes, attribute values
* CSS selectors, properties, and property 
* __Exception of__ strings
``` html
<!-- Recommended -->
<img src="google.png" alt="Google">
```
``` css
/* Recommended */
color: #e5e5e5;
```

## Encoding
 UTF-8
``` html
<!-- Recommended -->
<img src="google.png" alt="Google">
```
``` css
<!-- NOT Recommended -->
@charset "UTF-8";
```

## Action Items
Mark todos and action items with TODO.
```html
<!-- TODO: remove optional tags -->
<ul>
  <li>Apples</li>
  <li>Oranges</li>
</ul>
```

# HTML
## Document Type
* HTML 5
* HTTP Header
  * Content-Type: text/html; charset=UTF-8

```html
<!DOCTYPE html>
``` 
## HTML Validity
Use tools such as the [W3C HTML validator](https://validator.w3.org/nu/) to test.

## Semantics
Use HTML according to its purpose.

 For example, use heading elements for headings, p elements for paragraphs, a elements for anchors, etc.

 ```html
<!-- Recommended -->
<a href="/">This is a Link</a>
 ```

 ## Multimedia Fallback
 For multimedia, such as images, videos, animated objects via canvas, make sure to offer alternative access. For images that means use of meaningful alternative text (alt) and for video and audio transcripts and captions, if available.

 ``` html
<!-- Recommended -->
<img src="spreadsheet.png" alt="Spreadsheet screenshot.">
 ```
 ## Separation of Concerns
 Strictly keep structure (markup), presentation (styling), and behavior (scripting) apart, and try to keep the interaction between the three to an absolute minimum.

 In addition, keep the contact area as small as possible by linking as few style sheets and scripts as possible from documents and templates.

## Entity References
Do not use entity references.

The __only exceptions__ apply to characters with special meaning in HTML (like < and &) as well as control or “invisible” characters (like no-break spaces).

## Optional Tags
Omit optional tags (optional).

``` html
<!-- Recommended -->
<!DOCTYPE html>
<title>Saving money, saving bytes</title>
<p>Qed.
```

## type Attributes
Omit type attributes for style sheets and scripts.

Specifying type attributes in these contexts is not necessary as HTML5 implies `text/css` and `text/javascript` as defaults. This can be safely done even for older browsers.

```html
<!-- Recommended -->
<link rel="stylesheet" href="https://www.google.com/css/maia.css">

<!-- Recommended -->
<script src="https://www.google.com/js/gweb/analytics/autotrack.js"></script>
``` 
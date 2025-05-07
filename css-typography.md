# Font Family
## Mult-word values
should be placed in quotes ''

    h1 {
    font-family: 'Times New Roman';
    }

## Web safe fonts
appear the same across all browsers and OSes.
full list https://www.cssfontstack.com/

### Fallback fonts and font stacks

Defining multiple fonts creates a font stack. If the first listed isn't available, next is tried, etc.

- Serif fonts have embellishments on characters
- Sans serif fonts don't.
- These can be used as a generic fallback

ie

    h1 {
    font-family: Caslon, Georgia, 'Times New Roman', serif;
    }

## Font Weight
Options:
- bold
- normal
- lighter one weight lighter than parent element
- bolder one weight bolder than parent element
- Numeric values 1 to 1000 also accepted
  - increments of 100 commonly used
  - 400 = normal
  - 700 = bold

## Font Style

apply italics
normal = normal

    h3 {
    font-style: italic;
    }

## Text transform
Change case
uppercase / lowercase
  
    h1 {
    text-transform: uppercase;
    }

## Text Layout

### Letter Spacing

    p {
    letter-spacing: 2px;
    }

### Word Spacing

    h1 {
    word-spacing: 0.3em; 
    }

accepts px or em with em being preferred

https://www.w3schools.com/cssref/css_units.php

em 	Relative to the font-size of the element (2em means 2 times the size of the current font)

### Line Height

accepts px or em or unitless w/ unitless being preferred because it's responsive based on font size

    p {
    line-height: 1.4;
    }

### Text Alignment

    h1 {
    text-align: right;
    }

## Web fonts
- https://fonts.google.com/
- https://fonts.adobe.com/
- fonts.com
Free font services, like Google Fonts and Adobe Fonts, host fonts that you can link to from your HTML document with a provided <link> element.

You can also use fonts from paid font distributors like fonts.com by downloading and hosting them with the rest of your site’s files. You can create a @font-face ruleset in your CSS stylesheet to link to the relative path of the font file. 

### Web font using link

index.html:

    <head>
    <!-- Add the link element for Google Fonts along with other metadata -->
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@100&display=swap" rel="stylesheet">
    </head>

style.css:

    p {
    font-family: 'Roboto', sans-serif;
    }

### Web font using @font-face

common file formats:
- OTF
- TTF
- WOFF
- WOFF2

It’s a good idea to include TTF, WOFF, and WOFF2 formats with your @font-face rule to ensure compatibility on all browsers.

[mdn web-fonts docs](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Text_styling/Web_fonts#generating_the_required_code)

    @font-face {
    font-family: 'MyParagraphFont';
    src: url('fonts/Roboto.woff2') format('woff2'),
        url('fonts/Roboto.woff') format('woff'),
        url('fonts/Roboto.ttf') format('truetype');
    }

Best practice to define @font-face at top of CSS stylesheet.

Within delcaration block 'font-family' sets custom name for the font. src property points to each font file + its filetype.

Browser will try fonts in order listed.

[CSS-TRICKS How to use @font-face in CSS: font prioritization](https://css-tricks.com/snippets/css/using-font-face-in-css/)

Font used as normal after that.

    p {
    font-family: 'MyParagraphFont', sans-serif;
    }


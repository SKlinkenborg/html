# CSS

Change different elements by invoking element + {} ie h1 {}, p {} for heading1 or paragraph
## Fonts

### Font Family
Change font using font-family property:

    h1 {
        font-family: Garamond;
    }

- Font must be installed locally or loaded from online
- 'Web safe fonts': fonts supported by most browsers & OS
- Non-web safe fonts may render different in different contexts
- If more than 1 word, best practice to put name in quotes

### Font Size

    p {
        font-size: 18px;
    }

### Font Weight

    p {
        font-weight: (bold | normal);
    }

### Text Align

    h1 {
        text-align: (left | center | right| justify);
    }

Justify: spread text out to align w right and left side of parent element.

### Color

Color can affect foreground and background color.
FG is the color the element appears in. = color property
BG is the BG... = background-color

    h1 {
        color: red;
        background-color: blue;
    }

### Opacity

0 to 100 as 0.0 to 1.0 where
0 = opaque 1 = fully invisible

    .overlay {
        opacity: 0.5; /* 50% opacity /*
    }

### Background Image

Set background image *for an element*

    .main_banner {
        background-image: url('https://example.com/image.png'); /* relative or absolute URL */
    }

### Important

Over-ride other style rules

    p {
    color: blue !important;
    }

    .main p {
    color: red;
    }

W color blue !important, blue will override red in .main even though .main's reference is more specific.
Useful when workingg with multiple stylesheets.
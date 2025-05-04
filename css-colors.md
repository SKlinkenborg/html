# Colors

Can be defined 3 ways
- Named colors "white"
- RGB Red Green Blue 
  - Hex "#FFFFFF" or Decimal "rgb(23, 45,23) (0-255);
- HSL

foreground color ('color') referes to the element itself, background ('background-color') is the color behind it.

## RGB
### Hex color examples:

    darkseagreen: #8FBC8F
    sienna:       #A0522D
    saddlebrown:  #8B4513
    brown:        #A52A2A
    black:        #000000 or #000
    white:        #FFFFFF or #FFF
    aqua:         #00FFFF or #0FF

ie

    background-color: #9932cc;

### RGB Decimal color examples:

    #8FBC8F = rgb(143, 188, 143)

ie

    color: rgb(23, 45, 23);

## HSV
    color hsl(hue, saturation, lightness)
    color: hsl(120, 60%, 70%);

- Hue: angle on the color wheel- see color_wheel_4_background.svg
- Saturation: intensity / purity of color 100% pure color 0% grey color
- Lightness: how light or dark. 50% is default/normal; 100% white, 0% black

HSL is convenient for adjusting colors. In RGB, making the color a little darker may affect all three color components. In HSL, that’s as easy as changing the lightness value. HSL is also useful for making a set of colors that work well together by selecting various colors that have the same lightness and saturation but different hues.

## Opacity and Alpha

### Add opacity parameter to HSL
    color: hsla(34, 100, 50$, 0.1);

where 0 is opaque and 1 is transparent

You can think of the alpha value as, “the amount of the background to mix with the foreground”. When a color’s alpha is below one, any color behind it will be blended in. The blending happens for each pixel; no blurring occurs.

A little unconventional, but still worth mentioning is how hex colors can also have an alpha value. By adding a two-digit hexadecimal value to the end of the six-digit representation (#52BC8280), or a one-digit hexadecimal value to the end of the three-digit representation (#F003), you can change the opacity of a hexadecimal color. Hex opacity ranges from 00 (transparent) to FF (opaque).

Alpha can only be used with HSL, RGB, and hex colors; we cannot add the alpha value to name colors like green.

There is, however, a named color keyword for zero opacity, transparent. It’s equivalent to rgba(0, 0, 0, 0), and it’s used like any other color keyword:

color: transparent;

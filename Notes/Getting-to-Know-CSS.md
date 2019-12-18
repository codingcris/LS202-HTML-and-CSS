# Getting to Know CSS
These are my personal notes from Shay Howe's Getting to Know CSS tutorial. You can view the tutorial [here](https://learn.shayhowe.com/html-css/getting-to-know-css/)

## The Cascade 
The cascade determines the order in which styles are applied to elements. In general, styles are applied as they are declared in our stylesheet from top to bottom, with the potential to easily override styles at the top. The specicifity of selectors adds complexity to this model, as a more specific selector's declared styles will not be overwritten by a less specific selector regardless of position.

## Calculating Specificity
* Selectors hold different specificity weights; these along with a selector's position in the cascade will determine how a style is rendered.
    1. The type selector has the lowest specificity weight with a point value of 0-0-1
    2. The class selector has medium specificity weight with a point value of 0-1-0
    3. The id selector has the highest specificity weight with a point value of 1-0-0 

### Specifity Within Combined Selectors
* We can combine different selectors in order to target specific elements. This creates a combined selector which has a specificity weight point value equal to the sum of the point values of each selector being combined. Ex:

    ```CSS
    .hotdog p.mustard {
        background: yellow;
    }
    ```
    Types of selectors used: 2 class (0-1-0) and one type (0-0-1) selector.
    Specificity point value of combined selectors: 0-2-1

* These point values are important to understanding how our styles will be rendered. Higher point value selectors will override lower point value selectors.
* Keeping specificity weights low makes our CSS code harder to break.

## Common CSS Property Values

### Colors
* Colors in CSS are defined on a standard RGB color space. We may represent color values with keywords, hexadecimal notation, and RGB & HSL values.
    * keyword colors are defined within the [CSS specification](https://www.w3.org/TR/css-color-3/)
    * Hexadecimal values give us access to 16.7+ million colors and can be used in place of keywords
    * RGB colors are defined using the ```rgb(red, green, blue)``` function where red, green, and blue are integers from 0-255 with 0 being a value of pure black and 255 being a value of pure white.
        * The ```rgba(red, green, blue, alpha)``` function accepts an alpha parameter which is a value from 0-1 (decimals included) that determines the transparancy of our color. 1 is fully opaque, 0 is fully transparent.
    * HSL colors are defined using the ```hsl(hue, saturation, lightness)``` function.
        * hue accepts a value from 0-360 specifying a color's degree on a color wheel.
        * saturation accepts a percent value specifying how saturated with color the hue is. 0% is greyscale, 100% is fully saturated.
        * lightness accepts a percent value specifying how dark or light a color is. 0% is full black, 100% is full white.
        * the ```hsla()``` function accepts an alpha parameter which is a value from 0-1 (decimals included) that determines the transparancy of our color. 1 is fully opaque, 0 is fully transparent.

### Lengths
* Pixels (px) are an absolute measurement of length. A pixel is 1/96th of an inch
* Percentages are a relative measurement of length and are determined as the percent of an element's parent length.
# Sass/Less Material Color Palettes

> This color palette comprises primary and accent colors that can be used for illustration
> or to develop your brand colors. They’ve been designed to work harmoniously with each other.
> The color palette starts with primary colors and fills in the spectrum to create a complete
> and usable palette for Android, Web, and iOS. Google suggests using the 500 colors as the
> primary colors in your app and the other colors as accents colors.
>
> From [material.io](https://material.io/guidelines/style/color.html#color-color-palette).

Google's Material Design color palettes, for [Sass/SCSS](http://sass-lang.com/) and [Less](http://lesscss.org/).


## Sass

For Sass/SCSS projects, include `_google-material-colors.scss` high in your project's cascade (the Settings or Tools level if you follow [ITCSS](http://www.creativebloq.com/web-design/manage-large-css-projects-itcss-101517528) for project management).
The palettes are stored in a nested map, and are accessible through the custom `material-color` function.

To get the desired color, pass the name and (optionally) the tone into the function.
Colors have the same names given on the Material Design website, with hyphenation instead of spaces where relevant.
The tone argument is optional, and will default to 500 if not specified.

Example:
```scss
.block {
    background-color: material-color(deep-purple);
    color: material-color(grey, 100);
}
```
Output:
```css
.block { background-color: #673ab7; color: #f5f5f5; }
```

## Less

For Less projects, including `google-material-colors.less` in your project will add the entire palette to the global scope.
If you don't want the entire palette in your scope, individual color palettes can be specified by including their respective files (e.g. to use the red palette alone, include `google-material-colors.red.less`).
Variables follow a `@material-[color]-[tone]` namespace, with the option to drop `[tone]` and default to 500.

Example:
```less
.block {
    background-color: @material-deep-purple;
    color: @material-grey-100;
}
```
Output:
```css
.block { background-color: #673ab7; color: #f5f5f5 }
```

## LICENSE

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <http://unlicense.org>


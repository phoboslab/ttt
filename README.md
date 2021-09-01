# Tiny Texture Tumbler

A small JS library to create textures. Mainly useful for file size restricted 
competitions.

# Editor

https://phoboslab.org/ttt/


# Usage

Include the ttt.min.js into your project.

The `ttt()` function takes an array of texture definitions and returns an array
of canvas elements. You can use the canvas element as the source for 
`ctx.drawImage()`, to create WebGL textures with `gl.texImage2D()` or to just 
add them to your HTML.

```js
// Example texture 32x32 pixels with a pink background
ttt([32, 32, 0xf0ff]).map(canvas => document.body.appendChild(canvas));
```


# Notes

- Colors are saved as 16bit values. Each nibble (that is each 4 bit value or each
character in hex) correspondes to an r,g,b,a value.
- The library currently has very few different drawing operations. Don't be afraid
to extend those to whatever else you need. But keep in mind
that you can draw circles and many shapes with the `text` function and a single 
letter or emoji :^)
- The `rectangle` function actually draws 3 rectangles with different colors at 
1px offsets. This is useful to create insets or bumps. You can set the alpha
of the top/bottom to 0 if you don't need it.
- You can draw a texture onto itself. If you modify the x/y position and the
alpha value, you can get some cool effects.


# License

The MIT License(MIT)

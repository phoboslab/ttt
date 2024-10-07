# Tiny Texture Tumbler

A small JS library to create textures. Mainly useful for file size restricted 
competitions. Used with much success in [Q1k3](https://phoboslab.org/log/2021/09/q1k3-making-of).

![Example](https://phoboslab.org/content/assets/q1k3-textures.png)

# Editor

- [phoboslab.org/ttt](https://phoboslab.org/ttt/) (empty workspace)
- [phoboslab.org/ttt/#W1s2NCw2NC...](https://phoboslab.org/ttt/#W1s2NCw2NCwwLDIsMywxLjQsMiwxNzE3NiwxLjNdLFs2NCw2NCwzODc1MSwxLDE4LDQsMiwyLDI3LDksNjU1MzAsMCw3LDEsLTEsOSwxMyw1LDUyLDgsOCw2NTUyOCwzOTAzOSw0LDAsMCwwLDY0LDUxMiwxNSw0LDAsMCwwLDY0LDY0LDE0XSxbNjQsNjQsMzg3NTEsMSwxOCw0LDIsMiwyNyw5LDY1NTMwLDAsNywxLC0xLDAsMTMsNjQsNTIsNjQsOCw2NTUzMSwzOTAzOSw0LDAsMCwwLDY0LDUxMiwxNSw0LDAsMCwwLDY0LDY0LDE0XSxbNjQsNjQsMTMxMTksNCwxLDAsMCw2NCw2NCwxNSwwLDI0LDExLDE3LDUwLDY1NTIzLDIsOF0sWzMyLDMyLDIxODM5LDEsMCwyLDEwLDIsMTEsNCw2NTUyOCwxMCwyNTkzMSw0LDAsMCwwLDMyLDMyLDE0XSxbMzIsMzIsMTc0ODcsMCwxLDEsMzAsMzAsNjU1MjgsMTEsMjE1ODAsNCwwLDAsMCwzMiwzMiwxNV0sWzMyLDMyLDMwMDE1LDQsNSwwLDAsMzIsMzIsMTUsMSw1LDQsMiwyLDIyLDYsNjU1MjIsMCw4XSxbMzIsMzIsODc1MSwxLDEsMSw4LDQsMTEsNSw2NTUyNCwxNSwxNzQ4Nyw0LDAsMCwwLDY0LDY0LDE1XSxbMzIsMzIsMTMxMTksNCw0LDAsMCwzMiwzMiwxNSwxLDEwLDMsMTEsNiwyNSwxMCw2NDUzNiw2NDU2OCw2NTUxOV0sWzMyLDMyLDg3NTEsMSwxLDEsMywzLDQsNCw2NTUyNCwxNCwyMTU2NSwxLDEsLTEsMTUsMSwxNiwxNiw2NTUyMiw3LDAsMSwtMSwwLDEsMTUsMTYsNiw2NTUyMSwwLDQsNCwwLDAsMCwzMiwzMiwxNV0sWzMyLDMyLDg3MTksMiw2MzUwNiwxLDQsMCwwLDAsMzIsMzIsMTJdLFszMiwzMiwyMTI5NSw0LDEwLDAsLTQsMzIsMjk4LDEwLDIsNDM3MiwxXSxbMzIsMzIsODQ2MywxLC0xLDEsMzUsMSwzNSw0LDY1NTIyLDEwLDM0Mzk5LDAsLTEsNiwzNCw2LDY1NTI2LDIsMzQzOTksMiwyOTQ3OSwxLDQsNiwwLDAsMzIsMzIsNV0sWzMyLDMyLDg0NjMsMSwwLDAsMywzLDQsNCwwLDEwLDY1NTIxLDAsNCw0LDIzLDIzLDEwLDY0ODg1LDIxNTUxLDMsNCwxNiwxMywwLDExLCI6Ol1bOjoiLDQsMCw0LDQsMjYsMjYsMTVdLFszMiwzMiw4NzUxLDEsMSwxLDgsMywxMSw1LDY1NTI0LDE1LDE3NDg3LDAsOSw2LDE0LDEzLDE1LDY1NTI1LDQzODMsNCwwLDAsMCw2NCw2NCwxMiwzLDEwLDExLDIwMjY3LDAsOCwiLS0tIl0sWzMyLDMyLDE3NDg3LDQsNSwwLDAsMzIsMzIsMTUsMSw0LDQsMywzLDIyLDIyLDY1NTIzLDcsMzA1ODddLFs2NCw2NCwxMzExOSwwLDAsMCw2NCw2NCwwLDAsNjQyNzEsMywtMSw1MCwzMzc5NSwwLDMyLCJYWFgiLDQsNywwLDAsNjQsNjQsNl0sWzY0LDY0LDM0MDYzLDQsNywwLDAsNjQsNjQsMTIsMiwxMjU1NCwxXSxbMzIsMzIsNjU1MzUsNCwxMiwwLDAsMzIsMzIsOSwzLDYsMzAsNjE0NTUsMCwyNSwiKyJdLFszMiwzMiw1OTAzLDQsMTIsMCwwLDMyLDMyLDksMyw1LDE0LDY1NTI5LDAsMTIsIk5J0JgiXSxbMzIsMzIsNjQyNzEsMCwxMiwxLDcsMzAsNjU1MjgsOCw2MzI0Nyw0LDcsMCwwLDMyLDMyLDhdLFszMiwzMiwxMzExOSwxLDEsMSwxNCwxNCwxNiwzMiw1NjMyOCwxNSwyNjM5OSwxLC03LDE3LDE0LDE0LDE2LDMyLDU2MzI4LDgsMjYxNTksMiwyOTcwNiwxLDQsMCwwLDAsMzIsMzIwLDE0XSxbMzIsMzIsMzM1NjcsMSwxLDEsNiwzMCwxNiwzMSw2NTUyNiwxNSwzMzgyMywxLDksLTE0LDYsMzAsMTYsMzIsNjU1MjYsMTUsMjk3NDMsMiw1NTYyNSwxLjUsNCwwLDAsMCwzMiwzMjAsMTVdLFszMiwzMiwxMjU1OSwxLDEsMSwxNCwxNCwxNiwxNiw2NTUyNSw3LDIxMjk1LDAsMSwxLDE0LDE0LDY1NTI1LDAsMzQzOTksMCwxNywxNywxNCwxNCw2NTUyNCwwLDM0Mzk5LDIsOCwxLjVdLFszMiwzMiw5NTAzLDQsMTEsMCwwLDMyLDMyLDEyLDEsMSwxLDYsNyw2LDgsNjU1MjEsMCw0XV0=) (some textures from [q1k3](https://github.com/phoboslab/q1k3))


# Usage

Include the ttt.min.js into your project.

The `ttt()` function takes an array of texture definitions and returns an array
of canvas elements. You can use the canvas element as the source for 
`ctx.drawImage()`, to create WebGL textures with `gl.texImage2D()` or to just 
add them to your HTML.

```js
// Example texture 32x32 pixels with a pink background
ttt([[32, 32, 0xf0ff]]).map(canvas => document.body.appendChild(canvas));
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

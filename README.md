# Sloped Edge - Sass mixin

With this powerful Sass mixin (uses `scss` syntax), you'll be able to build sloped section edges with a consistent angle.
It uses most basic `css` properties, mainly just a `border`... No `transforms` or `clip-path` properties, no `svg` images.


## Installation (pick one)

1. [Download latest release](https://github.com/dvlden/sloped-edge/releases)
2. `git clone https://github.com/dvlden/sloped-edge.git`
3. `yarn add sloped-edge`
4. `npm i sloped-edge`


## Usage

```scss
// import mixin
@import '~sloped-edge';

// set variable for a color
$dark-gray: #292929;

// give it a class with any name you prefer
.section {
  // apply some base styling to the section
  background-color: $dark-grey;
  min-height: 50vh;
  
  // let the mixin do the magic
  @include sloped-edge-root;
  @include sloped-edge($dark-grey, 'right');
}
```

> HINT: For "real-world" use case and more advanced example, check "examples" live or locally.


## Arguments

| Argument    | Default Value | Possible Value               |
| ----------- | ------------- | ---------------------------- |
| `$color`    | -             | any color (e.g. `#292929`)   |
| `$position` | -             | `in`, `out`, `right`, `left` |
| `$height`   | `5rem`        | any number with a unit that is supported within `border-width` property |

> HINT: For the `$color` you don't necesserily have to use `HEX` value.


## Variables

| Variable              | Default Value       | Possible Value |
| --------------------- | ------------------- | -------------- |
| `$sloped-edge-height` | `5rem`              | -              |
| `$sloped-edge-layout` | `'y'`               | `x`, `y`       |


## Examples

You'll find two examples that include all possible variations. The only difference between these examples is a layout...
You can download this whole project and open examples locally or you may check live examples _(hosted on GitHub Pages)_:

- [Sloped Edge - Vertical Example](https://dvlden.github.io/sloped-edge/vertical/)
- [Sloped Edge - Horizontal Example](https://dvlden.github.io/sloped-edge/horizontal/)


## Browser Support

Basically, just the support of Viewport units (`vw` | `vh`). Check the browser coverage on the link below...

[Can I Use - Viewport units?](https://caniuse.com/#search=viewport%20units)

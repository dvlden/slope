# Slope - A Sass mixin

With this powerful Sass mixin (uses `scss` syntax), you'll be able to build slope section edges with a consistent angle.
It uses most basic `css` properties, mainly just a `border`... No `transforms` or `clip-path` properties, no `svg` images.


## Installation (pick one)

- `npm i @dvlden/slope`
- `pnpm i @dvlden/slope`
- `yarn add @dvlden/slope`


## Usage

```scss
// import mixin
@use './node_modules/slope/src/index' as slope;

// set variable for a color
$dark-grey: #292929;

// give it a class with any name you prefer
.section {
  // apply some base styling to the section
  background-color: $dark-grey;
  min-height: 50vh;

  // let the mixin do the magic
  @include slope.edge-root;
  @include slope.edge($dark-grey, 'right');
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

| Variable  | Default Value | Possible Value |
| --------- | ------------- | -------------- |
| `$height` | `5rem`        | -              |
| `$layout` | `'y'`         | `x`, `y`       |


## Examples

You'll find two examples that include all possible variations. The only difference between these examples is a layout...
You can download this whole project and open examples locally or you may check live examples _(hosted on GitHub Pages)_:

- [Vertical Example](https://dvlden.github.io/slope/vertical/)
- [Horizontal Example](https://dvlden.github.io/slope/horizontal/)


## Browser Support

Basically, just the support of Viewport units (`vw` | `vh`). Check the browser coverage on the link below...

[Can I Use - Viewport units?](https://caniuse.com/#search=viewport%20units)

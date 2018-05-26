# Sloped Edge - Sass mixin

With this powerful Sass mixin (uses `scss` syntax), you'll be able to build sloped section edges with consistent angle.
It uses most basic `css` properties, mainly just a `border`... No `transforms` or `clip-path` properties, no `svg` images.


## Installation (pick one)

1. [Download latest release](https://github.com/dvlden/sloped-edge/releases)
2. `git clone https://github.com/dvlden/sloped-edge.git`
3. `yarn add sloped-edge`
4. `npm i sloped-edge`


## Usage

```scss
// import mixin
@import 'sloped-edge';

// set variable for a color
$dark-gray: #292929;

// give it a class with any name you prefer
.sloped {
  // apply some base styling to the section
  background-color: $dark-grey;
  min-height: 300px;
  
  // let the mixin do the magic
  @include sloped-edge($dark-grey, 'right', $root: true);
}
```

## Arguments

| Argument    | Default | Description |
| ----------- | ------- | ----------- |
| `$color`    | `null`  | The color of sloped edge. _(color of your section should match this color)_ |
| `$position` | `null`  | The position of sloped edge. _(can be: `in`, `out`, `right`, `left`)_ |
| `$height`   | `5rem`  | The height of the sloped edge. _(that's a perfect size, but you can tweak it if you like)_ |
| `$root`     | `false` | Prevents code duplication. _(as you will always have sections, you would call root once at the sloped edge class)_ |


## Examples

You can download the Sloped Edges locally and take a look at `example` directory.
I combined all possible variants into a single demo.

> Reminder for myself: I think we can use GH pages to link into `example` directory and make live demo instead?


## Browser Support

Basically, just the support of `vw` unit. Check the browser coverage on the link below...

[Can I Use - Viewport Width unit?](https://caniuse.com/#search=vw)


## Q & A

1. You said no `transform` properties, but I can clearly see one in your mixin? `-webkit-transform: rotate(360deg);`

> Yes, I clearly stated that. You can also see a note next to that line of code... It simply fixes some weird choppy border bug on Safari _(cause Safari is dumb)_ :punch:. It is also affects Webkit browsers only, but it really makes no difference in any other Webkit browser, except Safari.

2. Why the need for `$root` argument? 

> Because it prevents duplicate code and it is the only way that actually can work out for this particular mixin. In most cases, you will have multiple Sloped/Angled sections and this will help a lot. Trust!

# 449 CSS

A CSS "helper" created at 4:49 pm🙂🎨

449 takes away the pain of performing basic utility tasks, has helpers for margin-ing, padding-ing, color-ing and some other basic stuff.

## Directory Structure

```bash
C:.
├───dist
├───scss
└───templates
```

- **dist** contains raw css files
- **scss** contains the scss source of 449
- **templates** contains examples created with 449

## Why use 449?

Other utility libraries come with bloated functionality (features you most likely will never use), others come with pre-built styling and a whole lot more unnneccesities. 449 comes with classes for only the most used css functions like positioning, spacing...

This means that you can use 449 together with other css libraries like bootstrap, materialize and even other utility libraries like tailwind, and it won't get in the way. That's a promise!

## Installation

You can quickly install 449 using npm or yarn.

```sh
yarn add 449.css
```

```sh
npm i 449.css
```

## Usage

After installing 449, you can use the prebuilt css or scss if you want more control and "power".

```js
// import css
import "449.css/dist/449.css";

// import scss
import "449.css/scss/";

// you may need to add the index pased on your compiler
import "449.css/scss/index.scss";
```

Or in html

```html
<script src="node_modules/449.css/dist/449.css"></script>
```

You can also import the scss source directly in your own scss

```scss
@import "~449.css/scss/";
```

### responsiveness

449 doesn't come with a grid system like other libraries do, however, it still comes with grid breakpoints that follow bootstrap's system.

```scss
$xs: 0;
$sm: 576px;
$md: 768px;
$lg: 992px;
$xl: 1200px;
$xxl: 1400px;
```

Thanks to the media breakpoints, you can build responsively, like hiding items on smaller screens, setting a particular height for an item on tab... There are endless possibilities here.

If you imported the scss source, you should have access to the 449 reponsive mixins which allow you to easily make responsive media queries like this:

```scss
@include sm-down {
    color: blue;
}
```

This code will only run on screens smaller than `$sm: 576px;`

The available mixins are:

- xs - 0px to 576px
- sm-down - 576px down
- sm - 577px to 768px
- sm-up - 577px up
- md-down - 768px down
- md - 769px to 992px
- md-up - 769px up
- lg-down - 992px down
- lg - 993px to 1200px
- lg-up - 993px up
- xl-down - 1400px down
- xl - 1201px to 1400px
- xl-up - 1200px up
- xxl - 1401px up

Even if you won't be using mixins, 449's dimensions are based on these mixins, so you can always refer to them.

### dimensions

Dimensions are the basis of 449 css styling. There are a few things to note in terms of sizing:

#### Scales

449 has 2 unique scales for sizing: pixels and percentages. To reference the pixel sizing, use `_` eg: `ml:_1` to give a margin left of `10px`. You can use a number directly for the percentage scale eg: `ml:10` for a margin left of `10%`. Below is the full range of available values for both scales.

- "-1": -10px
- "-2": -20px
- "-3": -30px
- "-4": -40px
- "-5": -50px
- "-6": -60px
- "-7": -70px
- "-8": -80px
- "-9": -90px
- "-10": -100px
- "0": 0
- "_1": 10px
- "_2": 20px
- "_3": 30px
- "_4": 40px
- "_5": 50px
- "_6": 60px
- "_7": 70px
- "_8": 80px
- "_9": 90px
- "_10": 100px
- "auto": auto
- "10": 10%
- "20": 20%
- "25": 25%
- "30": 30%
- "33": 33.33%
- "40": 40%
- "45": 45%
- "50": 50%
- "60": 60%
- "66": 66.66%
- "70": 70%
- "75": 75%
- "80": 80%
- "90": 90%
- "100": 100%
- "10vh": 10vh
- "25vh": 25vh
- "50vh": 50vh
- "75vh": 75vh
- "100vh": 100vh
- "10vw": 10vw
- "25vw": 25vw
- "50vw": 50vw
- "75vw": 75vw
- "100vw": 100vw

The dimensions util comes with classes for setting:

- height (h) eg: `h:100`
- max height (max-h) eg: `max-h:100`
- min height (min-h) eg: `min-h:100`
- width (w) eg: `w:100`
- max width (max-w) eg: `max-w:100`
- min width (min-w) eg: `min-w:100`

As shown in the **responsiveness** section above, you can combine these dimensions with breakpoints like this:

```html
<div class="max-h-xs:100 max-h-sm-up:80">...
```

### margin

449 comes with a margin utility that allows you to easily set margins for your elements. The available classes are:

- margin (m) eg: `m:_1`
- margin left and right (mx) eg: `mx:_1`
- margin up and down (my) eg: `my:_1`
- margin top (mt) eg: `mt:_1`
- margin bottom (mb) eg: `mb:_1`
- margin left (ml) eg: `ml:_1`
- margin right (mr) eg: `mr:_1`

Just as with **dimensions**, you can also combine margins with breakpoints:

```html
<div class="m-xs:_1 m-sm-up:_5">...
```

### padding

449 comes with a padding utility that allows you to easily set paddings for your elements. The available classes are:

- padding (p) eg: `p:_1`
- padding left and right (px) eg: `px:_1`
- padding up and down (py) eg: `py:_1`
- padding top (pt) eg: `pt:_1`
- padding bottom (pb) eg: `pb:_1`
- padding left (pl) eg: `pl:_1`
- padding right (pr) eg: `pr:_1`

Just as with **margins**, you can also combine paddings with breakpoints:

```html
<div class="p-xs:_1 p-sm-up:_5">...
```

### position

The position utility allows you to easily set a CSS position on your element. The available classes are:

- `position:relative`
- `position:absolute`
- `position:fixed`
- `position:sticky`

Besides these, you can also set the top, bottom, left and right positions of items on the screen using dimensions. eg:

- `top:_1` (top: 10px)
- `left:20` (left: 20%)

```html
<div class="position:fixed bottom:_1 right:_2">...
```

Just as with the above utilities, you can also use responsiveness here:

```html
<div class="position-xs:relative position-sm-up:fixed">...
<div class="left-xs:0 left-sm-up:_3">...
```

### display

### cursor

### overflow

### animation

### shadow

### border

### colors

### font

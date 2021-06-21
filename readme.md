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

### margin

### padding

### position

### display

### cursor

### overflow

### animation

### shadow

### border

### colors

### font

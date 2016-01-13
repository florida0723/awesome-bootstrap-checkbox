Awesome Bootstrap Checkbox
==========================
[![NPM version](https://img.shields.io/npm/v/awesome-bootstrap-checkbox.svg?style=flat)](https://www.npmjs.com/package/awesome-bootstrap-checkbox)
[![NPM downloads](https://img.shields.io/npm/dm/awesome-bootstrap-checkbox.svg?style=flat)](https://www.npmjs.com/package/awesome-bootstrap-checkbox)
[![Dependency Status](https://img.shields.io/david/dev/flatlogic/awesome-bootstrap-checkbox.svg?branch=master&style=flat)](https://www.npmjs.com/package/awesome-bootstrap-checkbox)

Font Awesome Bootstrap Checkboxes &amp; Radios plugin. Pure css way to make inputs look prettier. **No javascript**!

**[Demo](http://flatlogic.github.io/awesome-bootstrap-checkbox/demo/)**

Use
------------

First just include **awesome-bootstrap-checkbox.css** somewhere in your html. Or **awesome-bootstrap-checkbox.scss** if you use sass.
Next everything is based on code convention. Here is checkbox markup from Bootstrap site:

````html
<form role="form">
  ...
  <div class="checkbox">
    <label>
      <input type="checkbox"> Check me out
    </label>
  </div>
  ...
</form>
````

We have to alter it a bit:
````html
<form role="form">
  ...
  <div class="checkbox abc-checkbox">
    <input type="checkbox" id="checkbox1">
    <label for="checkbox1">
        Check me out
    </label>
  </div>
  ...
</form>
````
That's it. It will work. But it **will not** work if you nest input inside label or put label before input.

If you want to enable **Opera 12** and earlier support  just add class `styled` to `input` element:
````html
...
<input type="checkbox" id="checkbox1" class="styled">
...
````

Browser support
-----------
- Firefox (_3.6+_)
- Chrome  (_14+_)
- IE      (_9+_)
- Opera   (_11.6+_)
- Safari  (_6+_)

Radios
------------

It's the same for radios. Markup has to be the following:
````html
<form role="form">
  ...
  <div class="radio abc-radio">
      <input type="radio" name="radio2" id="radio3" value="option1">
      <label for="radio3">
          One
      </label>
  </div>
  <div class="radio abc-radio">
      <input type="radio" name="radio2" id="radio4" value="option2" checked>
      <label for="radio4">
          Two
      </label>
  </div>
  ...
</form>
````

Brand Colors and other features
------------

You may use `abc-checkbox-primary`, `abc-checkbox-danger`, `abc-radio-info`, etc to style checkboxes and radios with brand bootstrap colors.

`abc-checkbox-circle` is for rounded checkboxes.

`abc-checkbox-single` and `abc-radio-single` for inputs without label text.

Glyphicons way (Opt-out Font Awesome)
------------

If you want to use glyphicons instead of font-awesome then override `.abc-checkbox` class:
````css
.abc-checkbox input[type=checkbox]:checked + label:after {
    font-family: 'Glyphicons Halflings';
    content: "\e013";
}
.abc-checkbox label:after {
    padding-left: 4px;
    padding-top: 2px;
    font-size: 9px;
}
````

Using SASS
----------

As per example in the `demo` folder, to use these **awesome** you'll have to `@import` the following library parts:

````scss
@import "../bootstrap/scss/variables";
@import "../bootstrap/scss/mixins";

@import "../Font-Awesome/scss/variables";
````

Adjust this to the path where your bootstrap and font-awesome files are located.

Credits
------------

Based on the [Bootstrap 4][http://getbootstrap.com/] and the awesome [Font Awesome](https://github.com/FortAwesome/Font-Awesome).

# Components

Mui by default contains components. to use them you must import file to your project after importing core.

```scss
@import "mui/src/mui";
@import "mui/src/component/button";
@import "mui/src/component/container";
@import "mui/src/component/grid";
@import "mui/src/component/heading";
@import "mui/src/component/icon";
@import "mui/src/component/image";
@import "mui/src/component/input";
@import "mui/src/component/layout";
@import "mui/src/component/link";
```

## Button

by default button styling `<input type="button">`, `<input type="submit">`, `<input type="reset">`, `<button>` and `.button` class.

**is-{color}** change color to registered {color}

```html
<input type="submit" />
<input type="reset" />
<button class="is-error">Delete item</button>
<a class="button is-primary"></a>
```

**Note:** by default every button use `get-gap('element')` for margin to next element. the margin is left side for `rtl` and right side for `ltr` global direction mode. to override this direction you can wrap buttons inside `is-ltr` and `is-rtl` block or attach `is-ltr-layout` and `is-rtl-layout` class to button.

```html
<div class="is-rtl">
    <input type="submit" class="is-primary" />
    <a href="..." class="button">Back</a>
</div>

// manually
<button class="is-primary is-rtl-layout">Reverse margin button</button>
```

## Container

**is-fluid** This class make container width 100% on all devices.

**is-fit** Remove container bottom margin.

**has-{gap}-padding** This class set container padding to registered gaps.

**Note:** Container has `normal gap` for padding and `container gap` for margin bottom by default.

container width is `100%` for **tablet** and **mobile**, `960px` for **desktop** and `1200px` for **widescreen** and larger screen.

**has-grid** remove all container padding and make grid fit inside container.

## Grid

Mui has default grid system. columns size is equal by default but you can register and use unit to add column size.

**is-start-align** This class align grid items to start of grid.

**is-end-align** This class align grid items to end of grid.

**is-stretched** This class align grid items stretched.

**is-stackable** This class make grid stacked on mobile.

**is-reversed** This class make stacked grid reversed.

**is-fit** Make column size fit to content size

```html
<div class="grid">
    <!-- Three equal column -->
    <div class="column">...</div>
    <div class="column">...</div>
    <!-- Break line and make new row -->
    <div class="break">...</div>
    <div class="column is-fit">...</div>

    <!-- Half size on all device, 2-of-3 on mobile and 1-of-3 on widescreen or wider -->
    <div class="column is-half is-2-of-3-mobile is-1-of-3-widescreen">...</div>
</div>
```

## Heading

Mui use registered font size for headings. You can override registered font sizes to change this behavior.

| Heading Level | Used Font Size |
| :------------ | :------------- |
| h1            | huge           |
| h2            | big            |
| h3            | large          |
| h4            | medium         |
| h5            | normal         |
| h6            | small          |

## Icon

Make a icon container for img and svg tags.

**is-fit** disable end margin for gap for icon.

**Note:** by default every icon without `is-fit` class use `get-gap('element')` for margin to next element. the margin is left side for `rtl` and right side for `ltr` global direction mode. to override this direction you can wrap icon inside `is-ltr` and `is-rtl` block or attach `is-ltr-layout` and `is-rtl-layout` class to icon.

```html
<div class="icon">
    <svg>...</svg>
</div>
```

## Image

**is-centered** This class make img tag center aligned.

**has-radius** This class add default border radius to img tag.

**is-rounded** This class make img tag rounded.

**is-circular** This class make img tag circular.

**Sizing** Mui use registered font size for image sizing. You can override registered font sizes to change this behavior.

```html
<img src="..." alt="..." class="is-huge" />
```

## Input

input is a wrapper for input element

**is-required** mark input as required

**has-error** show errors block

```html
<div class="input is-required">
    <label>Your name:</label>
    <input type="text" />
    <!-- Show only if has-error class added to input container -->
    <div class="errors">
        <p>Name is required</p>
    </div>
</div>
```

## Layout

Layout component can used for main container of page. its come with default styled scrollbar.

**has-modal** You can add this class to make layout ui disabled (ex: make ui looks disabled when modal opened).

**is-centered** You can add this class to make layout content center aligned (ex: login page).

**is-simple** You can add this class to disable scrollbar.

## Link

Make a link element with hover animation

**is-{color}** change the link color from registered colors.

```html
<a href="/" class="link is-primary">Test link</a>
```

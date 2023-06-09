# Very Simple Grid

## Description
**Very Simple Grid**, as its name suggests, is a very simple and lightweight responsive grid system for **WordPress > DIVI** usage. It is designed to be adapted to DIVI specific media queries and can be easily inserted in some DIVI modules like text, code or tabs.

As a reminder, DIVI media queries are :

`'sm':  479px`,

`'md': 768px`,

`'lg':  980px`

**Very Simple Grid** uses the **Bootstrap class nomenclature** for easy usage.

Very Simple grid provides :
- flex grid responsive system in twelve column wrapped in container and row,
- spacing: margin and padding with breakpoints,
- display properties classes with breakpoints,
- flex direction classes with breakpoints,
- flex justify-content and align-items classes with breakpoints,
- text alignment classes with breakpoints.


## Flex responsive grid system

Very Simple Grid defines a set of styles for a grid system. It first sets two custom properties on the `:root` selector to define the gutter size and the maximum width of the container.

Then, it defines a `.s-row` class that sets the display to flex and wraps the items within it. It also sets a negative margin on the inline axis to account for the gutter.

Each child of the `.s-row` class gets the `box-sizing: border-box` property, which includes the padding within the element's width calculation. The `flex-shrink` property is set to `0`, which ensures that elements don't shrink when the container is too small. The `width` and `max-width` of the children are set to `100%` to ensure they fill the available space, and the `padding` is set to the custom property for the gutter size.

The class `.s-col` is set to `flex: 1 0 0%`, which means that it takes up as much space as possible and doesn't shrink or grow.

Classes from `.s-col-1` to `.s-col-12` define the width of each column as a fraction of the row's total width. Each class has a width value that corresponds to the number of columns it should take up, with a minimum of `8.3333%` for the smallest column and a maximum of `100%` for the largest.

Finally, there are media queries, designed to fit DIVI module's one, for small and medium-sized screens that define the same set of classes with different widths. These queries overwrite the previous styles on smaller screens, creating a responsive grid system.


## Margin and padding responsive system

The margin and padding classes in the CSS file use a naming convention similar to the Bootstrap one; it combines three parameters: direction, breakpoint, and size using the follwing structure `.m{direction}-{breakpoint}-{size}` and `.p{direction}-{breakpoint}-{size}`.

The `{direction}` can be one of the following: `t` (top), `r` (right), `b` (bottom),  `l` (left), `x` (horizontal), or `y` (vertical). 
The `{breakpoint}` also reffers to the DIVI breakpoints `sm`: 479px, `md`: 768px and `lg`: 980px.
And `{size}` can be a number from `0` to `5`, indicating the size of the margin or the padding.

For example, the class `.m-t-md-4` would add a margin of `1.5` times the value of `$s-spacer` (custom variable) to the top of an element when the screen width is at least `768px` (md breakpoint). The class `.p-b-lg-0` would remove the bottom padding of an element when the screen width is at least `980px` (lg breakpoint).

The margin and padding classes offer a simple and flexible way to add or remove margins and paddings to elements on different screen sizes.

## Responsive display properties

The display properties classes are structured this way: `.d-{breakpoint}-{displayProperty}`.
All display properties uses the `{breakpoint}` parameter as previously described.

Available display properties are:
- `.d-none` and `.s-d-none` classes hide the element they are applied to.
- `.d-inline` and `.s-d-inline` classes make the element they are applied to display as an inline element.
- `.d-inline-block` and `.s-d-inline-block` classes make the element they are applied to display as an inline block element.
- `.d-block` and `.s-d-block` classes make the element they are applied to display as a block element.
- `.d-grid` and `.s-d-grid` classes make the element they are applied to display as a grid element.
- `.d-table` and `.s-d-table` classes make the element they are applied to display as a table element.
- `.d-table-cell` and `.s-d-table-cell` classes make the element they are applied to display as a table cell element.
- `.d-table-row` and `.s-d-table-row` classes make the element they are applied to display as a table row element.
- `.d-flex` and `.s-d-flex classes` make the element they are applied to display as a flex container.
- `.d-inline-flex` and `.s-d-inline-flex` classes make the element they are applied to display as an inline flex container.

## Responsive flex directions

In conjunction with `.d-flex`or `s-d-flex`, flex directions classes offers abilities to set flexbox directions at several media queries using this pattern: `.flex{breakpoint}-{flex-direction}`or `.s-flex{breakpoint}-{flex-direction}`.

- `.flex-row` and `.s-flex-row`: Both classes set the flex-direction property to `row` with the `!important` flag. These classes can be used to make an element a flex container with items arranged horizontally in a row.
- `.flex-row-reverse` and `.s-flex-row-reverse`: Both classes set the flex-direction property to `row-reverse` with the `!important` flag. These classes can be used to make an element a flex container with items arranged horizontally in reverse order.
- `.flex-column` and `.s-flex-column`: Both classes set the flex-direction property to `column` with the `!important` flag. These classes can be used to make an element a flex container with items arranged vertically in a column.
- `.flex-column-reverse` and `.s-flex-column-reverse`: Both classes set the flex-direction property to `column-reverse` with the `!important` flag. These classes can be used to make an element a flex container with items arranged vertically in reverse order.

## Responsive flex alignments properties

In conjunction with `.d-flex`or `s-d-flex`, flex alignments classes offers abilities to set flexbox alignment items on `x`and `y`axis at several media queries using this pattern: `.justify-content-{breakpoint}-{flex-alignment}` or `.s-justify-content-{breakpoint}-{flex-alignment}` and `.align-items-{breakpoint}-{flex-alignment}` or `.s-align-items-{breakpoint}-{flex-alignment}`.

### Justify-content classes

- `.justify-content-start`, `.s-justify-content-start`: aligns elements to the left of the container.
- `.justify-content-end`, `.s-justify-content-end`: aligns elements to the right of the container.
- `.justify-content-center`, `.s-justify-content-center`: centers elements horizontally in the container.
- `.justify-content-between`, `.s-justify-content-between`: evenly distributes elements along the main axis, with the first element aligned to the start and the last element aligned to the end.
- `.justify-content-around`, `.s-justify-content-around`: evenly distributes elements along the main axis, with equal space around them.
- `.justify-content-evenly`, `.s-justify-content-evenly`: evenly distributes elements along the main axis, with equal space between them.

### Align-items classes

- `.align-items-start`, `.s-align-items-start`: aligns elements to the top of the container.
- `.align-items-end`, `.s-align-items-end`: aligns elements to the bottom of the container.
- `.align-items-center`, `.s-align-items-center`: centers elements vertically in the container.
- `.align-items-baseline`, `.s-align-items-baseline`: aligns elements such that their baselines align.
- `.align-items-stretch`, `.s-align-items-stretch`: stretches elements to fill the container along the cross-axis.

## Text alignment classes

The classes are named using a consistent pattern: `.text-{breakpoint}-{alignment}` and `.s-text-{breakpoint}-{alignment}`. The `{breakpoint}` portion of the class name indicates the screen width at which the alignment should be applied, and the `{alignment}` portion indicates the desired alignment.

There are four alignment options available: `left`, `right`, `center`, and `revert`. The `revert` option is used to reset the text alignment to the default value for the element, which can be useful in situations where the alignment has been set by some other CSS rule and needs to be overridden.


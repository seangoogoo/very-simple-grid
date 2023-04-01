# Very Simple Grid

## Description
Very Simple Grid, as its name suggests, is a very simple and lightweight responsive grid system for WordPress > DIVI usage. It is designed to be adapted to DIVI specific media queries and can easily be inserted in DIVI modules.

As a reminder, DIVI media queries are :
`'sm':  479px,
'md': 768px,
'lg':  980px`
  
Very Simple Grid uses the Bootstrap class nomenclature for easy usage.

Very Simple grid provides :
- flex grid responsive system in twelve column wrapped in container and row,
- spacing: margin and padding with breakpoints,
- display properties classes with breakpoints,
- flex direction classes with breakpoints,
- flex justify-content and align-items classes with breakpoints,
- text alignment classes


## CSS Grid system

Very Simple Grid defines a set of styles for a grid system. It first sets two custom properties on the :root selector to define the gutter size and the maximum width of the container.

Then, it defines a .s-row class that sets the display to flex and wraps the items within it. It also sets a negative margin on the inline axis to account for the gutter.

Each child of the .s-row class gets the box-sizing: border-box property, which includes the padding within the element's width calculation. The flex-shrink property is set to 0, which ensures that elements don't shrink when the container is too small. The width and max-width of the children are set to 100% to ensure they fill the available space, and the padding is set to the custom property for the gutter size.

The class .s-col is set to flex: 1 0 0%, which means that it takes up as much space as possible and doesn't shrink or grow.

Classes from .s-col-1 to .s-col-12 define the width of each column as a fraction of the row's total width. Each class has a width value that corresponds to the number of columns it should take up, with a minimum of 8.3333% for the smallest column and a maximum of 100% for the largest.

Finally, there are media queries for small and medium-sized screens that define the same set of classes with different widths. These queries overwrite the previous styles on smaller screens, creating a responsive grid system.

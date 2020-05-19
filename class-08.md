# More CSS Layout



CSS treats each HTML element as if it is in its own box. This box will either be a block-level box or an inline box.
If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element.
It is common to group a number of elements together inside a `<div>` (or other block-level) element. For example, you might group together all of the elements that form the header of a site (such as the logo and the main navigation). The `<div>` element that contains this group of elements is then referred to as the containing element.


CSS has the following positioning schemes that allow you to control the layout of a page: normal flow, relative positioning, and absolute positioning. You specify the positioning scheme using the position property in CSS. You can also float elements using the float property.

To indicate where a box should be positioned, you may also need to use box offset properties to tell the browser how far from the top or bottom and left or right it should be placed. (You will meet these when we introduce the positioning schemes on the following pages.)

### position:relative:

Relative positioning moves an element in relation to where it would have been in normal flow.
For example, you can move it 10 pixels lower than it would have been in normal flow or 20% to the right.


### position:absolute

When the position property is given a value of absolute, the box is taken out of normal flow and no longer affects the position of other elements on the page. (They act like it is not there.) 

### position:fixed:

Fixed positioning is a type of absolute positioning that requires the position property to have a value of fixed.

## Screen Size :

Different visitors to your site will have different sized screens that show different amounts of information, so your design needs to be able to work on a range of different sized screens.

## a Liquid layout :

The liquid layout uses percentages to specify the width of each box so that the design will stretch to fit the size of the screen.

---

[home](/README.md) | [About me](/about-me.md) | [contact me](/contact-me.md)
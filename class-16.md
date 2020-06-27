# Responsive Web Design
The Internet took off quicker than anyone would have predicted, growing like crazy. Now, for the past few years, mobile growth has exploded onto the scene. The growth of mobile Internet usage is also far out pacing that of general Internet usage growth.

## Responsive vs. Adaptive vs. Mobile
Responsive and adaptive web design are closely related, and often transposed as one in the same. Responsive generally means to react quickly and positively to any change, while adaptive means to be easily modified for a new purpose or situation, such as change. With responsive design websites continually and fluidly change based on different factors, such as viewport width, while adaptive websites are built to a group of preset factors. A combination of the two is ideal, providing the perfect formula for functional websites. Which term is used specifically doesn’t make a huge difference.

## Flexible Layouts
Responsive web design is broken down into three main components, including flexible layouts, media queries, and flexible media. The first part, flexible layouts, is the practice of building the layout of a website with a flexible grid, capable of dynamically resizing to any width. Flexible grids are built using relative length units, most commonly percentages or em units. These relative lengths are then used to declare common grid property values such as width, margin, or padding.
`<div class="container">`
 ` <section>...</section>`
  `<aside>...</aside>`
`</div>`

`.container {`
`  width: 538px;`
`}`
`section,`
`aside {`
`  margin: 10px;`
`}`
`section {`
`  float: left;`
`  width: 340px;`
`}`
`aside {`
`  float: right;`
`  width: 158px;`
`}`


# What is “Float”?
**Float** is a CSS positioning property. To understand its purpose and origin, we can look to print design. In a print layout, images may be set into the page such that text wraps around them as needed. This is commonly and appropriately called “text wrap”. Here is an example of that.

In web design, page elements with the CSS float property applied to them are just like the images in the print layout where the text flows around them. Floated elements remain a part of the flow of the web page. This is distinctly different than page elements that use absolute positioning. Absolutely positioned page elements are removed from the flow of the webpage, like when the text box in the print layout was told to ignore the page wrap. Absolutely positioned page elements will not affect the position of other elements and other elements will not affect them, whether they touch each other or not.

## Clearing the Float
Float’s sister property is clear. An element that has the clear property set on it will not move up adjacent to the float like the float desires, but will move itself down past the float. Again an illustration probably does more good than words do.

Clear has four valid values as well. **Both** is most commonly used, which clears floats coming from either direction. **Left** and **Right** can be used to only clear the float from one direction respectively. **None** is the default, which is typically unnecessary unless removing a clear value from a cascade. **Inherit** would be the fifth, but is strangely not supported in Internet Explorer. Clearing only the left or right float, while less commonly seen in the wild, definitely has its uses.

---

[home](/README.md) | [About me](/about-me.md) | [contact me](/contact-me.md)
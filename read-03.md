## Javascript Templating

Javascript templating is a fast and efficient technique to render client-side view templates with Javascript by using a JSON data source. The template is HTML markup, with added templating tags that will either insert variables or run programming logic. The template engine then replaces variables and instances declared in a template file with actual values at runtime, and convert the template into an HTML file sent to the client.
![image](https://images.unsplash.com/photo-1461749280684-dccba630e2f6?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80)


## FLEXBOX
**Properties for the Parent (flex container):**
- **display:** This defines a flex container; inline or block depending on the given value. It enables a flex context for all its direct children.
- **flex-direction:** This establishes the main-axis, thus defining the direction flex items are placed in the flex container.
  - **row (default):** left to right in ltr; right to left in rtl
  - **row-reverse:** right to left in ltr; left to right in rtl
  - **column:** same as row but top to bottom
  - **column-reverse:** same as row-reverse but bottom to top
- **flex-wrap:** By default, flex items will all try to fit onto one line. 
  - **nowrap (default):** all flex items will be on one line
  - **wrap:** flex items will wrap onto multiple lines, from top to bottom.
  - **wrap-reverse:** flex items will wrap onto multiple lines from bottom to top.
- **flex-flow:** This is a shorthand for the flex-direction and flex-wrap properties, which together define the flex containerâ€™s main and cross axes. The default value is row nowrap.
- **justify-content:** This defines the alignment along the main axis. It helps distribute extra free space leftover when either all the flex items on a line are inflexible, or are flexible but have reached their maximum size. It also exerts some control over the alignment of items when they overflow the line.
  - **flex-start (default):** items are packed toward the start of the flex-direction.
  - **flex-end:** items are packed toward the end of the flex-direction.
  - **start:** items are packed toward the start of the writing-mode direction.
  - **end:** items are packed toward the end of the writing-mode direction.
  - **left:** items are packed toward left edge of the container, unless that doesnâ€™t make sense with the flex-direction, then it behaves like start.
  - **right:** items are packed toward right edge of the container, unless that doesnâ€™t make sense with the flex-direction, then it behaves like start.
  - **center:** items are centered along the line.
  - **space-between:** items are evenly distributed in the line; first item is on the start line, last item on the end line
  - **space-around:** items are evenly distributed in the line with equal space around them.
  - **space-evenly:** items are distributed so that the spacing between any two items (and the space to the edges) is equal.
- **align-items:** This defines the default behavior for how flex items are laid out along the cross axis on the current line.
  - **stretch (default):** stretch to fill the container (still respect min-width/max-width).
  - **flex-start / start / self-start:** items are placed at the start of the cross axis. The difference between these is subtle, and is about respecting the flex-direction rules or the writing-mode rules.
  - **flex-end / end / self-end:** items are placed at the end of the cross axis. The difference again is subtle and is about respecting -flex-direction rules vs. writing-mode rules.
  - **center:** items are centered in the cross-axis.
  - **baseline:** items are aligned such as their baselines align. 
- **align-content:** This aligns a flex containerâ€™s lines within when there is extra space in the cross-axis, similar to how justify-content aligns individual items within the main-axis.
  - **flex-start / start:** items packed to the start of the container.
  - **flex-end / end:** items packed to the end of the container.
  - **center:** items centered in the container.
  - **space-between:** items evenly distributed; the first line is at the start of the container while the last one is at the end.
  - **space-around:** items evenly distributed with equal space around each line.
  - **space-evenly:** items are evenly distributed with equal space around them.
  - **stretch (default):** lines stretch to take up the remaining space.
  
**Properties for the Children (flex items):**
- **order:** By default, flex items are laid out in the source order. However, the order property controls the order in which they appear in the flex container.
- **flex-grow:** This defines the ability for a flex item to grow if necessary. It accepts a unitless value that serves as a proportion. It dictates what amount of the available space inside the flex container the item should take up.
- **flex-shrink:** This defines the ability for a flex item to shrink if necessary.
- **flex-basis:** This defines the default size of an element before the remaining space is distributed.
- **flex:** This is the shorthand for flex-grow, flex-shrink and flex-basis combined. The second and third parameters (flex-shrink and flex-basis) are optional. The default is 0 1 auto, but if you set it with a single number value, itâ€™s like 1 0.
- **align-self:** This allows the default alignment (or the one specified by align-items) to be overridden for individual flex items.

---

[home](/README.md) | [About me](/about-me.md) | [contact me](/contact-me.md)
# HTML Links, CSS Layout, JS Functions

## HTML links 

>**Writing Links**

Links are created using the `<a>` element. Users can click on anything
between the opening `<a>` tag and the closing `</a>` tag. You specify
which page you want to link to using the href attribute.

![how to write linke](./img/how-we-write-links.png)

>**pening Article Links in a New Window**

If you want a link to open in a new window, you can use the `target` attribute on the opening `<a>` tag. The value of this attribute should be `_blank` .

>**Relative URLs**

Relative URLs can be used when linking to pages within your own
website. They provide a shorthand way of telling the browser where to
find your files.

![relative urls](./img/relative-urls.png)

>**Email Links**

![email links](./img/email-links.png)

>**Linking to a Specific Part of the Same Page** 

![Linking to a Specific Part of the Same Page](./img/link-part-same-page.png)

>**Linking to a Specific Article Part of Another Page**

![Linking to a Specific Article Part of Another Page](./img/link-part-another-page.png)

---

## CSS Layout 

- CSS treats each HTML element as if it is in its own box. This box will either be a block-level box or an inline box.
    - Block-level box: starts on a new line. Examples include: <h1>, <p>, <ul>, and <li>.
    - Inline box: inline elements flow in between surrounding text. Examples include: <img>, <b>, and <i>.
- CSS has positioning schemes that allow you to control the layout of a page: normal flow, relative positioning, and absolute positioning. You specify the positioning scheme using the position property in CSS. You can also float elements using the float property.

- Normal flow: Every block-level element appears on a new line, causing each item to appear lower down the page than the previous one.
- Relative Positioning: This moves an element from the position it would be in normal flow, shifting it to the  top, right, bottom, or left of where it would have been placed. This does not affect the position of surrounding elements.
- Absolute positioning: This positions the element in relation to it's containing element, which means it's taken out of normal flow and move as users scroll up and down the page.
- Floating an element allows you to take that element out of normal flow and position it to the far left or right of a containing box. The floated element becomes a block-level element around which other content can flow.

- Different sized screens that show different amounts of information, so your design needs to be able to work on a range of different sized screens.

- Liquid layout designs stretch and contract as the user increases or decreases the size of their browser window. They tend to use percentages.

- Fixed width layout designs do not change size as the user increases or decreases the size of their browser window. Measurements tend to be given in pixels.

---

## JS Functions 

simply its bunsh of steps that work step by step to achive goal, and its reusable

## How to creat a Function :
first of all you need to start by calling `function`, then give it a name after space like `function sleep()` *follwd with prentheses, and finly we add the curly braces `function sleep(){}` and betwin them will have the task like `function sleep(){document.write('Heloo world')};`

## Calling a Function :
after creating the function it will stay there wating for call to start, and this happen with only 1 line! by caling the function name folowed with parantheses like: `sleep();`, after excuting the function it will countinue the code at the after the same calling line...

### Function witch need information:
sometimes the function needs specafic information to use in and it will be inside the paranthases acting like varubles only inside the function.. like: `function pluse(x, y){}`, and we must let th last step of the function in this case is to return the varubles like: `function pluse(x, y){(the steps); return x + y}`
and when we call that kind of functions we must to mention the informations value inside the paranthses like: `pluse(5, 6)`

<br>
<br>
<hr>

# Pair Programs :
simply “two heads are better than one”, the pair programs helps you improve the quality of your code produce

## How does it works :
the main idea depends on tow **Props**:
1. Driver :
is the programmer who is typing codes, Handling the “mechanics” of coding, manages the text editor, switching files, version control
the programmer also should had skills like: explain out loud what the code should do, listen to others’ guidance, read code that others have written, and write code themselves

2. Navigator :
who are uses their words to guide the Driver, thinks about the big picture,what comes next, how an algorithm might be converted in to code, while scanning for typos or bugs

## What Pair Programs provide to you?
- Greater efficiency
- Engaged collaboration
- Learning from fellow students
- More Social skills
- Job interview readiness
- Work environment readiness


---

[home](/README.md) | [About me](/about-me.md) | [contact me](/contact-me.md)
# HTML Lists, CSS Boxes, JS Control Flow

## no need to an intro!..
just go cheak :
[HTML In Few Lines (Read01)](https://3madov-77.github.io/Reading-Notes/class-01) & [HTML CSS JS In Parm Lines (Read02)](https://3madov-77.github.io/Reading-Notes/class-02)

<br>

# HTML Lists:
HTML provide 3 difreent kinds of lists wich is:
1. Ordered lists :
you can use the tag `<ol>` to create one and use `<li>` tag for each item in the list it should looks like:

![cap](https://3madov-77.github.io/Reading-Notes/Resorses/Capture03-1.PNG)

2. Unordered lists :
as in orderd list you can use the tag `<ul>` to create one and also use `<li>` tag for each item in the list it should looks like:

![cap](https://3madov-77.github.io/Reading-Notes/Resorses/Capture03-2.PNG)

3. Definition lists :
use the tag `<dl>` to create one and use `<dt>` tag to create  the defintion term and use `<dd>` tag for each content defention it should looks like:
![cap](https://3madov-77.github.io/Reading-Notes/Resorses/Capture03-3.PNG)

> you can create Nested lists by adding second list inside an `<li>` element to create a sublist or nested list

<br>
<hr>

### as you see previosly in (CSS) topic that css treat every elemnt in HTML as it lives in own *box*, so you can set several properties that affect the appearance of these boxes lets talk littel bit about it :

# Box Dimensions :

## width & height:
well .. luckly by defultthe browser box is sized just big enough to hold its contents, But you can use **width & height** if you want to specfie size you want
width & height uses pixels, percentages, or ems to controle their size like:

![cap](https://3madov-77.github.io/Reading-Notes/Resorses/Capture03-4.PNG)

### Limiting Width :
***min-width, max-width***
you can use `min-width` property specifies the smallest size a box can be displayed at when the browser window is narrow
and also max-width property indicates the maximum width a box can stretch to when the browser window is wide
and write it like:

![cap](https://3madov-77.github.io/Reading-Notes/Resorses/Capture03-5.PNG)

### Limiting Hight :
as *Limiting Width* you can use `min-hight` property specifies the smallest hight of the box, can be displayed at when the browser window is narrow
and also max-hight property indicates the maximum hight a box can stretch to when the browser window is wide
and write it like:

![cap](https://3madov-77.github.io/Reading-Notes/Resorses/Capture03-6.PNG)

## Overflowing Content :
### overflow :
tells the
browser what to do if the content contained within a box is larger than the box itself. It can have one of two values:
- hidden
- scroll
witch adds a scrollbar to the box so that users can scroll to see the missing content

![cap](https://3madov-77.github.io/Reading-Notes/Resorses/Capture03-7.PNG)

## Border, Padding & Margen :
notice the **Capture** :

![cap](https://3madov-77.github.io/Reading-Notes/Resorses/Capture03-8.PNG)

*it also can slove to you ***White space & Vertical Margin**
*you can specify padding or margins for ***top or right or bottom or left*** or even use it in same patern in **shorthand way** like:
`padding: (T)10px (R)5px (B)3px (L)1px;`

![cap](https://3madov-77.github.io/Reading-Notes/Resorses/Capture03-9.PNG)

<br>

### Border Width :

***border-width*** we youse this property is used to control the width of a border, it uses values "thin, medium, thick"
> You cannot use percentages with this property
also You can control the individual size of borders using four separate properties `border-top-width, border-right-width, border-bottom-width, border-left-width`
Or just specify different widths for the four border values in one property, like :
`border-width: 2px 1px 1px 2px;`
*The values here appear in clockwise order: top, right, bottom, left*

<br>

### Border Style :
There is alot of styles you can usedfor the border like:

![cap](https://3madov-77.github.io/Reading-Notes/Resorses/Capture03-10.PNG)

<br>

### Border Color :
Also there is alot of colors to use and alot of ways to do that, also you can specify witch side of the border you want to color by using : `border-top-color, border-right-color, border-bottom-color, border-left-color`

**Shorthand** : by only typing `border:` then add the *width*, *style* and *color* ...

### Border Images:
**border-image**
use this proparity to applies an image to the border of any box by slices it into nine pieces `>>` ![cap](https://3madov-77.github.io/Reading-Notes/Resorses/Capture03-12.PNG) and taking 18 pixels from each corner to place an entire circle in each corner, it requires three pieces of information:
1. The URL of the image
2. Where to slice the image
3. What to do with the straight edges, witch take vlues: `stretch, repeat, round,`
it writes like:

![cap](https://3madov-77.github.io/Reading-Notes/Resorses/Capture03-13.PNG)


<br>


## Centering Content :
to center a box on the page, you need to set a width for the box (otherwise it will take up the full width of the page), Once you have specified the width of the box, setting the left and right margins to auto will make the browser put an equal **gap** on each side of the box and thats it..

![cap](https://3madov-77.github.io/Reading-Notes/Resorses/Capture03-11.PNG)

<br>


## Inline/Block :
***display*** witch allows you to turn an inline element into a **block-level** element, and uses values :

1. **inline** :witch causes a block-level element to act like an inline element
2. **block** :witch causes an inline element to act like a block-level element
3. **inline-block** :witch causes a block-level element to flow like an inline element, while retaining other features of a block-level element
4. **none** :witch hides an element from the page

<br>


## Hiding Boxes :
**visibility**
use this property with values : `hidden & visible`

<br>


## Box Shadows :
**box-shadow**
this proparity allows you to add a drop shadow around a box, it must uese tow vlues color and one of:
- `Horizontal offset` :Negative values position theshadow to the left of the box
- Vertical offset :Negative values position the shadow to the top of the box
- Blur distance :If omitted, the shadow is a solid line like a border
- Spread of shadow :If used, a positive value will cause the shadow to expand in all directions, and a negative value will make it contract
it must look like: `box-shadow: 5px 5px 5px #777777;}`

<br>


## Rounded Corners :
**border-radius**
use this proparity to make the corners mre rounded, also you can specify witch corner to rounded by useing: `border-top-right-radius, border-bottom-right-radius, border-bottom-left-radius, border-top-left-radius`
also you can use shorthand way with it like :`border-radius: 5px, 10px,
5px, 10px;`
you can also create ***Elliptical Shpes*** with this proparty like :

![cap](https://3madov-77.github.io/Reading-Notes/Resorses/Capture03-14.PNG)

<br>
<br>
<hr>

# JS :

<br>

# Loops :
its another kind of cheak conditions, if it returns **true** the code after will run, then it will recheak again if it is still return true and keep cheak and run until returns **flse**
and there is 3 typs of loops:
![cap](https://3madov-77.github.io/learning-journal/New%20folder/Capture-8-1b.PNG)

### 1. FOR : it is usually a counter which is used to tell how many times loop should run..

### 2. WHILE : you can use while if you dont know how many times the code will keep loop, it will keep loop until the condition is true and its like :

![cap](https://3madov-77.github.io/learning-journal/New%20folder/Capture-8-8b.PNG)

### 3. DO WHILE : its same of ehile loop but in difference: it will always run thr statments inside the curly braces at least once, even if the condation evaluates to false..

## Loops Counters :
when the loop used to counter for how many times it should repeat, so the counters loops must had 3 main sections:
1. **Initialization** : wich it basicly creating the varuble inside the loop

![cap](https://3madov-77.github.io/learning-journal/New%20folder/Capture-8-2b.PNG)

2. **Condition** : the loop should continue to run until the counter reaches specified number

![cap](https://3madov-77.github.io/learning-journal/New%20folder/Capture-8-3b.PNG)

3. **Update** : evrey time the has run the statment in the curly braces, it will adds the update to the varuble (it is usualy adds 1) like:

![cap](https://3madov-77.github.io/learning-journal/New%20folder/Capture-8-4b.PNG)

So simply looping be somthing like :

![cap](https://3madov-77.github.io/Reading-Notes/Resorses/Capture03-15.PNG)


---

[home](/README.md) | [About me](/about-me.md) | [contact me](/contact-me.md)
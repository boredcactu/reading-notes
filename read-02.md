
# jQuery, Events, and The DOM

## JQUERY
The examples in this chapter
revisit the list application used in
the previous two chapters, and
they will use jQuery to update
the content of the page. 
`<script src="j s/ jquery-1 .11. 0 .js "></script> `
### WHY USE JQUERY?
jQuery doesn't do anything you cannot achieve with pure JavaScript.
It is just a JavaScript file but estimates show it has been used on over a
quarter of the sites on the web, because it makes coding simpler. 

jQuery's motto is "Write less, do more," because it allows you to achieve
the same goals but in fewer lines of code than you would need to write
with plain JavaScript. 

### FINDING ELEMENTS
Using jQuery, you usually select elements
using CSS-style selectors. It also offers some
extra selectors, noted below with a 'jQ'. 

### LOOPING :
In plain JavaScript, if you wanted
to do the same thing to several
elements, you would need to
write code to loop through all of
the elements you selected. 
`$('l i em') .addClass('seasonal ') ;`
`$( ' li .hot') .addClass('favorite'); `

### CHAINING 
`$( 'l i [i d!="one"] ') . hide() .delay(SOO) . fadeln(1400); `
If you want to use more than
one jQuery method on the same
selection of elements, you can
list several methods at a time
using dot notation to separate
each one, as shown below

### GETTING ELEMENT CONTENT

The â€¢ htm 1 () and â€¢ text () methods both retrieve and update the content
of elements. This page will focus on how to retrieve element content. To
learn how to update element content. 

### GETTING AT CONTENT
On this page you can see variations on how the . html() and . text()
methods are used on the same list (depending on whether `<ul >`or `<l i >`
elements are used in the selector). 
`var $listHTML = ${'ul') . html(};`
`$ ( 'ul '). append($1 i stHTML);`

### UPDATING ELEMENTS 
Here are four methods that update the content
of all elements in a jQuery selection . 

### BASIC EFFECTS 
In this example, it appears as
if list items are faded into view
when the page loads. Each item
is faded out when it is clicked on. 
`$(function() {`
`$('h2').hide().slideDown();`
`var $li = $('li');`
`$li.hide().each{function(index) {`
`2 $(this).delay(700 * index) .fadeln(?OO);`
`} ) ;`
`3`
`$li.on('click', function()`
`$(this) .fade0ut(700);`
`} ) ;`
`} ) ; `

### ANIMATING CSS

The .animate() method allows you to create
some of your own effects and animations by
changing CSS properties. 

`$(function() {`
`$(' l i').on( 'click', function() {`
`~ $(this).animate({`
`~r opacity : 0.0,`
`~ paddingleft: '+=80'`
`@ } , 500, function() {`
`~ $(this).remove();`
`} ) ;`
`} ) ;`
`} ) ; `

All list items are selected and,
when a user clicks on one of
them, an anonymous function
runs. Inside it, $(this) creates
a new jQuery object holding
the element the user clicked on.
The .animate() method is then
called on that jQuery object. 

### TRAVERSING THE DOM
When you have made a jQuery selection, you
can use these methods to access other element
nodes relative to the initial selection. 

# 6 Reasons for Pair Programming
Iterative loops. Code reviews. Fast feedback. Error checking and linting. These are software engineering practices that have proven to dramatically improve the quality of code developers produce. What if you can could get all of this, instantaneously, while typing code line by line and character by character? You can, with pair programming, a technique common to many agile work environments.

### How does pair programming work?

While there are many different styles, pair programming commonly involves two roles: the Driver and the Navigator. The Driver is the programmer who is typing and the only one whose hands are on the keyboard. Handling the â€œmechanicsâ€ of coding, the Driver manages the text editor, switching files, version control, andâ€”of course writingâ€”code. The Navigator uses their words to guide the Driver but does not provide any direct input to the computer. The Navigator thinks about the big picture, what comes next, how an algorithm might be converted in to code, while scanning for typos or bugs. The Navigator might also utilize their computer as a second screen to look up solutions and documentation, but should not be writing any code.

### Why pair program?

While learning to code, developers likely study several programming languages. Similar to a foreign language class, there are four fundamental skills that help anyone learn a new language: Listening: hearing and interpreting the vocabulary Speaking: using the correct words to communicate an idea Reading: understanding what written language intends to convey Writing: producing from scratch a meaningful

* 1. Greater efficiency
* 2. Engaged collaboration
* 3. Learning from fellow students
* 4. Social skills
* 5. Job interview readiness
* 6. Work environment readiness

---

[home](/README.md) | [About me](/about-me.md) | [contact me](/contact-me.md)
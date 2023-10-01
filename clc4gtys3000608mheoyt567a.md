---
title: "CSS Selectors : The Sorting Hat & much more"
seoTitle: "CSS, CSS Selectors, ineuron, pseudo-elements"
datePublished: Mon Dec 26 2022 07:16:10 GMT+0000 (Coordinated Universal Time)
cuid: clc4gtys3000608mheoyt567a
slug: css-selectors-the-sorting-hat-much-more
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1670691734061/CHcfz-Q1p.gif
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1672038326877/f6847129-b3ed-48e2-99ec-722ccbbb93a2.avif
tags: ineuron, hiteshchoudharylco, iwritecode, ineuron-hiteshchaudhary-webdev-javascript-lco-learncodeonline-lco-css-learncodeonline-cssselectors-hiteshchoudharylco-code-with-hitesh-choudhary, iwritecode-hiteshchoudhary-lco-markdown-git-github

---

Hola! Coders 👨‍💻 Hope you all are doing well, In this article, I'm going to tell, about all the **CSS Selectors** with code snippets and examples, "**The Sorting Hat**" is a character mentioned in the novel by J.K Rowling "**The Harry Potter**" series that decides/selects which children should go into which Hogwarts house in according to their specific attributes similarly (but not exactly), CSS Selectors selects/decides/find HTML elements with specific attributes.

By entering **"Mark" into the** skin through spell - **Inline CSS**  
By distributing **"Poly juice Potion"** internally - **Internal CSS**  
Externally using Our **"Magic Wand"** - **External CSS**

# CSS Selectors :

## Overview

The sorting hat in the Harry Potter series appears when all the Hogwarts students are going to be selected for their Hogwarts house. The Sorting Hat decides/selects

### What is CSS?

The term "CSS" stands for **Cascading Style Sheets**, which are used to style Websites and are in charge of how landing pages appear in browser-reflective ways.

* CSS is a powerful magic word that may be used to alter the "**Graphical Appearance**" or GUI of Web Pages without using any CLI commands.
    
* On a website, it is in charge of **styling**, **resizing**, **positioning**, **colors**, **responsiveness**, and more.
    

When we discuss a website's "**Responsiveness**," CSS is what makes that possible. Style switching between desktop, tablet, and mobile versions is possible with it. To know more about how it will function, [**"Magic that makes HTML more Handsome"**](https://arpitdubey.hashnode.dev/magic-that-makes-html-more-handsome#heading-what-is-css) please read my blog and Kindly click on read more. [Read More](https://arpitdubey.hashnode.dev/magic-that-makes-html-more-handsome#heading-what-is-css)

#### The Anatomy of CSS Syntax:

```markdown

selector { property : value; }
```

![Selectors](https://i.imgur.com/H3hx2rW.png align="left")

Just as in English, we have grammatical rules that state where you should put commas, where you should have full stops, which words need to be capitalized, etc., all programming languages also have their particular syntax. Now, the first thing that you'll see in the **selector** then pair of **curly brackets** inside which your CSS rules going to reside.

The **selector is** just the **"WHO"** so, it tells it the "WHO" you want to **"modify" o**n your web page. it is `<h1> , <p> , <img>` whose style do you gonna change? background color, text color, and position. The next Part, for **"property"** is the **"WHAT"** like if you select `<h1>` as a selector then what about `<h1>`? do you want it blue or red? and To change it we have assigned some sort of values So, **"HOW"** do you want to change the background color of `H1`? for modifying any color or properties input we just give various values.

## What are Selectors in CSS?

Selectors for CSS are a component of CSS rules. It facilitates the **targeting of an HTML element** on a website. A pattern, series of elements, or other terms that specify which HTML elements should be chosen so that the CSS property values contained in the rule are applied to them.

In layman's terms, it is a means to pick anything using a specified class name, id, and special symbols that are associated with a specific attribute or HTML element, then apply styles to all of the matching items.

CSS Selectors CSS selectors are used to "find" (or select) the HTML elements you want to style.

We can divide CSS selectors into five categories:

* Simple selectors (select elements based on name, id, and class)
    
* Combinator selectors (select elements based on a specific relationship between them)
    
* Pseudo-class selectors (select elements based on a certain state)
    
* Pseudo-elements selectors (select and style a part of an element)
    
* Attribute selectors (select elements based on an attribute or attribute value)
    

# Types of Selectors?

1. Basic Selector
    
    * Universal Selector
        
    * Element Selector
        
    * Class Selector
        
    * ID Selector
        
2. Grouping Selector -Selector List
    
3. Combinators
    
    * Descendant Combinator
        
    * Child Combinator
        
    * General sibling combinator combinator
        
    * Adjacent sibling combinator combinator
        
4. Pseudo classes & Elements
    
    * root
        
    * hover
        
    * focus
        
    * active
        
    * enabled & disabled
        
    * last-child
        
    * nth-child
        
    * before & after
        
    * selection
        

## Basic Selector

### Universal Selector

* The CSS universal selectors are represented by the asterisk `(*)`. The entire HTML page with all of its elements can be chosen. The asterisk can also be used to pick a child object, followed by a selector. When we want to select every element on the page, this selector is helpful.
    

#### Example

```CSS
* {
      margin: 0;
      padding: 0;
      color: #fff;
      background: #000;
}
```

<iframe height="600" style="width:100%" src="https://codepen.io/aarpitdubey/embed/qBKKajJ?default-tab=html%2Cresult&editable=true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/qBKKajJ">
  Universal Selector</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### Element Selector

* Based on the **"element name (or tag)"**, such as h(1-6), div, span, etc., the element selector **chooses (or) selects (or) find (or) target** the HTML elements.
    

#### Example

```CSS
/*** Element Selector ***/
    h1, h3 {
      text-align:center;
    }
    
    img {
      border-radius:50%;
      width:400px;
    }
    
    b {
      color: red;
    }
 /*************************/
```

<iframe height="600" style="width:100%" src="https://codepen.io/aarpitdubey/embed/KKeegPM?default-tab=html%2Cresult&editable=true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/KKeegPM">
  Element Selector</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### Class Selector

* To apply styles to all of the matching elements, use the **class selector** to select (or) target (or) find all elements that have the supplied **class name and correspond to a specific attribute**.
    

#### Example

```CSS

   /*** Class Selector ***/

    .HarryWithHermione {
      background-color: #000;
      color: #fff;
      text-align:center;
    }
    
    .HarryDanceWithHermione {
      border-radius: 50%;
      width:400px;
    }

    /****************************/
```

<iframe height="600" style="width:100%" src="https://codepen.io/aarpitdubey/embed/QWxxGZZ?default-tab=html%2Cresult&editable=true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/QWxxGZZ">
  Class Selector</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### ID Selector

* Using the Id selector, you can only pick and apply styles to elements that have the given id. It is exclusive to a page and only applies to one element at most.
    
* In CSS, you only place a hashtag (#) before the element's ID to utilize an Id selector.
    

#### Example

```CSS

/******* ID Selector *******/
    
    #bodyID {
      background-color: #000;
      color:#fff;
      text-align: center;
    }
    #hermoine {
      border-radius:50%;
      width:400px;
    }
    
    /****************************/
```

<iframe height="600" style="width:100%" src="https://codepen.io/aarpitdubey/embed/xxzzgwE?default-tab=html%2Cresult&editable=true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/xxzzgwE">
  ID Selector</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## Grouping selector

### Selector list

The (",") selector is a grouping mechanism that picks up several selections and can simultaneously give them properties.

```CSS

p, span, .button {
  background-color: rgb(16, 16, 150);
  color: #fff;
}
```

<iframe height="800" style="width:100%" src="https://codepen.io/aarpitdubey/embed/RwJerLJ?default-tab=html%2Cresult&editable=true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/RwJerLJ">
  Selectorlist_</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

<iframe height="600" style="width:100%" src="https://codepen.io/aarpitdubey/embed/vYrrqZp?default-tab=html%2Cresult&editable=true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/vYrrqZp">
  Selector List : (
<h2>Combinators</h2>
<ul>
      <li>Descendent Combinator</li>
</ul>
<p>A single "  " (space) character is used to indicate it between two or more HTML elements, and it is used to pick an element that is nested inside of tags.</p>
<pre><code class="language-CSS">
  /*  Descendent Combinator */
    div span {
      color: gold;
      font-style: italic;
      font-size: 32px;
    }
<p>/***********************/</p></code></pre><p></p>
<iframe height="600" style="width:100%" src="https://codepen.io/aarpitdubey/embed/NWzEzYG?default-tab=html%2Cresult&editable=true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/NWzEzYG">
  Descendent Combinator</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe></a></iframe>

* Child combinators
    

It is denoted by the symbol "&gt;" which chooses one or more elements that are the initial element's direct children.

```CSS

 /*  Child Combinator */
    ul > li  {
        list-style: none; /* Remove the bullet point */
        margin: 20px;
        color: pink;
      font-weight: 800;
      font-size:24px;
}
```

<iframe height="600" style="width:100%" src="https://codepen.io/aarpitdubey/embed/ExRJezM?default-tab=html%2Cresult&editable=true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/ExRJezM">
  Child Combinators</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

* General sibling combinator
    

It chooses all elements that share a parent element and are next siblings to a given element (not necessarily immediately). It is symbolized by the character '~'.

```CSS

 /*  General sibling combinator  */

 .rocket > h4 ~ p  {
   color: blue;
   font-weight:800;
   font-size:24px;
   background-color: orange;
 }
```

<iframe height="600" style="width:100%" src="https://codepen.io/aarpitdubey/embed/zYaXbJz?default-tab=html%2Cresult&editable=true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/zYaXbJz">
  General sibling combinator </a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

* Adjacent sibling combinator
    

It is symbolized by the symbol +, which is used to choose an element that is present after + and that comes just after the element that is present before +.

```CSS
  /*  Adjacent sibling combinator  */
 .rocket > h4 + p.saffron {
   color: #FF9933;
   font-weight:800;
   font-size:24px;
   background-color: #FF9933;
 }
```

<iframe height="600" style="width:100%" src="https://codepen.io/aarpitdubey/embed/ExRJJgL?default-tab=html%2Cresult&editable=true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/ExRJJgL">
  Adjacent sibling combinator</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## Pseudo-classes

* **: root**
    
* `: root` CSS pseudo-class matches the root element of a tree representing the document. In HTML, the root represents the element and is identical to the selector HTML, except that its specificity is higher.
    

```CSS
  /*  :root  */
:root {
   --primary-color:rgb(31,170,89);
     background-color:var(--primary-color);
   font-size:18px;
 }
```

<iframe height="600" style="width:100%" src="https://codepen.io/aarpitdubey/embed/eYKaOVa?default-tab=html%2Cresult&editable=true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/eYKaOVa">
  : root</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

* **: hover**
    

When the mouse cursor is over a target element, it performs different/various effects are going to start happening.

```css
.style_prev_kit
{
    display:inline-block;
    border:0;
    width:196px;
    height:210px;
    position: relative;
    -webkit-transition: all 200ms ease-in;
    -webkit-transform: scale(1); 
    -ms-transition: all 200ms ease-in;
    -ms-transform: scale(1); 
    -moz-transition: all 200ms ease-in;
    -moz-transform: scale(1);
    transition: all 200ms ease-in;
    transform: scale(1);   

}
.style_prev_kit:hover
{
    box-shadow: 0px 0px 150px #000000;
    z-index: 2;
    -webkit-transition: all 200ms ease-in;
    -webkit-transform: scale(1.5);
    -ms-transition: all 200ms ease-in;
    -ms-transform: scale(1.5);   
    -moz-transition: all 200ms ease-in;
    -moz-transform: scale(1.5);
    transition: all 200ms ease-in;
    transform: scale(1.5);
}
```

<iframe height="600" style="width:100%" src="https://codepen.io/aarpitdubey/embed/gOjpVPM?default-tab=html%2Cresult&editable=true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/gOjpVPM">
  Untitled</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

* **:focus**
    
    It applies the required styling as stated when the target element gets focused.
    

### **Example**

```plaintext
input:focus {
  background-color: #b49ebe;
  border: 3px solid #7c6686;
}
```

* **: active**
    
    It is applied when we add styling to the target element in its active state i.e. when an action is performed on it like clicking.
    

```plaintext
button:active {
  background-color: #0f1f11;
  transform: scale(0.7);
}
```

* **:enable : disable**;
    
    Represents a user interface element that is in an enabled or disabled state.
    

```css
input:enabled {
    background-color: gold;
}

input:disabled {
  cursor: not-allowed;
}
```

* **:first-child**
    
    It will select the first specified element in the document and applies the required styling.
    

```css
li:first-child {
  margin: 10px;
  background-color: #42a192;
}
```

* **:last-child**
    
    It will select the last one of the specified element in the document and applies the required styling.
    

```css
li:last-child {
  margin: 10px;
  background-color: #42a192;
}
```

* **:nth-child**
    
    It is used to style some specific elements that follow a particular mathematical order.
    

```css
li:nth-child(-n+3) {
  margin-bottom: 1px;
  border: 2px solid #7c5306;
}
```

## **Pseudo-elements**

* **:: before:: after they** are often used to add cosmetic content to the first child of the selected element with the content property. They are inline by default. **:: before** is used to add content before the element and::after is used to add content after the element.
    

```css
p::before {
  content: "« Start »";
  color: Gree;
}

p::after {
  content: "« end »";
  color: red;
}
```

<iframe height="600" style="width:100%" src="https://codepen.io/aarpitdubey/embed/rNrOeGO?default-tab=html%2Cresult&editable=true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/rNrOeGO">
  Untitled</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

* **::selection**
    
    This is used to change the style of the selected text.
    

```css
p::selection {
  background-color: orange;
}
```

<iframe height="600" style="width:100%" src="https://codepen.io/aarpitdubey/embed/rNrOeGO?default-tab=html%2Cresult&editable=true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/rNrOeGO">
  Untitled</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1672039452032/457744d8-e86e-4d4e-a996-77ecf6f9eb9f.gif align="center")

Thank you for reading this Article.
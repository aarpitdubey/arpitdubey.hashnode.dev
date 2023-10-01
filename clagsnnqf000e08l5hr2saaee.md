---
title: "Magic that makes HTML more Handsome"
seoTitle: "#CSS, #CSS3,  #HTML, #WEB DEVELOPMENT, #MERN, #JAVASCRIPT, #MAGIC,"
datePublished: Mon Nov 14 2022 13:01:01 GMT+0000 (Coordinated Universal Time)
cuid: clagsnnqf000e08l5hr2saaee
slug: magic-that-makes-html-more-handsome
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1668430616998/ZgG-cXc5T.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1668430786004/6wA8Sq_JO.jpeg
tags: css, web-development, ineuron, iwritecode, ineuron-hiteshchaudhary-webdev-javascript-lco-learncodeonline-lco-css-learncodeonline-cssselectors-hiteshchoudharylco-code-with-hitesh-choudhary

---

Hola! Coders 👨‍💻 Hope you all are doing good, In this article I'm going to tell about the Magical spell which will makes the HTML page more Handsome or Beautiful irrespective of it's HTML author's gender 😄 let's see what that's magic spell is and how it's going to work.

## Magic Spell

#### *Overview :*

> The magic spell here is known as **C**ascading **S**tyle **S**heet (CSS). We can perform the magic rituals by three different ways: 
1. By Giving "Mark" directly through spell  -  **Inline CSS**
2. By Giving "Polyjuice Potion" internally    -  **Internal CSS**
3. Through Our "Magic Wand" externally   -  **External CSS**

Now, we understand that to beautify the HTML document we have to use some magic that transform the frog into a handsome Prince and It can be performed in three ways using Inline, Internal and external CSS but Still we don't know what is CSS? how we can actually implement it in real life, out of the fictitious world. 

## What is CSS? 

#### *Introduction :*

> As we know, the **CSS** stands for **Cascading Style sheets** and, it is used to styling the Web page and responsible for the appearances of landing pages reflects on the browser.

- CSS is the magical spell which can be use to manipulate the **"Graphical looks"** or **GUI** of the Web Pages.  
- It is responsible for the styling, re-sizing, positioning, coloring, responsiveness and more on a website. 

As we talk about the "Responsiveness" of a website, CSS is the key to make that possible. It can be use to style shift between Desktop, Tablet and Mobile versions. Let us see **how** it will going to work

## How?

> There are three ways as we discussed previously, about inline CSS, internal CSS and external CSS, using these three methods we can add the CSS file or it's code-snippets on a HTML document. It can be achieve by manipulating HTML elements such as HTML tags etc., 

### Types of method to link CSS with HTML document

We can inject the CSS code within the HTML element as an attribute. <br> ```<tagname style="....."></tagname>```

**1. Inline Style: ** We can write CSS rules directly inside an HTML element, with the style attribute. In this method, we define the CSS rules directly inside the tag and don’t need to create a class for it.

```CSS
 <p style="color: blue; font-size: 22px;"> I'm a Text </p> ```

> **Note :** *This approach is not an example of clean code, SEO ranking problems, increase page loading time, slow down loading speed  and it’s not recommended to use.*

<iframe height="300" style="width: 100%;" scrolling="no" title="inline CSS" src="https://codepen.io/aarpitdubey/embed/MWXoEGq?default-tab=result&editable=true" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/MWXoEGq">
  inline CSS</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

As an internal CSS in tag :<br>&nbsp; &nbsp; &nbsp; &nbsp;```<style>```<br>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  .... <br> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  .... <br>
&nbsp; &nbsp; &nbsp; &nbsp; ```</style>```

**2. Internal CSS: ** Another way where we can write the CSS code in side```<style>``` tag in HTML., This will keep the HTML code directly inside the HTML file rather than in a separate file.

``` CSS
<style>
  p {  
    color: red;
  }
</style>
<body>
  <p> I'm a Text </p>
</body> ```

<iframe height="300" style="width: 100%;" scrolling="no" title="Internal CSS" src="https://codepen.io/aarpitdubey/embed/OJEgOoB?default-tab=result&editable=true" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/OJEgOoB">
  Internal CSS</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

Using external CSS, through linking another css file using ```<link href="style.css">```

**3. External CSS File : ** Keeping CSS code in a separate file is the best practice, In real world file structure has some convention which every developer has to follow and keeping every files separate and in modular structure are considered as the good programming practices.

Here, we can create a separate CSS file with an extension of ```.css``` and include it to HTML using ```<link href="style.css">``` tag. For example:
we can create ```style.css```, we can write our CSS code:

``` CSS

p {  
  color: red;
}
```
Then we can import ```style.css``` to HTML with a ```<link>``` tag like below:

```
<head>
   <link rel="stylesheet" href="style.css">
 </head>
<body>

 <p> I'm a Text </p>

</body>
```
So now the HTML file has the CSS code and the changes will apply to the elements.

<iframe height="300" style="width: 100%;" scrolling="no" title="External CSS" src="https://codepen.io/aarpitdubey/embed/rNKwYbL?default-tab=result&editable=true" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/rNKwYbL">
  External CSS</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## Conclusion :

> CSS is an essential part of Full Stack WEB Development. In this article, we learn
* CSS is used to give a better UI (User Interface) to HTML document or a website.
* Responsiveness of Website according to the size of device is possible because of CSS.
* CSS can be applied to HTML document using three ways: Using Inline CSS, Internal CSS and, 
External CSS.
* We come to know what is Inline CSS, Internal CSS and, External CSS with examples for each.
* We come to know what are the Drawbacks of using Inline CSS.
* We come to know Which method is preferred by Web Developers and Good Practices.
  
I tried to explain in a Layman's terminology but there are much more, some Advanced CSS and more additional functionalities. Asks as much question and do practice about it and don't hesitate to ask questions below in the comment section.
<br>

![hp_css.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1668430440922/SXGUzqCul.jpg align="left")

There are many other rules and features to explore in the world of CSS. I will be covering them in my following articles.
Thank you.
                         
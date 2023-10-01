---
title: "The God Father of WEB: Secret Sauce behind Websites"
seoTitle: "HTML, Basic of HTML, Godfather of Web, html, heading tags, links, html"
datePublished: Wed Nov 16 2022 12:40:05 GMT+0000 (Coordinated Universal Time)
cuid: clajmsfy3000608jn4j2bg256
slug: the-god-father-of-web-secret-sauce-behind-websites
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1668575989653/pm1S58Qbz.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1668602266629/ftmCNR7qN.avif
tags: ineuron, ineuron-hiteshchaudhary-webdev-javascript-lco-learncodeonline, iwritecode, ineuron-hiteshchaudhary-webdev-javascript-lco-learncodeonline-lco-css-learncodeonline-cssselectors-hiteshchoudharylco-code-with-hitesh-choudhary, iwritecode-hiteshchoudhary-lco-markdown-git-github

---

## HTML

#### An Overview:

> HTML is an acronym used for the **H**yper **T**ext **M**arkup **L**anguage. <br><br>
It is **Browser Understandable Language**, a **Scripting Language** and, **Markup Language** but it can't be considered as a Programming Language.  <br><br>
Currently, HTML - 5 is in use but many other HTML version are still available in HTML archive. <br><br>
HTML is use to **provide proper structuring and give meaning** to all the tags, linked css, javascript etc., elements in a document. <br>Entire Web is depended on HTML <br><br>
HTML is the **Building Block** of the Web

#### Anatomy of an HTML element

let's explore the HTML tag using ```<p> ... </p>``` :

![Anatomy of an HTML element]( https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started/grumpy-cat-small.png )

 * **The opening tag : ** *This consists of the name of the element (in this example, *p* for paragraph), wrapped in opening and closing angle brackets.* 

* **Content :** *Any thing which is written after the opening tag and before the closing tag, is called as Content of that tag.*




### Markup Language : 
Any symbol or Character that you insert at certain place in a text file or document is known as Markup. The Language which use such Markup's, symbol's or character's is called Markup Language. HTML have tags for defining the meaning and structure of web content besides HTML are generally used to describe a web page's appearance/presentation (CSS) or functionality/behavior (JavaScript).

HTML uses "markup" to annotate text, image, and other content for display in a web browser. It includes some special "elements" or HTML elements or HTML tags.

#### How to write first HTML file
To write your first HTML file, you need an HTML document, which is a document a ```.html``` or ```.htm``` extension. You can use editors like VS Code, Sublime Text, Atom, Notepad++, etc.,

### Emmet :

Emmet is a powerful extension which provides boilerplate or pre-coded code snippets. 

```!``` + ```tab``` can gives whole HTML5 boilerplate code snippet on the text editor.

![emmet.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1668536958742/2-F7zazww.gif align="left")

It allows us to write **HTML components as if they were CSS selectors, CSS styles with abbreviations** and also gives us access to **a collection of keyboard shortcuts to manipulate** and **navigate** through the code. EMMET is **already present in most modern editors**, such as **VSCODE**, not being necessary its installation. In these cases, **just start writing**. If your editor don’t have it by default, just download and install the plugin.

#### Text
 It is a unique element which doesn't require an opening or closing tag
to be displayed on the browser screen.

<iframe height="300" style="width: 100%;" scrolling="no" title="HTML ELEMENT - TEXT" src="https://codepen.io/aarpitdubey/embed/XWYaoLe?default-tab=html%2Cresult&editable=true" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/XWYaoLe">
  HTML ELEMENT - TEXT</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

As, I just type
```Hola! coders, "I writing the HTML element Text over the browser screen"``` but you manupulate/change the text for better understanding.

#### HTML Structure 

```
<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width" />
    <title>Arpit Dubey describing about HTML Structure</title>
  </head>
  <body>
    <img src="images/firefox-icon.png" alt="My test image" />
  </body>
</html>

```
let's us know about the tag used : 

- ```<!DOCTYPE html>``` : It is used to link to a set of rules that the HTML page had to follow to be considered a good HTML.

- ```<html lang="en-US"></html>``` : It wraps all the content on the entire page and also known as the root element. It also includes the *lang* attribute, setting this as the primary language of the document.

- ```<head></head>``` :  It act like  a container for all the stuff you want to include on the HTML page that isn't the content you are showing to your page's viewers. 
CSS for styling content, character set declarations, Meta tags (SEO purpose) and, more.

- ```<meta charset="utf-8">``` :  It sets the character set, document should use to **utf-8** which includes most characters from the vast majority of written languages. 

- ```<meta name="view port" content="width=device-width">``` : It ensures that the web page renders at the width of view port, preventing mobile browsers from rendering pages wider than the view port and the shrinking them down. 

- ```<title></title>``` : It sets the title of your page, which appears in the browser tab of the page is loaded in, it is also used to describe the page when you bookmark/favorite it.

- ```<body></body>``` : It contains all the content that you want to show to web users when they visit your page, whether that's text, images, videos, games, playable audio tracks, or whatever else.

> **Note :** Meta tags are use to ensuring that search engines know what your content is about and using such meta description ranking of the website get improved. So these are used for SEO purposes.

#### Images 
For displaying images on the screen of browser ```<img>``` tag is used.

<iframe height="300" style="width: 100%;" scrolling="no" title="HTML Element - image" src="https://codepen.io/aarpitdubey/embed/YzvxMmd?default-tab=html%2Cresult&editable=true&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/YzvxMmd">
  HTML Element - image</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

```<img src=" ... " alt=" ... " >``` it embeds an imgae into our web page in the position it appears. It does it via the ```src``` (source) attribute, which contain the path to that image file.

** ```alt``` (alternative) attribute :** In the alt attribute, you specify descriptive text for users who cannot see the image, possibly because of the following reasons:

**1. Visually impaired : ** Users with significant visual impairments often use tools called **screen readers** to read out the alt text to them if image is not displaying.

**2. Unwanted Error :** The keywords for alt text are "descriptive text". The alt text you write should provide the reader with enough information to have a good idea of what the image conveys if the image is failed to display may because of wrong image path etc.,

### Headings
Heading tags allow you to specify certain parts of content as Headings or the subheadings. It is are of 6 levels, from ```<h1>, <h2> ... <h6>``` 
```HTML
<h1> Main Heading </h1>
<h2> Top level Heading </h2>
<h3> Sub Heading </h3>
<h4> Sub Sub Heading </h4>
<h5> Sub Sub Sub Heading </h5>
<h6> Sub Sub Sub Sub Heading </h6>
```

<iframe height="300" style="width: 100%;" scrolling="no" title="HTML Element - Headings" src="https://codepen.io/aarpitdubey/embed/QWxMRXO?default-tab=html%2Cresult&editable=true&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/QWxMRXO">
  HTML Element - Headings</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

> **Note :** You'll see that your heading level 1 has an implicit style. Don't use heading elements to make text bigger or bold, because they are used for accessibility and other reasons such as SEO. Try to create a meaningful sequence of headings on your pages, without skipping levels.

### Paragraphs

```<p>``` tag are used for containing paragraphs of text; it is the most generally used tags which is frequently used by Web Developers

``` HTML
<p> Hola! coders I'm your Paragraph Tag </p>

```

<iframe height="300" style="width: 100%;" scrolling="no" title="HTML Element - Paragraph tag" src="https://codepen.io/aarpitdubey/embed/ExRvBNB?default-tab=html%2Cresult&editable=true&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/ExRvBNB">
  HTML Element - Paragraph tag</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### Lists

To display the HTML content in a listed format, lists are commonly used. To make list it consist of at least two elements. There are two type f lists Ordered and Unordered list.


**Unordered lists** where the order or sequencing of list items doesn't matter, such as shopping list. List items are wrapped in ``` <ul> ``` tag.

```HTML
  <ul>
      <li> item 1 </li>
      <li> item 2 </li>
 <ul>
```

<iframe height="300" style="width: 100%;" scrolling="no" title="Unordered List" src="https://codepen.io/aarpitdubey/embed/QWxMXZJ?default-tab=html%2Cresult&editable=true&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/QWxMXZJ">
  Unordered List</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

**Ordered lists** are lists where the order of list items does matter, such as a recipe or steps to prepare a recipe. List items are wrapped in an ``` <ol> ``` tag.

```HTML
  <ol>
      <li> item 1 </li>
      <li> item 2 </li>
 <ol>
```

<iframe height="300" style="width: 100%;" scrolling="no" title="Ordered List" src="https://codepen.io/aarpitdubey/embed/BaVdXvg?default-tab=html%2Cresult&editable=true&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/BaVdXvg">
  Ordered List</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>


### Links

Links are the most crucial part of a HTML document because to create a **"Hyper Text"** we required links to connect them.
**Hyper Text** are those text present in the HTML document which connect or link multiple pages together. 

```<a>``` tag "a" being the short form for "anchor".  To make text as hyper text you have to insert paragraph content within the ```<a> Here </a>``` tag.

Example :

```HTML
<a href=" ">Home Page</a>
  
```

fill ```href=" "``` with the URL link you want to redirect after clicking the hyper text.

```HTML
<a href="https://www.linkedin.com/in/aarpitdubey/">Arpit Dubey LinkedIn 
 Profile</a>

<a href="https://github.com/aarpitdubey">Arpit Dubey Github Profile</a>
  
```

<iframe height="300" style="width: 100%;" scrolling="no" title="Untitled" src="https://codepen.io/aarpitdubey/embed/ZERXzVo?default-tab=html%2Cresult&editable=true&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/aarpitdubey/pen/ZERXzVo">
  Untitled</a> by aarpitdubey (<a href="https://codepen.io/aarpitdubey">@aarpitdubey</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

<hr> 

## Conclusion 

We can see HTML is still widely used over the Web for Development and having more than 50% of websites which are build using HTML.

We learn many HTML elements and Now let's talk about Flutter

While Flutter web may be a good solution for web apps that are UI-heavy, it is not well suited for a blog or a website such as hashnode itself.

Tim Sneath (product manager for Flutter) says so himself:

<iframe id="twitter-widget-0" scrolling="no" frameborder="0" allowtransparency="true" allowfullscreen="true" class="" style="position: static; visibility: visible; width: 1000px; height: 435px; display: block; flex-grow: 1;" title="Twitter Tweet" src="https://platform.twitter.com/embed/Tweet.html?dnt=false&amp;embedId=twitter-widget-0&amp;features=eyJ0ZndfdGltZWxpbmVfbGlzdCI6eyJidWNrZXQiOlsibGlua3RyLmVlIiwidHIuZWUiLCJ0ZXJyYS5jb20uYnIiLCJ3d3cubGlua3RyLmVlIiwid3d3LnRyLmVlIiwid3d3LnRlcnJhLmNvbS5iciJdLCJ2ZXJzaW9uIjpudWxsfSwidGZ3X2hvcml6b25fdGltZWxpbmVfMTIwMzQiOnsiYnVja2V0IjoidHJlYXRtZW50IiwidmVyc2lvbiI6bnVsbH0sInRmd190d2VldF9lZGl0X2JhY2tlbmQiOnsiYnVja2V0Ijoib24iLCJ2ZXJzaW9uIjpudWxsfSwidGZ3X3JlZnNyY19zZXNzaW9uIjp7ImJ1Y2tldCI6Im9uIiwidmVyc2lvbiI6bnVsbH0sInRmd19jaGluX3BpbGxzXzE0NzQxIjp7ImJ1Y2tldCI6ImNvbG9yX2ljb25zIiwidmVyc2lvbiI6bnVsbH0sInRmd190d2VldF9yZXN1bHRfbWlncmF0aW9uXzEzOTc5Ijp7ImJ1Y2tldCI6InR3ZWV0X3Jlc3VsdCIsInZlcnNpb24iOm51bGx9LCJ0Zndfc2Vuc2l0aXZlX21lZGlhX2ludGVyc3RpdGlhbF8xMzk2MyI6eyJidWNrZXQiOiJpbnRlcnN0aXRpYWwiLCJ2ZXJzaW9uIjpudWxsfSwidGZ3X2V4cGVyaW1lbnRzX2Nvb2tpZV9leHBpcmF0aW9uIjp7ImJ1Y2tldCI6MTIwOTYwMCwidmVyc2lvbiI6bnVsbH0sInRmd19kdXBsaWNhdGVfc2NyaWJlc190b19zZXR0aW5ncyI6eyJidWNrZXQiOiJvbiIsInZlcnNpb24iOm51bGx9LCJ0ZndfdmlkZW9faGxzX2R5bmFtaWNfbWFuaWZlc3RzXzE1MDgyIjp7ImJ1Y2tldCI6InRydWVfYml0cmF0ZSIsInZlcnNpb24iOm51bGx9LCJ0Zndfc2hvd19ibHVlX3ZlcmlmaWVkX2JhZGdlIjp7ImJ1Y2tldCI6Im9uIiwidmVyc2lvbiI6bnVsbH0sInRmd190d2VldF9lZGl0X2Zyb250ZW5kIjp7ImJ1Y2tldCI6Im9uIiwidmVyc2lvbiI6bnVsbH19&amp;frame=false&amp;hideCard=false&amp;hideThread=false&amp;id=1460464879404388353&amp;lang=en&amp;origin=https%3A%2F%2Fcodewithandrea.com%2Fvideos%2Fflutter-web-html-css-js-performance-comparison%2F&amp;sessionId=b0357a19de27546a449108dcad8c88a5eb997b1c&amp;theme=light&amp;widgetsVersion=a3525f077c700%3A1667415560940&amp;width=550px" data-tweet-id="1460464879404388353" scrolling="no"></iframe>

So, HTML is still Considered as the **The GodFather of WEB**



![ty.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1668602047723/xRbI3ni_9.jpg align="left")








---
layout: post
title: Common HTML tags
category: HTML
tags: HTML
published: true
---
Here are some of the most common HTML tags and their uses.



|    Tags for document structure   | Usage |
| ---       |    ---   |
| `<!DOCTYPE HTML>`<br>`<html lang='en'></html>`| Used to specify the document is in html. <br> Used to specify the language is English.        |
| `<head>`<br>&emsp;`<meta charset="utf-8"/>`<br>&emsp;`<title></title>`<br>&emsp;`<link></link>`<br>&emsp;`<script></script>`<br>`</head>`   | The head tag is used to contain all the head elements <br>e.g. link to stylesheets, title, meta, linke to external CDNs.       |
| `<header></header>` | Is used for headers as seen in articles. <br> The likes of a newspaper header.|
|`<body></body>` | Body of the article or webpage. |
|`<div></div>` | A general purpose container for other elements.|
|`<h1></h1>` | Heading tag, used to segregate the different sections <br> or sub-sections of an article.|
| `<p></p>` | Used to denote a paragraph.|
| `<br>` | Used to break the line.|
|`<hr/>` | Used to display a horizontal line in the document.|
|`<blockquote></blockquote>` | For creating quotes on the page.|
|`<!-- -->` | For comments.|
|`<main></main>`<br>`<header></header>`<br>`<footer></footer>`<br>`<nav></nav>`<br>`<video></video>`<br>`<article></article>`<br>`<section></section>`| Some HTML 5 elements that give a descriptive <br> structure to HTML and help with SEO.

|    Tags for adding images and links   | Usage |
| ---       |    ---   |
|`<img alt="relaxing cat" src="https://www.freecatphotoapp.com/your-image.jpg">`| All img elements must have an alt attribute. The text inside an alt attribute <br> is used for screen readers to improve accessibility and is displayed if hte image fails to load.|
|`<a href="https://www.freecodecamplorg">this links to freecodecamp.org</a>` <br><br> `<a href="https://www.freecodecamp.org" target="_blank"> ...</a>` | Anchor elements are used to link to content outside of the webpage and has an href attribute. <br><br> The "_blank" target attribute tells the browser to open the link in a new tab.|
|`<a href="#contacts-header">Contacts</a>`<br>...<br>`<h2 id="contacts-header">Contacts</h2>`|You can also use the `<a>` tag to link to an internal section of the page through id attributes.|
|`<a href="#"><img src="https://www.bit.ly/fcc-running-cats"` <br> `alt="Three kittens running towards the camera."></a>` | You can turn an image into a link by nesting it in an `<a>` tag. A "#" in the href makes it a dead link.|

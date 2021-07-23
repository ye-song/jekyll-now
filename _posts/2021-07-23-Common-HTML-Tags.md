---
layout: post
title: Common HTML tags
category: HTML
tags: HTML
published: true
---
<style>
  .table {
    font-family: Helvetica;
    border: px solid black;
    border-collapse: collapse;
    width: 100%;
  }
  .table th {
    padding-top: 12px;
    padding-bottom: 12px;
    text-align: center;
    color: white;
    background-color: #0d58e9;
  }
  .table td {
    padding: 5px;
  }
  .table tr:nth-child(even){background-color: #f2f2f2;}
  .table tr:hover {background-color: #ddd;}

  span.highlight {
    background: #ADD6FF;
  }

  span.begin {
    border-top-left-radius: 5px;
    border-bottom-left-radius: 5px;
  }

  span.end {
    border-top-right-radius: 5px;
    border-bottom-right-radius: 5px;
  }
</style>

Here are some of the most common HTML tags and their uses.

<table class="table">
  <tr>
    <th>Tags for document structure</th>
    <th>Usage</th>
  </tr>
  <tr>
    <td> &lt;!DOCTYPE HTML> <br> &lt;html lang='en'>&lt;/html> </td>
    <td> Used to specify the document is in html. <br> Used to specify the language is English. </td>
  </tr>
  <tr>
    <td> <span>&lt;head><br>&emsp;&lt;meta charset="utf-8"/><br>&emsp;&lt;title>&lt;/title><br>&emsp;&lt;link>&lt;/link><br>&emsp;&lt;script>&lt;/script><br>&lt;/head></span> </td>
    <td> The head tag is used to contain all the head elements <br>e.g. link to stylesheets, title, meta, link to external CDNs. </td>
  </tr>
  <tr>
    <td> &lt;header>&lt;/header>  </td>
    <td> Is used for headers as seen in articles. <br> The likes of a newspaper header. </td>
  </tr>
  <tr>
    <td> &lt;body>&lt;/body>  </td>
    <td> Body of the article or webpage. </td>
  </tr>
  <tr>
    <td> &lt;div>&lt;/div>  </td>
    <td> A general purpose container for other elements. </td>
  </tr>
  <tr>
    <td> &lt;h1>&lt;/h1>  </td>
    <td> Heading tag, used to segregate the different sections <br> or sub-sections of an article. </td>
  </tr>
  <tr>
    <td> &lt;p>&lt;/p>  </td>
    <td> Used to denote a paragraph. </td>
  </tr>
  <tr>
    <td> &lt;br> </td>
    <td> Used to break the line. </td>
  </tr>
  <tr>
    <td> &lt;hr/> </td>
    <td> Used to display a horizontal line in the document. </td>
  </tr>
  <tr>
    <td> &lt;blockquote>&lt;/blockquote> </td>
    <td> For creating quotes on the page. </td>
  </tr>
  <tr>
    <td> &lt;!-- --> </td>
    <td> For comments. </td>
  </tr>
  <tr>
    <td> &lt;main>&lt;/main><br>&lt;header>&lt;/header><br>&lt;footer>&lt;/footer><br>&lt;nav>&lt;/nav><br>&lt;video>&lt;/video><br>&lt;article>&lt;/article><br>&lt;section>&lt;/section> </td>
    <td> Some HTML 5 elements that give a descriptive <br> structure to HTML and help with SEO. </td>
  </tr>


<br>

|    Tags for adding images and links   | Usage |
| ---       |    ---   |
|`<img alt="relaxing cat" src="https://www.freecatphotoapp.com/your-image.jpg">`| All img elements must have an alt attribute. The text inside an alt attribute <br> is used for screen readers to improve accessibility and is displayed if hte image fails to load.|
|`<a href="https://www.freecodecamplorg">this links to freecodecamp.org</a>` <br><br> `<a href="https://www.freecodecamp.org" target="_blank"> ...</a>` | Anchor elements are used to link to content outside of the webpage and has an href attribute. <br><br> The "_blank" target attribute tells the browser to open the link in a new tab.|
|`<a href="#contacts-header">Contacts</a>`<br>...<br>`<h2 id="contacts-header">Contacts</h2>`|You can also use the `<a>` tag to link to an internal section of the page through id attributes.|
|`<a href="#"><img src="https://www.bit.ly/fcc-running-cats"` <br> `alt="Three kittens running towards the camera."></a>` | You can turn an image into a link by nesting it in an `<a>` tag. A "#" in the href makes it a dead link.|

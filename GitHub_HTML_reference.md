---
title: "Using HTML with GitHub"
author: "Will Gammerdinger"
date: "October 24th, 2022"
---

Contributors: Will Gammerdinger

# HTML Basics

GitHub's Markdown format supports a limited amount of HTML formatting. The goal of this reference is to provide users of GitHub Markdown with a reference that they can use when using HTML within GitHub's Markdown.

The basic syntax of HTML will look like:

<***tag***>Text you want that tag applied<***/tag***>.

You can think of the first `<>` as "opening the tag" and `</>` as "closing the tag".

## General formatting

The first few subsections will discuss formatting that can easily be done in GitHub Markdown. However, ***if you are working within a larger HTML code chunk it is best to use HTML formatting for all parts of that HTML code chunk***, thus we need to discuss these essential formatting tools in HTML.

### Bold `<b>`

You could be accustomed to using `**`in order to initiate **bold** in GitHub Markdown. However, you can also do this in HTML by using `<b>` before the text you would like to be bold and `</b>` following the text you would like to be bold. The syntax would look like this:

```
<b>Text that you want to be bold</b>
```

Which appears as:

<b>Text that you want to be bold</b>

### Italics `<i>`

In order to do italics in HTML, you need to use `<i>` to initiate the italics and `</i>` to close the italics. The syntax would look like:

```
<i>Text that you want to be italicized</i>
```

Which appears as:

<i>Text that you want to be italicized</i>

### Underline `<ins>`

Underlining text in HTMl requires that you use `<ins>` to initiate underlining and `</ins>` to close underlining. The syntax would look like:

```
<ins>Text that you want to be underlined</ins>
```

Which appears as:

<ins>Text that you want to be underlined</ins>

### Subscript `<sub>`

To initiate subscript you need to use `<sub>` and to close subscript you need to use `</sub>`. The syntax would look like:

```
H<sub>2</sub>O
```

Which appears as:

H<sub>2</sub>O


### Subscript `<sup>`

To initiate superscript you need to use `<sup>` and to close subscript you need ot use `</sup>`. The syntax would look like:

```
F<sup>2</sup>
```

Which appears as:

F<sup>2</sup>

### Hyperlink `<a>`

To intiate a hyperlink you need to use `<a>` and to close a hyperlink you need to use `</a>`. Additionally, within the `<a>` tag you will need to place the `href=` option and then place your URL link in double quotes after it. The text you would like to appear to click on for the hyperlink will be between the `<a>` and `</a>`. The syntax would look like:

```
<a href="https://bioinformatics.sph.harvard.edu/training">HBC Training Webpage</a>
```

Which appears as:

<a href="https://bioinformatics.sph.harvard.edu/training">HBC Training Webpage</a>

### Blockquote `<blockquote>`

TO initiate a blockquote you need to use `<blockquote>` and to close a blockquote you need to use `<blockquote>`. The syntax would look like:

```
<blockquote>
Sometimes we need to blockquote text. Blockquoting text can have several purposes, perhaps we are adding a note about a command or we are quoting our favorite celebrity, Olivia Colman.
</blockquote>
```

Which appears as:

<blockquote>
Sometimes we need to blockquote text. Blockquoting text can have several purposes, perhaps we are adding a note about a command or we are quoting our favorite celebrity, Olivia Colman.
</blockquote>

### Keyboard Keys `<kbd>`

In order to insert a keyboard looking key, we need to intiate it with `<kbd>` and close it with `</kbd>`.The syntax would look like:

```
<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Delete</kbd>
```

Which appears as:

<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Delete</kbd>

## Combining formatting

Formatting in HTML is oftentimes quite flexible and you can nest one formatting tag within another. For example if you wanted your text to be bold and underlined you could use:

```
<b><ins>Text that you want to be bold and underlined</ins></b>
```

Which appears as:

<b><ins>Text that you want to be bold and underlined</ins></b>

## Code

You may be interested in displaying code in HTML. Similarly, to how GitHub Markdown has <code>`</code> for in-line code and <code>```</code> for code blocks, HTML has <code>&lt;code&gt;</code> for in-line code and <code>&lt;pre&gt;</code> for code blocks.

### In-line <code>&lt;code&gt;</code> 

You can initiate in-line code with <code>&lt;code&gt;</code> and close in-line code with <code>&lt;/code&gt;</code>. The syntax would look like:

```
Change directories to your favorite pictures directory by using: <code>cd /my/favorite/pictures/</code>
```

Which appears as:

Change directories to your favorite pictures directory by using: <code>cd /my/favorite/pictures/</code>

### Code Blocks <code>&lt;pre&gt;</code>

To initial a code block in HTML, you need to use <code>&lt;pre&gt;</code> and <code>&lt;/pre&gt;</code> terminates a code block. The syntax would look like:

```
To see the contents of your favorite pictures directory:
<pre>cd /my/favorite/pictures/
ls</pre>
```

Which appears as:

To see the contents of your favorite pictures directory:
<pre>cd /my/favorite/pictures/
ls</pre>

## Special Characters

HTML is has some special characters that it is picky about. The table below displays the special characters and what you should use in their place in HTML.

| Character | HTML |
|----|----|
| < | `&lt;` |
| > | `&gt;` |
| ' | `&#39;` |
| " | `&quot;` |
| & | `&amp;` |

Their syntax would look like:

```
As Lisa recounted the story, &quot;Marge said &#39;Homer, don't you know that 3 &lt; 4 &amp; also that 3 &gt; 1?&#39;&quot;
```

Which appears as:

As Lisa recounted the story, &quot;Marge said &#39;Homer, don't you know that 3 &lt; 4 &amp; also that 3 &gt; 1?&#39;&quot;

## Breaks `<br>`

To add breaks/new lines use `<br>`. The syntax would look like:

```
Text 1<br>
Text 2<br><br>
Text 3
```

Which appears as:

Text 1<br>
Text 2<br><br>
Text 3

## Thematic Breaks `<hr />`

In order to add thematic, which are light lines that go across the page to break up sections, we need to use <hr />. The syntax would look like:

```
Section 1
<hr />
Section 2
```

Which appears as:

Section 1
<hr />
Section 2

## Headers

To add headers use `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>` and `<h6>`. The syntax would look like:

```
<h1>Header 1</h1>
<h2>Header 2</h2>
<h3>Header 3</h3>
<h4>Header 4</h4>
<h5>Header 5</h5>
<h6>Header 6</h6>
```

Which appears as:

<h1>Header 1</h1>
<h2>Header 2</h2>
<h3>Header 3</h3>
<h4>Header 4</h4>
<h5>Header 5</h5>
<h6>Header 6</h6>

**NOTE: It does not appear that you can go further than `<h6>`.**

## Lists

You could be interested in making bulleted lists without numbers (Unordered Lists) using `<ul>` or list with numbers (Ordered Lists) `<ol>`.

### Unordered Lists `<ul>`

To make a bulleted list without numbers (Unordered List) You will need to initiate the unordered list with `<ul>` and close the unordered list with `</ul>`. Each bullet in the unordered list is going to need to start with a line item tag `<li>` and then close with `<li>`. The syntax would look like:

```
Items I need from the grocery store:
<ul><li>Milk</li>
<li>Eggs</li>
<li>Cereal</li></ul>
```

Which appears as:

Items I need from the grocery store:
<ul><li>Milk</li>
<li>Eggs</li>
<li>Cereal</li></ul>

### Ordered Lists `<ol>`

Ordered lists function similarly to unordered lists except you initiate ordered lists with `<ol>` and close them with `</ol>`. Like unordered lists they still need each list item to be initiated with `<li>` and closed with `</li>`. The syntax would look like:

```
The definitive ranking of best colors is:
<ol><li>Red</li>
<li>Green</li>
<li>Blue</li></ol>
```

Which appears as:

The definitive ranking of best colors is:
<ol><li>Red</li>
<li>Green</li>
<li>Blue</li></ol>

### Nesting Lists
  
Sometimes you might want to put a sub-bullets to a bulleted item. This follows all of the same syntactical rules we have discussed and your new list needs to be intiated and closed prior to the larger list being closed. The syntax for would like:
  
```
My unordered list:
<ul><li>List Item 1</li>
<li>List Item 2</li>
<ul><li>Sub-list Item 1</li>
<li>Sub-list Item 2</li>
<li>Sub-list Item 3</li></ul>
<li>List Item 3</li></ul>
```

Which appears as:

My unordered list:
<ul><li>List Item 1</li>
<li>List Item 2</li>
<ul><li>Sub-list Item 1</li>
<li>Sub-list Item 2</li>
<li>Sub-list Item 3</li></ul>
<li>List Item 3</li></ul>

## Tables

Tables are a useful way of organizing data. You will need to initiate a table with `<table>` and close a table with `</table>`. Each row will need to be initiated with `<tr>` and closed with `</tr>`. If the elements of the table are headers, then they can be initiated with `<th>` and closed with `</th>`. While elements of data in a table that aren't headers are initiated with `<td>` and closed with `</td>`. Elements that are table headers get slightly different formatting than normal table data elements. The syntax would look like this:

```
My Table:
<table>
  <tr>
    <th>Header 1</th>
    <th>Header 2</th>
    <th>Header 3</th>
  </tr>
  <tr>
    <td>Data 1 for Header 1</td>
    <td>Data 1 for header 2</td>
    <td>Data 1 for Header 3</td>
  </tr>
  <tr>
    <td>Data 2 for Header 1</td>
    <td>Data 2 for header 2</td>
    <td>Data 2 for Header 3</td>
  </tr>
</table>
```

Which appears as:

My Table:
<table>
  <tr>
    <th>Header 1</th>
    <th>Header 2</th>
    <th>Header 3</th>
  </tr>
  <tr>
    <td>Data 1 for Header 1</td>
    <td>Data 1 for header 2</td>
    <td>Data 1 for Header 3</td>
  </tr>
  <tr>
    <td>Data 2 for Header 1</td>
    <td>Data 2 for header 2</td>
    <td>Data 2 for Header 3</td>
  </tr>
</table>

## Inserting Images `<p>`

You might be interested in inserting an image. To do this, initiate the image with `<p>` and close the image with `</p>`. However, in your `<p>` you are also going to need to specifiy your alignment for the image (i.e. would you like the image `left`-aligned, `center`-aligned or `right`-aligned. The default is a `left`-alignment.

Between your `<p>` and `</p>` you will need to open up `<img>` tag and and provide the indirect path from your current position to the image on GitHub to the `src` option along with the width in pixels that you would like to use to the `width` option. The syntax would look like:

```
<p align="center">
<img src="img/breakfast_Monvej.png" width="700" >
</p>
```

Which appears as:

<p align="center">
<img src="img/breakfast_Monvej.png" width="700" >
</p>

## Dropdowns Menus

One neat aspect that HTML offers that we can't do in GitHub's Markdown is use dropdown menus. These collapsible menus are great for allowing users to toggle information. All of the formatting that we've used up to this point is all able to be used within these dropdown menus. To initiate a dropdown menu use `<details>` and to end a dropdown menu use `</details>`. When using a dropdown menu, you will likely want to have text for the user to click on in order to engage this dropdown. This text is initiated with `<summary>` and closed with `</summary>`. The syntax would look like:

```
<details>
<summary>Click here to expand the dropdown menu</summary>
You couldn't see this menu before, but now you can. Click the &quot;Click here to expand the dropdown menu&quot; again to hide this.
</details>
```

Which appears as:

<details>
<summary>Click here to expand the dropdown menu</summary>
You couldn't see this menu before, but now you can. Click the &quot;Click here to expand the dropdown menu&quot; again to hide this.
</details>

***
*This lesson has been developed by members of the teaching team at the [Harvard Chan Bioinformatics Core (HBC)](http://bioinformatics.sph.harvard.edu/). These are open access materials distributed under the terms of the [Creative Commons Attribution license](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), which permits unrestricted use, distribution, and reproduction in any medium, provided the original author and source are credited.*

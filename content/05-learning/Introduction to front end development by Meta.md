---
title: Front end development by Meta
date: 2023-10-04
summary: ""
tags:
  - learning
  - "front end"
---

## How does internet work

### Web stuff: server, browser, hosting

**Web server**: a computer that runs application and provide services to another computer - the client. 

A web server's duty 
	 - website storage and administration
	 - data storage
	 - handling web requests
	 - managing email, security, etc.

The client-server model & request response model.

When we (client) visit a website by URL, the server sends a copy of its html file,
our **Web browser** renders the page.

URL: uniform resource locator.
htttp://www.example.com,
contains protocol (http), domain name and file path.

**Website vs Webpage**
	- webpage: one document displaying text, image, video, etc.
	- website: a collection of web pages linked together

**Web hosting**
	- shared hosting
		- share processing, memory and bandwidth
		- low-cost sandbox for practice environment or deploying
	- virtual private hosting
	- dedicated hosting
	- cloud hosting: physical + virtual servers

###  Internet protocols, TCP, UDP, HTTP

**IP**: internet protocols. v4 and v6.

**IP packets**: or datagrams. Consists of header and payload.
	- header: destination, source IP and other info
	- payload: data and other protocols

Protocols address potential issues:
	- packets arrived out of order
	- damaged or corrupted
	- dropped or lost

**TCP**: transmission control protocol. 
Make sure the data arrive correct and in order.

**UDP**: user datagram protocol, data intact but may be out of order

**HTTP**: hyper text transfer protocol.
It's the communication protocol for browsers.

**HTTPS**: secure version of http, data encrypted.

Other protocols:
	- DHCP, DNS
	- IMAP, SMTP, POP
	- FTP, SSH, SFTP

### Request - response model

#### Methods
- **GET**: retrieve
- **POST**: send
- **PUT**: update
- **DELETE**: remove

#### Response status codes: 100 - 599
Has a code and text message, such as 200 OK or 404 not found.

| num       | group         | Notes                                  e.g.                             |
| --------- | ------------- | ----------------------------------------------------------------------- |
| 100 - 199 | Informational | provisional, sent by server            100 continue                     |
| 200 - 299 | Successful    | successfully processed                 200 OK                           |
| 300 - 399 | Redirection   | requested resource moved to diff path  301 moved permanently; 302 found |
| 400 - 499 | Client error  | 400 bad data, 401 must login first, 403 permission, 404 not found       |
| 500 - 599 | Server error  | 500 server not responding                                               | 

### Front end, back end and full stack

**Front end**:  style, colors, buttons, menus, UI stuff.
Deal with html, CSS and Javascript.

**Back end**: where the users don't see.
	 - web server (back end) languages (such as python), setup, configuration
	 - database management
	 - architecture, APIs

**Full stack** both frond and back end.

## Front end intro

### HTML, CSS and Javascript

**HTML**: hyper text markup language.
Webpage documents.

**CSS**: cascading style sheets.

**Javascript**: interactivity, data processing, control and action. The powerhouse of websites.

### Developer tools
In browser, right click -> inspection.
F12 (win) or cmd+J (mac).

**Console**: Javascript logs and errors.

**Sources**: all contents.

**Network**: timeline of http requests and response.

Performance, memory.

**Elements**: html elements, like lego blocks that assembles to the whole page.

You can play around and change things temporarily.

**IDE**:
Refactoring: like update var or function names. 

### Framework, library and API

Frameworks are more about structures, libraries more about reusable codes.

Frameworks call your app, your app calls library, frameworks contain library.

It's harder to replace frameworks than libraries.
It's kind of like changing landlord/ houses vs upgrading furniture inside your room

**API**: application programming interface. 
a service, application or interface offering advanced functionality with simple syntax.
	- Browser/ Web API: built into browser itself.
	- DOM API: turns html document into a tree of nodes represented by JS objects.
	- FetchAPI: fetch data
	- RESTful or REST API: representational state transfer (most common) 
		- A set of *principles* that build highly efficient APIs.  Like sending and receiving data to and from a centralized database.
	- Sensor-based API: physical sensors, like the raimbow hue bulbs

## HTML: hyper text markup language

### Head and body elements

*Head*: meta data, not rendered on the page

*Body*: content of the page

### HTML Tags

Most tags contain a pair of opening and closing tags: `<h1></h1>`, although some don't have a closing tag: `<br>`.

Some common tags: h1 (header), p (paragraph), ul (unordered list), ol (ordered list), li (list item), div (division), style, a (anchor), img (image), table.

```html
<!DOCTYPE html>
<html>
<head>
	<title>Some tag examples</title>
</head>
	<!-- Comments -->
<body>
	<!-- h1 - h7 (headers) -->
	<h1>Header 1</h1>

	<!-- p (paragraph) and br (line break) -->
	<p>
		A paragraph. <br>
		with a line break
	</p>

	<!-- ul (unordered list), li (list item) -->
	<ul>
		<li>Unordered list item 1</li>
		<li>Unordered list item 2</li>
		<li>Unordered list item 3</li>
	</ul>
	<!-- ol (ordered list), li (list item) -->
	<ol>
		<li>Ordered list item 1</li>
		<li>Ordered list item 2</li>
		<li>Ordered list item 3</li>
	</ol>

	<style>
	   div { border: 1px solid black; padding: 2px; }
	</style>	
	<!-- div (division) -->
	<div>
		<p>
			Division doesn't do anything until we style it.
		</p>
	</div>

	<!-- a (anchor): references and links -->
	<a href="https://gr-grey.github.io/" >Link to this blog.</a>

	<!-- img image -->
	<img src="https://static.wikia.nocookie.net/inconsistently-admirable/images/a/ab/Ghost.png/revision/latest/scale-to-width-down/1200?cb=20220331020028" width="30%" alt="Hollow Knight.png">

	<!-- table -->
	<table>
		<!-- tr (table row) -->
		<tr>
			<!-- th (table header) -->
			<th>col 1</th>
			<th>col 2</th>
		</tr>
		<tr>
			<!-- td (table data) -->
			<td>data 1.1</td>
			<td>data 1.2</td>
		</tr>
		<tr>
			<td>data 2.1</td>
			<td>data 2.2</td>
		</tr>
	</table>
</body>
</html>
```

How the code block html looks like:

<h1>Header 1</h1>
<p>
	A paragraph. <br>
	with a line break
</p>
<ul>
	<li>Unordered list item 1</li>
	<li>Unordered list item 2</li>
	<li>Unordered list item 3</li>
</ul>
<!-- ol (ordered list), li (list item) -->
<ol>
	<li>Ordered list item 1</li>
	<li>Ordered list item 2</li>
	<li>Ordered list item 3</li>
</ol>
<style>
   div { border: 1px solid black; padding: 2px; }
</style>	
<div>
	<p>
		Division doesn't do anything until we style it.
	</p>
</div>
<a href="https://gr-grey.github.io/" >Link to this blog.</a>
<img src="https://static.wikia.nocookie.net/inconsistently-admirable/images/a/ab/Ghost.png/revision/latest/scale-to-width-down/1200?cb=20220331020028" width="200" alt="Hollow Knight.png">
<table>
	<tr>
		<th>col 1</th>
		<th>col 2</th>
	</tr>
	<tr>
		<td>data 1.1</td>
		<td>data 1.2</td>
	</tr>
	<tr>
		<td>data 2.1</td>
		<td>data 2.2</td>
	</tr>
</table>

### Forms: transfer data to & from server

Input tags: text, password, checkbox, radio, text area, email, numbers, select, submit button

```html
<!-- forms -->
<form action="/registration" method="POST">
	<!-- text field and password -->
	<label for="username">Username: (text box)</label><br>
	<input type="text" name="username"><br>
	<label for="password">Password: (not showing text)</label><br>
	<input type="password">
	
	<!-- checkbox -->
	<input type="checkbox" name="dog" value="Dog">
	<label for="dog">dog person</label><br>
	<input type="checkbox" name="cat" value="Cat">
	<label for="cat">cat person</label><br>
	
	<!-- radio button: only select 1 -->
	<input type="radio" name="rad1" value="Rad1">
	<label for="rad1">Radio 1</label><br>
	<input type="radio" name="rad2" value="Rad2">
	<label for="rad2">Not Radio 1</label><br>
	
	<!-- text area: paragraph input -->
	<label for="multline">Type a paragraph:</label><br>
	<textarea name="multiline" name="para1" rows="5"></textarea><br>
	
	<!-- drop-down list -->
	<label for="dropDownlist">A drop down list:</label><br>
	<select name="dropDownList">
		<option value="chocolate">Chocolate</option>
		<option value="ice_cream">Ice Cream</option>
	</select>
</form>
```

<form action="/registration" method="POST">
	<label for="username">Username: (text box)</label><br>
	<input type="text" name="username"><br>
	<label for="password">Password: (not showing typed content)</label><br>
	<input type="password"><br>
	<input type="checkbox" name="dog" value="Dog">
	<label for="dog">dog person</label><br>
	<input type="checkbox" name="cat" value="Cat">
	<label for="cat">cat person</label><br>
	<input type="radio" name="rad1" value="Rad1">
	<label for="rad1">Radio 1</label><br>
	<input type="radio" name="rad2" value="Rad2">
	<label for="rad2">Not Radio 1</label><br>
	<label for="multline">Type a paragraph:</label><br>
	<textarea name="multiline" name="para1" rows="5"></textarea><br>
	<label for="dropDownlist">A drop down list:</label><br>
	<select name="dropDownList">
		<option value="chocolate">Chocolate</option>
		<option value="ice_cream">Ice Cream</option>
	</select>
</form>

### DOM: document object model

A tree, structure or model of the *objects* in a html file.

All elements in a HTML file are treated as *objects*.
We can use JavaScript to access and modify DOM to make the webpages dynamic.

A DOM can be quite complex for highly interactive pages, 
for example a div obj containing a p obj containing text obj.

### Web accessibility

W. A. I: Web accessibility initiative.

ARIA: accessible rich internet application

Bad practice to throw raw text around without wrapping them with paragraph p tags

## CSS: Cascading style sheets

Add `<link rel="stylesheet" href="yourCssFile.css">` in your html file head to apply the styles.


### Selector

Element selectors, ID selectors, class selectors, element with class selectors, descendant selectors, child selectors, pseudo class selectors.

```css
/* Comment */

/* Element Selectors (e.g. paragraph) */
p { color: blue; }

/* ID selectors 
html: <span id="latest">New!</span> */

#latest { background-color: purple; }

/* Class selectors
html: 
<a class="navigation">Go Back</a>
<p class="navigation">Go Forward</p>*/

.navigation { margin: 2px; }

/*Element with class selector
html: <p class="introduction"></p>*/

p.introduction {margin: 2px;}

/*Descendant selectors
HTML
<div id="blog">
  <h1>Latest News</h1>
  <div>
    <h1>Today's Weather</h1>
    <p>The weather will be sunny</p>
  </div>
  <p>Subscribe for more news</p>
</div>
<div>
  <h1>Archives</h1>
</div>
*/

#blog h1 {color: blue;}

/*Child selectors: direct children only, 
no grand children, only selects "Latest News"
*/

#blog > h1 {color: blue;}

/*:hover Pseudo-Class*/

a:hover { color: orange;}
```

### Color, Text font, size, transformation

#### Color
5 ways to reference a color: RGB, RGBA, HSL, hex, predefined color names.

``` css
p {color: rgb(255, 0, 0);}

/*rgba, last channel alpha, opacity*/
p {color: rgba(255, 0, 0, 0.8);}

p {color: hsl(0, 100%, 50%);}

p {color: #FF0000; }

p {color: blue;}

```

#### Text styles

```css
p { 
  /* mutilple families will be applied on the fall back order*/
  font-family: "Courier New", monospace;
  font-size: 12px;
  text-transform: uppercase;
  text-decoration: underline red solid 5px;
  /* same as setting them seperately*/
  text-decoration-line: underline;
  text-decoration-color: red;
  text-decoration-style: solid;
  text-decoration-thickness: 5px;
}
```

### BOX model

Allocate a rectangle or box to each element.

Four parts of the box, from inside to outside: content, padding, border and margin

### Document flow

browser calculate the position of html element

### Block, Inline and alignment

Blocks span the full horizontal width of its parent element and vertical height of its content, it'll stack on top of each others like boxes.

Inlines will take the width of itself, they don't appear on a new line.

`<span>` is inline

`<div>` is block

Can be changed by specify `display: inline/ block;`

[Alignment basics](https://www.coursera.org/learn/introduction-to-front-end-development/supplement/L9FYk/alignment-basics).

#### Text alignment
`p {text-align: center;}`.
Options: `left`, `right`, `center`, `justify`.

Justify spreads text out so every line has the same width.

#### HTML Element alignment 

**Align to center**

```html
<div class="parent">
  <div class="child">
  </div>
</div>
```

```css
.parent {
  border: 4px solid red;
}

.child {
  width: 50%;
  padding: 20px;
  border: 4px solid green;
/*Align child to the middle of parent*/
  margin: auto;
}
```

![result](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ElKjOOdnT2GSozjnZy9hJw_0670f63ae6e548a28dfa041b7983bfe1_css_center_div.png?expiry=1696982400000&hmac=JwO9ujkBhVpJoYTQjsQyhvH7mJE4ewLrLaSuMBWWVAU)

Aligning image

```html
<div class="parent">
  <img src="photo.png" class="child">
</div>
```

```css
.child {
  display: block;
  width: 50%;
  margin: auto;
  /*mor precisely, if want to set top/bottom margin too*/
  margin-left: auto;
  margin-right: auto;
}
```

**Align left or right**

Use the `float` property or `position` property.

`float` sets an element's position relative to the text content within a parent element. Text will wrap around the element.

Example:

```html
<div class="parent">
  <img src="photo.png" class="child"> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur eu odio eget leo auctor porta sit amet sit amet justo. Donec fermentum quam in diam volutpat, at lacinia diam placerat. Aenean quis feugiat sem. Suspendisse a dui massa. Phasellus scelerisque, mi vestibulum iaculis tristique, orci tellus gravida nisi, in pellentesque elit massa ut lorem. Sed elementum ornare nunc vel cursus. Duis sed enim in nulla efficitur convallis sed eget dolor. Curabitur scelerisque eros erat, in vulputate dolor consequat vel. Praesent ac sapien condimentum, ultricies libero at, auctor orci. Curabitur ut augue ac massa convallis faucibus sed in magna. Phasellus scelerisque auctor est a auctor. Nam laoreet sem sapien, porta imperdiet urna laoreet eu. Morbi dolor turpis, congue id bibendum eget, viverra et risus. Quisque vitae erat id tortor ullamcorper maximus.
</div>
```

```css
.child {
  float: right;
}
```

![Result](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/JBGR11KmTT-RkddSpn0_WA_a961d58ec8334d8387cc2df53c9b15e1_css_float_right.png?expiry=1696982400000&hmac=vJrogRUDInrlATEbR_GpsZHVJPzaiMIA2XDSpk2jBEg)
 
## Additional resources

### How internet works

**What is a Web Server? (NGINX)**
[https://www.nginx.com/resources/glossary/web-server/](https://www.nginx.com/resources/glossary/web-server/)

**What is a Web Browser? (Mozilla)**
[https://www.mozilla.org/en-US/firefox/browsers/what-is-a-browser/](https://www.mozilla.org/en-US/firefox/browsers/what-is-a-browser/)

**Who invented the Internet? And why? (Kurzgesagt)**
[https://youtu.be/21eFwbb48sE](https://youtu.be/21eFwbb48sE)

**What is Cloud Computing? (Amazon)**
[https://youtu.be/mxT233EdY5c](https://youtu.be/mxT233EdY5c)

**Browser Engines (Wikipedia)**
[https://en.wikipedia.org/wiki/Browser_engine](https://en.wikipedia.org/wiki/Browser_engine)

### HTML

**HTML Elements Reference (Mozilla)**
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

**The Form Element (Mozilla)**
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form)

**What is the Document Object Model? (W3C)**
[https://www.w3.org/TR/WD-DOM/introduction.html](https://www.w3.org/TR/WD-DOM/introduction.html)

**ARIA in HTML (W3C via Github)**
[https://w3c.github.io/html-aria/](https://w3c.github.io/html-aria/)

**ARIA Authoring Practices (W3C)**
[https://www.w3.org/TR/wai-aria-practices-1.2/](https://www.w3.org/TR/wai-aria-practices-1.2/)

### CSS Bacis

**CSS Reference (Mozilla)**

[https://developer.mozilla.org/en-US/docs/Web/CSS/Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)

**HTML and CSS: Design and build websites by Jon Duckett**

[https://www.amazon.com/HTML-CSS-Design-Build-Websites/dp/1118008189/](https://www.amazon.com/HTML-CSS-Design-Build-Websites/dp/1118008189/)

**CSS Definitive Guide by Eric Meyer**

[https://www.amazon.com/CSS-Definitive-Guide-Visual-Presentation/dp/1449393195/](https://www.amazon.com/CSS-Definitive-Guide-Visual-Presentation/dp/1449393195/)

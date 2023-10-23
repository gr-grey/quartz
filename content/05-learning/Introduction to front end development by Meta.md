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

## Front end concepts and tools

### HTML, CSS and Javascript

**HTML**: hyper text markup language.
Webpage documents.

**CSS**: cascading style sheets.

**Javascript**: interactivity, data processing, control and action. The powerhouse of websites.

### Developer tools
In browser, right click -> inspection.
F12 (win) or cmd+J (mac).

Developer tools has a mobile simulator.

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
<a href="https://gr-grey.github.io/" >Link to this blog.</a>
<img src="https://www.xboxtavern.com/wp-content/uploads/2018/09/HollowKnightRevRBBBB.jpg" width="30%" alt="Hollow Knight.png">

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
<img src="https://www.xboxtavern.com/wp-content/uploads/2018/09/HollowKnightRevRBBBB.jpg" width="30%" alt="Hollow Knight.png">
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

![result](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ElKjOOdnT2GSozjnZy9hJw_0670f63ae6e548a28dfa041b7983bfe1_css_center_div.png?expiry=1698192000000&hmac=X6fLD8pmDwUmkDytWsigxM7YM2HUAbLri1mccGTj7X4)

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

![Result](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/JBGR11KmTT-RkddSpn0_WA_a961d58ec8334d8387cc2df53c9b15e1_css_float_right.png?expiry=1698192000000&hmac=l7yiKjCpZTPQEccft358-dqNPIhjBCpRGYISnRWnhZU)

## Bootstrap framework and responsive design

 Libraries, dependencies and bundlers.
 - NPM: node package manager
 - Javascript bundlers: Gulp and webpack

### Responsive grids: flexible, fluid, large & small screens

Responsive design auto adjust the width depending on the size of the screen.

Responsive grids come with the following features.

1. Flexible grids
	 - are made up of columns, gutters and margins |< margin| column | gutter | column | margin >|
	 - set by percentage instead of absolute sizes
2. Fluid images
	 - e.g. max-width: 90%
	 - either shrinks to meet max width or keep the same size (won't expand bigger)
3. Media queries
	 - display size, orientation, aspect ratio

*Breakpoint*: 

 -  the "breaking point" between larger and smaller screens, e.g. below 768px should be one case (mobile), from 768 to 1024px should be one case (tablets), then > 1024 should be desktop.

*3 Grid types*

1. Fix grid: fixed column/ content width, flexible margins expand to fill the void.
2. Fluid/ full width grid: fluid column width, fixed gutter. Column/ content expands to fill the void.
3. Hybrid: mix of fix and fluid.

The approach to breakpoints has evolved over time. 
Initially, designers used device-specific breakpoints, but the industry has largely shifted towards content-specific breakpoints. 
This means we set breakpoints where the particular design naturally breaks or could be improved, rather than sticking rigidly to common device dimensions.

### Bootstrap framework: infixes, modifiers, layout, content, forms.

Bootstrap, a library of CSS and JavasScript code,
has been called a front-end framework, CSS framework and CSS library.

It has a lot of classes ready for use.

It's useful to build *Responsive grids*.

**Infixes and modifiers**

Infixes are thresholds for determine if a size is small, middle, large or xlarge

```html

<!--6 column for small screen (default xs) -->
<div class="col-6"></div>
<!--6 column for large screen -->
<div class="col-lg-6"></div>

<!--spans all 12 cols for small screen and split by occupying only 6 cols on large ones -->
<div class="col-12 col-lg-6"></div>

<div class="alert alert-primary"></div>
```

Modifier changes the color of the alert message.

[Using Bootstrap documentation](https://www.coursera.org/learn/introduction-to-front-end-development/supplement/AgPYj/using-bootstrap-documentation)

[Get started with Bootstrap · Bootstrap v5.3 (getbootstrap.com)](https://getbootstrap.com/docs/5.3/getting-started/introduction/)

#### Layout

Grid system of Bootstrap. 
More advanced usage such as offsets, column alignment, auto-layout and variable width columns.

#### Content

Responsive images and tables.

#### Forms styling

HTML form elements and corresponding Bootstrap CSS class 

| Form Element          | CSS class        |
| --------------------- | ---------------- |
| input                 | form-control     |
| input type="checkbox" | form-check-input |
| input type="radio"    | form-check-input |
| input type="range"    | form-range       |
| select                | form-select      | 

Using these CSS classes will style the elements appropriately for different input types, sizings and states. 
[Forms documentation page](https://getbootstrap.com/docs/5.0/forms/overview/).

*Switches*

If you've used an app on your mobile device, you're probably familiar with the switch input type.

![Bootstrap Doc Switches](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/t-RILIyKSwekSCyMipsHug_9b79ddf623c54c6f8719964fc25e20e1_bootstrap_docs_switches.png?expiry=1698192000000&hmac=aGSFW2EauOqIv9PFHrGAKiSiEl8e7dI-KmjiVe0pIRE)

Bootstrap includes CSS rules to style checkbox input elements as switches.

```html
<div class="form-check form-switch">
  <input class="form-check-input" type="checkbox">
</div>
```

[Switches section of the documentation](https://getbootstrap.com/docs/5.0/forms/checks-radios/#switches).

##### Input Groups

providing additional content to the input field. 
For example, request the user to input a US dollar amount, use an input group to show the dollar symbol and cents amount.

![Bootstrap Input Groups](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/mr7x2CKwQ86-8dgisGPOQQ_b4407177d0b74adc8b4affb9fc8efde1_bootstrap_input_group.png?expiry=1696204800000&hmac=_wXWVZTFQvpBD6HEKZ1HzCBNS-fr02rRFx6tXZjaktg)




```html
<div class="input-group">
  <span class="input-group-text">$</span>
  <input type="text" class="form-control">
  <span class="input-group-text">.00</span>
</div>
```


##### Floating Labels

provide form information to the user as part of the input itself. These are different from regular form placeholders. The information stays visible if the user is interacting with the element or if the element has content.

![Bootstrap floating label](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/d91CBY4JQoOdQgWOCaKD5Q_cee428e3084f4f51bb27b71a353924e1_bootstrap_docs_floating_label1.png?expiry=1696204800000&hmac=7-h2LjdtZSl--byzqfAJBfwQA8cMBnoyZZGklfaZ5_0)

![Bootstrap floating label](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/-5va2gC4R56b2toAuPeehQ_159ac1bc9ba744778bccd91d679fa2e1_bootstrap_docs_floating_label2.png?expiry=1696204800000&hmac=ZuomwQ0uvkuFBQPxRcFQ2fve9pTNdXSwyW767aQbs1I)

```html
<div class="form-floating">
  <input type="email" class="form-control" id="addressInput" placeholder="Address">
  <label for="addressInput">Address</label>
</div>
```

 [Floating Labels documentation page](https://getbootstrap.com/docs/5.0/forms/floating-labels/)
 
#### Components

Some components require Javascript to work, while others only require CSS classes applied to HTML elements. 

![The components section of the Bootstrap documentation](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/SF1dLntLRAqdXS57S1QKcg_27e2d870013f468ab187f7a708113fe1_bootstrap_docs_components.png?expiry=1696204800000&hmac=S-WLe1MBSU_aiABRc0JtcERxfVDeYT62FfvuBekvzhs)


### Other CSS frameworks and libraries


#### Foundation

[Foundation](https://get.foundation/)

similar to Bootstrap. 
used by companies such as Pixar, Polar and Sonos. 

One feature: can be used to style content for sending via email.

#### Pure.css

[Pure.css](https://purecss.io/)

While it doesn't have as many features as Bootstrap, it is designed to be minimal in file size. 
Smaller file sizes improve loading times for web pages as there is less data to transfer from the web server. 

#### Tailwind CSS

[Tailwind CSS](https://tailwindcss.com/)
Rapidly build modern websites without ever leaving your HTML.

uses a utility-based approach for its CSS rules. 
the framework provides many CSS classes with a single purpose. 

For example, the CSS class pt-6 sets the padding-top CSS property to 6 pixels. 
you can be precise in styling without writing CSS. 

The advantage is more flexible for customizing webpage's design.
the disadvantage is if multiple developers, it could lead to inconsistent design

#### UIKit

[UIKit](https://getuikit.com/)

a lightweight and modular CSS framework featuring a small set of responsive components. 
A simple design allows developers to easily customize the style rules and visuals.


#### MVP.css

[MVP.css](https://andybrewer.github.io/mvp/)
A minimalist stylesheet for HTML elements.

comes from the technical term Minimal Viable Product, a product with sufficient features to demo to customers or other business stakeholders.

a small CSS library that automatically styles HTML elements without needing to apply CSS classes to them. 
allow a developer to quickly prototype a user interface without worrying about the final design, while still being visually appealing. 


 
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

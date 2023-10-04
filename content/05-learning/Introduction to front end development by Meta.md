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
 
## Additional resources

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
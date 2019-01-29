### webpage life cycle
---
#### Request
when a link is clicked, then a webpage(text file) is requested by the web browser using http. 

#### Response
In web server, the response is made, the browser receive files, like html, css, images, javascripts, then downloaded by browser.

#### Build
* Build DOM (Document Object Map)

* Build CSSOM (CSS Object Map)
* Build Render Tree
Take DOM and the CSSOM and combines them to create a full map 

#### Render
Dispaly in browser
* layout(reflow)
the browser determines how big a screen is and how that will affect the way the page is displayed
* paint
the browser will convert each node in the render tree to actual pixels on the screen


#### reference
[1] [What are the steps of a webpage being displayed?](https://varvy.com/pagespeed/display.html)



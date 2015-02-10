Unzip the entire file to a local directory and run index.html


Optimizations:

1) Compressed the pizzeria photo (views\images\pizzeria.jpg) using the website below to decrease the size from 2.25 mb to 59kb
http://jpeg-optimizer.com/

2) Saved  a smaller version of (views\images\pizzeria.jpg) as pizzeria_small.jpg to be used with index.html

3) Compressed the file (\img\profilepic.jpg) using the website below
http://jpeg-optimizer.com/

4)Located the css for the webfont in the resources tab of Google-chrome and inlined it directly into index.hrml

5)In-lined the contents of (\css\style.css) directly into index.html

6)Added the "async" keyword to the script reference for google analytics.js
<script async src="http://www.google-analytics.com/analytics.js"></script>

7)Added a media attribute to the print.css stylesheet so it only is loaded when the document is printed
<link href="css/print.css" rel="stylesheet" media=print >

8)Added a viewport setting to pizza.html
<meta name=viewport content="width=device-width, initial-scale=1">

9)Decreased the number of pizzas in the background to 32 (4 rows). Most of the 200 that were 
originally added we never even visible on the screen.

10)Resized the background pizza images using the websites below
used http://images.my-addr.com/resize_png_online_tool-free_png_resizer_for_web.php
and https://tinypng.com/ 

11)Used  window.requestAnimationFrame  in the updatePositions() function in (\views\js\main.js) 
to draw the changes when the browser was ready for the next frame.

12)Placed all the "mover" containers in a global variable named "movingPizzas" so that the script would only have to 
query the DOM for them once (as opposed to every time the scroll event fired)
movingPizzas = document.querySelectorAll('.mover');

13)Placed all the random pizzas in the global array so that the script would only have to get them from the 
DOM once.
var randomPizzaContainers = document.querySelectorAll(".randomPizzaContainer");
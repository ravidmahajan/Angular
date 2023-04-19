# Angular
angular prep

1. is Angular MVC or MVVM?

Angular is a Model-View-Controller (MVC) framework. The core architecture of Angular is based on the MVC pattern, where the Model represents the data and business logic, the View represents the UI elements, and the Controller acts as an intermediary between the Model and View, handling user input and updating the Model and View accordingly.

However, Angular also incorporates some elements of the Model-View-ViewModel (MVVM) pattern, particularly in its use of templates and data binding. In MVVM, the ViewModel acts as an intermediary between the View and Model, and facilitates data binding between the two.

So, while Angular is primarily an MVC framework, it does incorporate some MVVM principles.
-----------------------------------------------------------------------------------------------------
=====================================================================================================
2. AOT and JIT

AOT and JIT are two different modes of compilation in Angular, with different benefits and trade-offs.

AOT (Ahead-of-Time) compilation generates compiled code during the build process, before the code is served to the browser. 
JIT (Just-in-Time) compilation, on the other hand, compiles the code in the browser at runtime.

Here are the step-by-step compilation processes for AOT and JIT in Angular:

AOT Compilation:

The developer writes the code in TypeScript and creates templates using Angular's template syntax.
The Angular Compiler compiles the templates and generates JavaScript code.
The TypeScript compiler compiles the TypeScript code into JavaScript code.
The AOT compiler generates compiled code during the build process, including the templates, components, and metadata, which is then bundled and sent to the browser.
When the browser receives the code, it does not need to compile the code again, which makes the application load faster and improves performance.

JIT Compilation:

The developer writes the code in TypeScript and creates templates using Angular's template syntax.
The Angular Compiler compiles the templates and generates JavaScript code.
The TypeScript compiler compiles the TypeScript code into JavaScript code.
When the application is served to the browser, the JIT compiler runs in the browser and compiles the code at runtime.
The compiled code is executed by the browser, and the application runs as expected.
The main benefit of AOT compilation is improved performance, as the compiled code is already optimized before it reaches the browser. This makes the application load faster and perform better. On the other hand, JIT compilation allows for faster development and easier debugging, as the code can be recompiled on the fly as needed.

In summary, AOT and JIT are two different modes of compilation in Angular, with different benefits and trade-offs. AOT generates compiled code during the build process, while JIT compiles the code in the browser at runtime. Both modes of compilation have their own advantages and disadvantages, and the choice depends on the specific needs of the application.
==============================

3. HTMl 5 features

Following are the new features in HTML5 : 
There are new semantic elements - header , footer , section ,nav , article , aside
New graphic elements like svg , canvas
New apis - localstorage , session storage , geolocation , drag and drop , server sent
events , web workers
Audio and video tags
New form controls like datalist , output
New form input types like color , range ,number , url , email , search , tel, datetime ,time , month ,week etc.
New input attributes like placeholder , multiple , autocomplete , autofocus , required,min and max , width and height ,list , formaction ,formnovalidate , formtarget ,formmethod, formenctype etc.
New form attributes autocomplete, novalidate


==============================================
4.how localStorage and sessionStorage used in javascript. Give example
localStorage and sessionStorage are two mechanisms provided by the browser's Web Storage API that allow you to store key-value pairs in the client-side storage.

localStorage is used to store data that persists even after the browser is closed or the user logs out of your web application. This means that data stored in localStorage will remain available until it is explicitly removed by the user or cleared by the web application.

sessionStorage, on the other hand, is used to store data that only persists for the duration of the user's session on a particular website. This means that data stored in sessionStorage will be available as long as the user remains on your web application or until the browser is closed.

Here is an example of how to use localStorage and sessionStorage in JavaScript:

javascript
Copy code
// Store data in localStorage
localStorage.setItem('username', 'JohnDoe');
localStorage.setItem('email', 'johndoe@example.com');

// Retrieve data from localStorage
const username = localStorage.getItem('username');
const email = localStorage.getItem('email');

// Remove data from localStorage
localStorage.removeItem('email');

// Store data in sessionStorage
sessionStorage.setItem('theme', 'dark');
sessionStorage.setItem('language', 'en');

// Retrieve data from sessionStorage
const theme = sessionStorage.getItem('theme');
const language = sessionStorage.getItem('language');

// Remove data from sessionStorage
sessionStorage.removeItem('language');
In this example, we first store two key-value pairs in localStorage using the setItem() method. We then retrieve the values using the getItem() method and store them in variables. Finally, we remove one of the key-value pairs using the removeItem() method.

We also store two key-value pairs in sessionStorage, retrieve the values, and remove one of the key-value pairs using the same methods. The key difference is that the data stored in sessionStorage will be removed when the user closes the browser or navigates away from the website, while the data stored in localStorage will persist until it is removed or cleared.
==========================================================================================
5. is localStorage data same for different protocol of same page
No, localStorage data is not shared between different protocols of the same page.

The Web Storage API is implemented on a per-origin basis. An origin consists of a combination of protocol (HTTP, HTTPS, etc.), domain, and port. If you try to access localStorage data from a different origin, you will not be able to access it due to the Same-Origin Policy.

Similarly, if you have the same page open in two tabs, one with the HTTP protocol and the other with the HTTPS protocol, they will be treated as different origins and will have separate localStorage data.

So, in short, localStorage data is not the same for different protocols of the same page. Each protocol and origin will have its own separate localStorage data.
========================================================================================================

6.What are trust tokens, interest groups, shared storage, cache storage in web browser, also webSQl and indexed DB and there storage size


Trust Tokens, Interest Groups, Shared Storage, and Cache Storage are browser technologies that provide various benefits to web developers and users. WebSQL and IndexedDB are storage technologies that allow web developers to store data locally on the user's device. Here's a brief overview of each:

Trust Tokens: Trust Tokens are an experimental feature that allows websites to delegate trust to other websites, which can then be used to combat fraud and abuse. Trust Tokens are based on cryptographic principles and can be used to identify trustworthy entities without the need for a centralized authority.

Interest Groups: Interest Groups are a privacy-enhancing technology that allows web browsers to group users with similar interests together without revealing their individual browsing histories. Interest Groups can be used to improve online advertising and content recommendations while protecting user privacy.

Shared Storage: Shared Storage is a new type of storage API that allows multiple tabs or windows of the same website to share data with each other. This allows for better collaboration between different parts of a website and can be used to improve performance and reduce duplicate data storage.

Cache Storage: Cache Storage is a browser storage mechanism that allows web developers to store frequently accessed resources (such as images, JavaScript files, and stylesheets) on the user's device, reducing the need for repeated downloads from the server.

WebSQL and IndexedDB: WebSQL and IndexedDB are two storage technologies that allow web developers to store data locally on the user's device. WebSQL is a SQL-based database API that has been deprecated and is no longer recommended for use. IndexedDB is a newer API that provides a more powerful, asynchronous, and flexible way of storing data locally.

As for storage size, the amount of storage available for each technology can vary depending on the browser and device being used. Generally, IndexedDB provides the most storage space, with a limit of around 50-100 MB depending on the browser. Cache Storage also has a limit, but it varies depending on the browser and can range from a few hundred MB to several GB. Trust Tokens, Interest Groups, and Shared Storage do not have a specified storage size limit.
=====================================================================================================================================================
7. canvas vs svg
Canvas and SVG (Scalable Vector Graphics) are both graphics technologies used on the web, but they have different strengths and are used for different purposes.

Canvas is a bitmap-based graphics technology, which means that it creates an image by drawing pixels directly onto a grid. The grid is created dynamically, which means that you can draw, animate, and manipulate the pixels in real time. Canvas is particularly useful for creating interactive games, animations, and other dynamic visual effects. Canvas has a lower overhead than SVG, making it faster for drawing and animating large numbers of objects. However, canvas images are not scalable without losing quality, so it may not be the best choice for graphics that need to be resized or printed at high resolution.

SVG is a vector-based graphics technology, which means that it creates an image using mathematical equations that define lines, curves, shapes, and colors. SVG images are resolution-independent, which means that they can be scaled up or down without losing quality. SVG is particularly useful for creating complex graphics and animations that need to be resized or printed at high resolution. SVG also supports interactivity and animation, but its overhead can be higher than canvas, making it slower for drawing and animating large numbers of objects.

In summary, canvas is best for real-time and interactive graphics, while SVG is best for complex and scalable graphics. The choice between the two depends on the specific requirements of your project.
==============================================

8. HTML 5 features

Following are the new features in HTML5 : 
There are new semantic elements - header , footer , section , nav , article , aside
New graphic elements like svg , canvas

New apis - localstorage , session storage , geolocation , drag and drop , server sent events , web workers
Audio and video tags
New form controls like datalist , output
New form input types like color , range ,number , url , email , search , tel, datetime ,time , month ,week etc.
New input attributes like placeholder , multiple , autocomplete , autofocus , required,min and max , width and height ,list , formaction ,formnovalidate , formtarget ,formmethod, formenctype etc.
New form attributes autocomplete, novalidate

=====================
9. geolocation

function getLocation() {
  if (navigator.geolocation) {
    navigator.geolocation.getCurrentPosition(showPosition);
  } else { 
    x.innerHTML = "Geolocation is not supported by this browser.";
  }
}

function showPosition(position) {
  x.innerHTML = "Latitude: " + position.coords.latitude + 
  "<br>Longitude: " + position.coords.longitude;
}

============
10. drag and drop API
<script>
function allowDrop(ev) {
  ev.preventDefault();
}

function drag(ev) {
  ev.dataTransfer.setData("text", ev.target.id);
}

function drop(ev) {
  ev.preventDefault();
  var data = ev.dataTransfer.getData("text");
  ev.target.appendChild(document.getElementById(data));
}
</script>
</head>
<body>

<div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)"></div>

<img id="drag1" src="img_logo.gif" draggable="true" ondragstart="drag(event)" width="336" height="69">

</body>

=====================
11. SSE
A server-sent event is when a web page automatically gets updates from a server. This was also possible before, but the web page would have to ask if any updates were available. With server-sent events, the updates come automatically.
Examples: Facebook/Twitter updates, stock price updates, news feeds, sport results, etc.

The EventSource object is used to receive server-sent event notifications:

var source = new EventSource("demo_sse.php");
source.onmessage = function(event) {
  document.getElementById("result").innerHTML += event.data + "<br>";
};

Create a new EventSource object, and specify the URL of the page sending the updates (in this example "demo_sse.php")
Each time an update is received, the onmessage event occurs
When an onmessage event occurs, put the received data into the element with id="result"

============
12. Range, audio, video
<input type="range" id="points" name="points" min="0" max="10">

<input type="datetime" id="meeting-time"
       name="meeting-time" value="2018-06-12T19:30"
       min="2018-06-07T00:00" max="2018-06-14T00:00">

<audio controls>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
  Your browser does not support the audio tag.
</audio>

autoplay	 - autoplay	Specifies that the audio will start playing as soon as it is ready
controls -	controls	Specifies that audio controls should be displayed (such as a play/pause button etc)
loop	 - loop	Specifies that the audio will start over again, every time it is finished
muted	- muted	Specifies that the audio output should be muted
preload -	auto,metadata, none	- Specifies if and how the author thinks the audio should be loaded when the page loads
src	- URL  -	Specifies the URL of the audio file

======
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
  Your browser does not support the video tag.
</video>

height -	pixels	Sets the height of the video player
poster -	URL	Specifies an image to be shown while the video is downloading, or until the user hits the play button
width -	pixels	Sets the width of the video player

==========================
13. data types in JavaScript
As of now there are 6 data types in JavaScript :

 string , boolean , number , undefined , null, object , symbol

Object is a composite data type and rest all are primitive data types
symbol is a new data type introduced in ES6

In JavaScript, there are six primitive data types:

Number: represents numeric values. Examples include 1, 2.5, -3, etc.
String: represents textual values. Examples include "hello", 'world', "123", etc.
Boolean: represents true/false values. Examples include true and false.
Undefined: represents a value that has not been assigned a value. A variable that is declared but not initialized has the value undefined.
Null: represents a deliberate non-value. It is used to represent a variable that has no value.
Symbol: represents a unique identifier. Symbols are new to JavaScript as of ECMAScript 6.
In addition to these primitive data types, JavaScript also has one non-primitive data type:

Object: represents a collection of key-value pairs. An object can contain properties that are either primitive data types or other objects. Objects are used to represent more complex data structures.
Note that in JavaScript, variables are not statically typed, which means that the data type of a variable can change during runtime. This is known as dynamic typing, and it allows for more flexibility in programming.
===================================
14. null vs undefined



===============
15. typeof

typeof([])
'object'

Number('ABC')
NaN
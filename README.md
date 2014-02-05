#Front-end Job Interview Questions

This repo contains a number of front-end interview questions that can be used when vetting potential candidates. It is by no means recommended to use every single question here on the same candidate (that would take hours). Choosing a few items from this list should help you vet the intended skills you require.

[Rebecca Murphey](http://rmurphey.com/)'s [Baseline For Front-End Developers](http://rmurphey.com/blog/2012/04/12/a-baseline-for-front-end-developers/) is also a great resource to read up on before you head into an interview.

**Note:** Keep in mind that many of these questions are open ended and could lead to interesting discussions that tell you more about the person's capabilities than a straight answer would.

## <a name='toc'>Table of Contents</a>

  1. [Original Contributors](#contributors)
  1. [General Questions](#general)
  1. [HTML Questions](#html)
  1. [CSS Questions](#css)
  1. [JS Questions](#js)
  1. [jQuery Questions](#jquery)
  1. [Coding Questions](#jscode)
  1. [Fun Questions](#fun)
  1. [Other Great References](#references)

####[[⬆]](#toc) <a name='contributors'>Original Contributors:</a>

The majority of the questions were plucked from an [oksoclap](http://oksoclap.com/) thread created originally by [Paul Irish](http://paulirish.com) ([@paul_irish](http://twitter.com/paul_irish)) and contributed to by the following individuals:

* [@bentruyman](http://twitter.com/bentruyman) - http://bentruyman.com
* [@cowboy](http://twitter.com/cowboy) - http://benalman.com
* [@ajpiano](http://ajpiano) - http://ajpiano.com
* [@SlexAxton](http://twitter.com/slexaxton) - http://alexsexton.com
* [@boazsender](http://twitter.com/boazsender) - http://boazsender.com
* [@miketaylr](http://twitter.com/miketaylr) - http://miketaylr.com
* [@vladikoff](http://twitter.com/vladikoff) - http://vladfilippov.com
* [@gf3](http://twitter.com/gf3) - http://gf3.ca
* [@jon_neal](http://twitter.com/jon_neal) - http://twitter.com/jon_neal
* [@wookiehangover](http://twitter.com/wookiehangover) - http://wookiehangover.com
* [@iansym](http://twitter.com/iansym) - http://twitter.com/iansym

####[[⬆]](#toc) <a name='general'>General Questions:</a>

* What did you learn yesterday/this week?
* What excites or interests you about coding?
* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
* Talk about your preferred development environment. (OS, Editor, Browsers, Tools etc.)
    + A: osX, Sublime Text and plugins, normal browser is Chrome and inspector, Firefox with agents to test other browser.
* Can you describe your workflow when you create a web page?
    + A: [Portfolio](http://www.smashingmagazine.com/2013/06/25/workflow-design-develop-modern-portfolio-website/)
    + A: Actually, for me as a dev from coding background. I might focus on interactions with backends. How to consume APIs and how the performance ? CSS spirit, js minimization and etc.
* Can you describe the difference between progressive enhancement and graceful degradation?
    + A: [Opera Explaination](http://dev.opera.com/articles/view/graceful-degradation-progressive-enhancement/) In a nutshell, graceful degradation is the practice of building your web functionality so that it provides a certain level of user experience in more modern browsers, but it will also degrade gracefully to a lower level of user in experience in older browsers. Progressive enhancement is similar, but it does things the other way round. You start by establishing a basic level of user experience that all browsers will be able to provide when rendering your web site, but you also build in more advanced functionality that will automatically be available to browsers that can use it.
  * Bonus points for describing feature detection
    + A: [Feature detecting](http://jibbering.com/faq/notes/detect-browser/#bdFD) It is the direct one-to-one relationship in the implemented tests that avoids the need to identify the specific browser because whatever browser it is it either will support all of the required features or it will not. That would mean testing the feature itself (to ensure that it exists on the browser) and possibly aspects of the behaviour of that feature.
* Explain what "Semantic HTML" means.
    + A: Semantic HTML is the use of HTML markup to reinforce the semantics, or meaning, of the information in webpages rather than merely to define its presentation or look. Semantic HTML is processed by regular web browsers as well as by many other user agents. CSS is used to suggest its presentation to human users.
    
    + It's useful because:

        1. Browsers can correctly apply your CSS (Cascading Style Sheets), describing how each type of content should look. You can offer alternative styles, or users can use their own; as long as you've labeled your elements semantically, rules like "I want headlines to be huge" will be usable.

        2. Screen readers for the blind can help them fill out a form more easily if the logical sections are broken into fieldsets with one legend for each one. The blind user can say, "oh, this section doesn't apply to me, so I can skip ahead," just as you would do by glancing at it.
      
        3. Mobile phones can switch to a numeric keyboard when they see a form input of type "tel" (for telephone numbers).

* How would you optimize a websites assets/resources?
      * [Yahoo performance rulse](http://developer.yahoo.com/performance/rules.html)
      * [NewRelic](http://www.sitepoint.com/web-site-optimization-steps/)
      * **Minimize HTTP requests**: combining all scripts into a single script, and similarly combining all CSS into a single stylesheet. Combining files is more challenging when the scripts and stylesheets vary from page to page, but making this part of your release process improves response times.
      * **File minification**: 
      * **CDN Hosted**
      * **Add a expires or a cache-control header**. For static components: implement "Never expire" policy by setting far future Expires header. For dynamic components: use an appropriate Cache-Control header to help the browser with conditional requests
      * **Gzip components**: Compression reduces response times by reducing the size of the HTTP response.
      * **Component positions** : Put Stylesheets at the Top and put scripts on the bottom. Moving stylesheets to the document HEAD makes pages appear to be loading faster. This is because putting stylesheets in the HEAD allows the page to render progressively. The problem with putting stylesheets near the bottom of the document is that it prohibits progressive rendering in many browsers, including Internet Explorer. These browsers block rendering to avoid having to redraw elements of the page if their styles change. The user is stuck viewing a blank white page.
      * **Minor things inclueds no 404s**, remove duplications, use GET as much as possible, minimize the number of iFrames, split components to enable parallel downloads.

* Why is it better to serve site assets from multiple domains? 
    * A: Maximize parallel downloads. But due to DNS lookup penalty and the size of components, the number of domains various.
* How many resources will a browser download from a given domain at a time? 
    * A: Two, from http/1.1 spec.
* Name 3 ways to decrease page load. (perceived or actual load time)
    * CDN hosted.
    * Conbining all scripts. CSS sprites.
    * Cache.

* If you jumped on a project and they used tabs and you used spaces, what would you do?
  * Suggest the project utilize something like EditorConfig (http://editorconfig.org)
  * Conform to the conventions (stay consistent)
  * `issue :retab! command`
* Write a simple slideshow page
  * Bonus points if it does not use JS. (Pure css trick. [scriptless-slides](https://github.com/bytasv/scriptless-slides)
* What tools do you use to test your code's performance?
  * Profiler: 
  * JSPerf
  * Dromaeo
* If you could master one technology this year, what would it be?
* What are the differences between Long-Polling, Websockets and SSE?
  * A: Long-polling is a normal http request but the server won't response until a new info available. The client will initial another request upon receiving the new info.
      SSE server sent event, server executes javascript and open a connection with client. 
      Websocket: create TCP connection to server, and keep is as long as needed. Server or client can easily close it. Bidirectional communication - so server and client can exchange data both directions at any time. It is very efficient if application requires frequent messages. WebSockets do have data framing that includes masking for each message sent from client to server so data is simply encrypted.Main advantage of WebSockets for server, is that it is not HTTP request (after handshake), but proper message based communication protocol. That allows you to achieve huge performance and architecture advantages.  
* Explain the importance of standards and standards bodies.
    * Eliminate these discrepancies and formalize the de facto standards, enabling you to create sites that worked reasonably well across all browsers. Standards bodies such as the World Wide Web Consortium (W3C) were created as forums to establish agreement across the industry and among vendors.

* What is FOUC? How do you avoid FOUC?
* Do your best to describe the process from the time you type in a website's URL to it finishing loading on your screen.

####[[⬆]](#toc) <a name='html'>HTML Questions:</a>

* What's a `doctype` do?
* What's the difference between standards mode and quirks mode?
* What are the limitations when serving XHTML pages?
  * Are there any problems with serving pages as `application/xhtml+xml`?
* How do you serve a page with content in multiple languages?
  * What kind of things must you be wary of when design or developing for multilingual sites?
* What are `data-` attributes good for?
* Consider HTML5 as an open web platform. What are the building blocks of HTML5?
* Describe the difference between cookies, sessionStorage and localStorage.
* Can you explain the difference between `GET` and `POST`?

####[[⬆]](#toc) <a name='css'>CSS Questions:</a>

* Describe what a "reset" CSS file does and how it's useful.
* Describe Floats and how they work.
* What are the various clearing techniques and which is appropriate for what context?
* Explain CSS sprites, and how you would implement them on a page or site.
* What are your favourite image replacement techniques and which do you use when?
* CSS property hacks, conditionally included .css files, or... something else?
* How do you serve your pages for feature-constrained browsers?
  * What techniques/processes do you use?
* What are the different ways to visually hide content (and make it available only for screen readers)?
* Have you ever used a grid system, and if so, what do you prefer?
* Have you used or implemented media queries or mobile specific layouts/CSS?
* Any familiarity with styling SVG?
* How do you optimize your webpages for print?
* What are some of the "gotchas" for writing efficient CSS?
* What are the advantages/disadvantages of using CSS preprocessors? (SASS, Compass, Stylus, LESS)
  * If so, describe what you like and dislike about the CSS preprocessors you have used.
* How would you implement a web design comp that uses non-standard fonts?
  * Webfonts (font services like: Google Webfonts, Typekit etc.)
* Explain how a browser determines what elements match a CSS selector?
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
* List as many values for the display property that you can remember.
* What's the difference between inline and inline-block?
* What's the difference between a relative, fixed, absolute and statically positioned element?

####[[⬆]](#toc) <a name='js'>JS Questions:</a>

* Explain event delegation
  A: When you have a parent node with multiple children, instead of adding event listener to each child, just add it to the parent.

```html
  <ul id="parent-node">
  <li id="child1">Item1</li>
  <li id="child2">Item2</li>
  </ui>
``` 
```javascript
document.getElementById("parent-node").addEventListener("click", function(e){
  if (e.target && e.target.nodeName == "LI"){
  //dosomething
}
})
```
* Explain how `this` works in JavaScript
  
    * A: [There are exactly five different ways in which the value of *this* can be bound in the language.](http://bonsaiden.github.io/JavaScript-Garden/#function.this)

* Explain how prototypal inheritance works

    * When accessing the properties of an object, JavaScript will traverse the prototype chain upwards until it finds a property with the requested name.

* How do you go about testing your JavaScript?
    
    * Mocha and Chai. TDD and BDD.

* AMD vs. CommonJS?
  
    * [AMD vs CommonJS](http://addyosmani.com/writing-modular-js/)

* What's a hashtable?

    * [Hashtable](http://www.mojavelinux.com/articles/javascript_hashes.html)

* Explain why the following doesn't work as an IIFE: `function foo(){ }();`. 
* What needs to be changed to properly make it an IIFE? (immediate-invoked function expression)
    * A: var bar = function foo(){}(); When the parser encounters the function keyword in the global scope or inside a function, it treats it as a function declaration (statement), and not as a function expression, by default.

* What's the difference between a variable that is: `null`, `undefined` or `undeclared`?
  * A: undeclared variable means it doesnt exist so the type of it is undefined. null means the absence of a value.
  * How would you go about checking for any of these states?
    typeof x === 'undefined'
    if (x) //null check.

* What is a closure, and how/why would you use one?
  

* What's a typical use case for anonymous functions?
  * A: Callback function. Closure.
* Explain the "JavaScript module pattern" and when you'd use it.
  * A: [module-pattern](http://elegantcode.com/2011/02/15/basic-javascript-part-10-the-module-pattern/)
  * Bonus points for mentioning clean namespacing.
  * What if your modules are namespace-less?

* How do you organize your code? (module pattern, classical inheritance?)

* What's the difference between host objects and native objects?
  
  *  A: native object
object in an ECMAScript implementation whose semantics are fully defined by this specification rather than by the host environment.

NOTE Standard native objects are defined in this specification. Some native objects are built-in; others may be constructed during the course of execution of an ECMAScript program.

Source: http://es5.github.com/#x4.3.6

host object
object supplied by the host environment to complete the execution environment of ECMAScript.

NOTE Any object that is not native is a host object.

* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
  * A: function declaration. function calling. initial object. 

* What's the difference between `.call` and `.apply`?
  * A: call take arguments listed explicitly, apply takes array of arguments.

* explain `Function.prototype.bind`?
  
* When do you optimize your code?
* Can you explain how inheritance works in JavaScript?
* When would you use `document.write()`?
  * Most generated ads still utilize `document.write()` although its use is frowned upon
* What's the difference between feature detection, feature inference, and using the UA string
* Explain AJAX in as much detail as possible
  
* Explain how JSONP works (and how it's not really AJAX)
* Have you ever used JavaScript templating?
  * If so, what libraries have you used? (Mustache.js, Handlebars etc.)
* Explain "hoisting".
* Describe event bubbling.
* What's the difference between an "attribute" and a "property"?
* Why is extending built in JavaScript objects not a good idea?
* Why is extending built ins a good idea?
* Difference between document load event and document ready event?
* What is the difference between `==` and `===`?
* Explain how you would get a query string parameter from the browser window's URL.
* Explain the same-origin policy with regards to JavaScript.
* Describe inheritance patterns in JavaScript.
* Make this work:
```javascript
[1,2,3,4,5].duplicate(); // [1,2,3,4,5,1,2,3,4,5]
```
* Describe a strategy for memoization (avoiding calculation repetition) in JavaScript.
* Why is it called a Ternary expression, what does the word "Ternary" indicate?
* What is the arity of a function?
* What is `"use strict";`? what are the advantages and disadvantages to using it?

####[[⬆]](#toc) <a name='jquery'>jQuery Questions:</a>

* Explain "chaining".
* Explain "deferreds".
* What are some jQuery specific optimizations you can implement?
* What does `.end()` do?
* How, and why, would you namespace a bound event handler?
* Name 4 different values you can pass to the jQuery method.
  * Selector (string), HTML (string), Callback (function), HTMLElement, object, array, element array, jQuery Object etc.
* What is the effects (or fx) queue?
* What is the difference between `.get()`, `[]`, and `.eq()`?
* What is the difference between `.bind()`, `.live()`, and `.delegate()`?
* What is the difference between `$` and `$.fn`? Or just what is `$.fn`.
* Optimize this selector:
```javascript
$(".foo div#bar:eq(0)")
```

####[[⬆]](#toc) <a name='jscode'>Code Questions:</a>


```javascript
modulo(12, 5) // 2
```
*Question: Implement a modulo function that satisfies the above*


```javascript
"i'm a lasagna hog".split("").reverse().join("");
```
*Question: What value is returned from the above statement?*

**Answer: "goh angasal a m'i"**

```javascript
( window.foo || ( window.foo = "bar" ) );
```
*Question: What is the value of `window.foo`?*

**Answer: "bar"** *(only if `window.foo` was falsey otherwise it will retain its value)*

```javascript
var foo = "Hello"; (function() { var bar = " World"; alert(foo + bar); })(); alert(foo + bar);
```
*Question: What is the outcome of the two alerts above?*

**Answer: "Hello World" & ReferenceError: bar is not defined**

```javascript
var foo = [];
foo.push(1);
foo.push(2);
```
*Question: What is the value of `foo.length`?*

**Answer: `2`**

####[[⬆]](#toc) <a name='fun'>Fun Questions:</a>

* What's the coolest thing you've ever coded, what are you most proud of?
* What are your favorite parts about the developer tools you use?
* Do you have any pet projects? What kind?
* What's your favorite feature of Internet Explorer?

####[[⬆]](#toc) <a name='references'>Other Great References:</a>

* http://programmers.stackexchange.com/questions/46716/what-technical-details-should-a-programmer-of-a-web-application-consider-before
* http://www.nczonline.net/blog/2010/01/05/interviewing-the-front-end-engineer/
* http://css-tricks.com/interview-questions-css/
* http://davidshariff.com/quiz/
* http://blog.sourcing.io/interview-questions

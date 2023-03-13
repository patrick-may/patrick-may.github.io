---
layout: page
title: Map My Shopping
description: Frontend Focused Flutter Application for Big-Box Shopping
img: assets/img/MMSLogo.png
importance: 1
category: coursework
---



This is a **flutter** application designed for mobile phone usage. Myself, along with two peers, were commisioned to be the designers and developers of this product with check-ins with our customers who ordered the app.

Throughout the primary development lifecycle, we followed a loose *Agile* framework in distribution of tasks and workload. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/MMSHomePage.JPG" title="Home Page" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/MMSListPage.JPG" title="List Page" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/MMSSearchPage.JPG" title="Search Page" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: MapMyShopping Home Page, when opening the app.
    Middle: Current Shopping List. 
    Right: Searching for Items
</div>

## Technical Jargon

- **Flutter** is a cross-device software development for applications, created by Google. It has significant built-in functionality through provided assets, widgets, etc. within its **Dart** programming language. The rendering engine itself is build in C++, but for our project we were working within Dart.
- **Hive** is an extremely lightweight noSQL database that functions through storing data in various "boxes". It allows for distributed, local storage of the end-user's device to be used within the program, and to store information from one usage of MapMyShopping to the next. 
- **RESTful APIs** were planned to be a portion of the project, where we could connect to an existing online database of shopping items and get dynamic information about product availability. We created some simple scripting connections within Dart, however we did not feel the need or desire to sign up for paid-APIs at this level of the project.
- **Widget Design and State Management** are both very important parts of Flutter development, and something that I engaged with frequently. 
- **Asynchronous Programming** was something I had to engage with briefly in some of the backend development of this project, primarily in awaiting asynchronous operations to finish to continue doing things imperatively.

## Lessons Learned
As my first real foray into **mobile development**, I now have a much greater perspective on how involved and complicated web/mobile development becomes, and also how development difficulty increases exponentially. 

**Decouple when possible**. Even within the project, as a group we were still working on related pieces that meant we each created bottlenecks for each other. It is not as simple as "delegating and dividing" different parts of the work. How impacted with one person be if another is running behind on their portion of the backend? We faced a couple challenges in that style that we spent much more time re-synchronizing than would have been spent if we just broke work in a better way.

**Check-in with the Customer** as much as possible. My development team was lucky to be closely connected to the customers we were working with, so our development never strayed from their end vision, however, other development teams did not have this luxury, and I can imagine that in a larger scale project it becomes even easier to be disconnected from what the customer really wants.
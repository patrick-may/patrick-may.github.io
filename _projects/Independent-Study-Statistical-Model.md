---
layout: page
title: IS Analyzer Project
description: An applied statistics project involving heaving webscraping and NLP processing
img: assets/img/wooimg.jpeg
importance: 1
category: coursework
---

# Hello Statistics!

This project spawned initially from an opportunity presented to me through my penultimate semester coursework. 
At the College of Wooster, I took *DATA-230: Applied Statistics* as a foray into the world of statistics and data science.
4-year-old high school statistics was really pulling its weight for me at the beginning of this course...
'Applied Statistics' is a course that has been just that -- applied, primarily covering linear and logistic regressions in the context of applying and fitting various models to real world datasets.
A substantial portion of the course has been building towards a free-form final project that is basically "go do statistics".
Of course, the project specification is sleighted towards working with existing datasets and building models on that pre-compiled data. 
As a computer scientist (and wanting an excuse to learn some webscraping and data processing), I instead immediately turned into the figurative brush in trying to first **build my own dataset** before using that data to play around with.
In a sense, this meant I did non-trivial work just to get to the starting point of my other peers, but thanks to an ammenable instructor, we modified the expectations of the project enough such that I still did statistics while accounting for the extra effort done in step 0.

Pre-preamble... complete!

# Motivation and Context 

At the College of Wooster (my undergraduate institution), there is substantial importance placed on our "**Independent Study**" project.
Our Independent Studies are year-long independent, individual research projects in the realm of each student's chosen major(s). 
As a senior in the computer science department, I am working on my own IS -- separate from this statistics project. Refer to other posts and pages on my site if you are interested in static analysis and understanding energy usage of programs. 
Back to an overview of ISes, each department differs somewhat, but generally each week seniors check in with an advisor in their department, who may or may not be an expert in the specific topic of the IS.
To be pompous, Independent Study is a very souped up version of a senior thesis at other institutions. Although I do not believe college rankings and special ranklists are anywhere near honest, for the last 20-ish years, [Wooster has been a premier undergraduate mentored research institution](https://wooster.edu/academics/research/).

I am not experienced in the machine learning space, but with increasingly ease of accessibility of generative AI, for the last year or so I was playing around with a dream to tune a GPT to independent studies and see the results -- for humor's sake.  
At this time, I was unaware of *where* I could collect IS training data, but at the beginning of the year I came across our college's [OpenWorks page](https://openworks.wooster.edu/). 

<center>**Bingo.**</center>

Now I have a source for where to collect data, as there is an "Independent Studies" publications page on Openworks. I also was reviewing final project writeups at this time, and saw that my statistics class was very open ended. *This is a perfect excuse to harvest all this data* ~~for personal project use~~ for a course project. I just need to *do* the collection.

# Webscraping, Go, Colly, and You 

My day job involves a lot of Selenium Automation in Groovy. My first thought for webscraping is exactly that -- lets do some kind of Selenium based script. After some quick ggoogling, I saw some discussion that webscraping with a browser automation tool may be using too powerful of a tool for the desired data collection. At the time, I was interested in poking around in Go, so a quick 'Go Webscraping' search later, I found myself point at [GoColly](https://go-colly.org/). Understand that this webscraping script is my first real `Go` code I've written, so some style may be forgone as I still cling onto my jumbled internalized program representation. 

If I'm doing some webscraping, lets peek into what an IS page on openworks [looks like](https://openworks.wooster.edu/independentstudy/10559/)

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/isthesismetadata.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/isthesismetadatainspect.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>



---
layout: page
title: SEC Database AutoScreener
description: Investment screening tool, built using polars and the public SEC API
img: assets/img/seclogo.png
importance: 1
category: personal
---

A deceptively difficult data analysis problem. 

## Need
As a college student heavily involved within the Jenny Investment Club, one of the United States' oldest and largest fully student-run investment groups (we collectively handle over $10 million!!!), part of club operations involves having club members find stocks for us to invest within. 

As a club, we have a variety of different hard and soft guidelines to help us screen through stocks, such as:
- **1 - 10 billion market cap (inclusive)**
- **ESG considerations** (we are a middle eastern liberal arts college)
- **Portfolio Diversification**. Would this stock overexpose us to a certain sector's risks?
- ***15% average growth, over 3 or 5 years in:***
    - Cash Flow
    - Revenue
    - Income

The most difficult quantitative benchmarks to pass are the various 15% growth metrics. These are actually somewhat *hard* to find, because they are commonly not possible screening axes within free screeners, and booting up excel and tracking down historical company data across balance sheets and income statements is tedious, especially in the early stages of stock research. 

I wanted to solve this problem to make my fellow club members stock research jobs a little bit easier. I initially started using the `yfinance` package within python, however I ran into multiple difficulties very quickly, in limited scope of data, validity of data (sometimes just wrong??), etc.

I then discovered that the SEC itself has a public API endpoint for looking up company information, documentation [here](https://www.sec.gov/edgar/search-and-access).

## Technologies
As this is less of a software engineering project and closer to that of a data analysis problem, I tried to keep things as simple and easy to change as possible by using a **jupyter notebook** for the data. 

Additionally, as I knew I was going to be doing datawrangling with a project such as this. However, I am only a novice working within `pandas`, so I instead capitalized on the opportunity to work with `polars`, a new rust-based dataframe library!

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/polarslogo.svg" title="Enter PolaRS" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Enter polaRS, a rust-based, blazingly fast, concurrent datawrangling library.
</div>

Polars has a multitude of benefits (and negatives) to consider, but for a simple project of my scale, anything would do, so why not dip my toes into the polars syntax?

Additionally, I was doing `RESTful API` queries, so I utilized some very simple functionality that comes with python's built in `requests` library. 

Then, you would imagine the problem is pretty simple, correct? Just:
- Follow SEC instructions to get all company CIKs (their database's lookup key)
- Find the CIK for a chosen stock of interest
- Construct API queries for information on stock about desired metrics
- Simple pct-change analysis 
- Results

*... not quite ...*

## xBrl (and why I won't be a business person)
xBrl, or e**X**tensible **B**usiness **R**eporting **L**anguage is a *somewhat* standardized flavor of XML for understanding business reports from companies, such as 10-Ks, 8-Ks, 20-Fs (for foriegn companies), etc. Without getting into the details of constructing specific API queries, it is easiest to get historical data of a **specific** xBrl tag. For example, if I identify the *Revenues* xBrl tag, then I can get the historical amounts for every form in a specific company's record. Then pipe this to filter for only yearly reports, and it *should* be easy to have a YoY percent change for our desired metric.

However... there is a big assumption here, in that the company is going to *always* going to tag their choice financial data under the *exact* same xBrl tag. For example, here is a example output after cleaning and filtering a query on `$AAPL`:

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/aaplstats.png" title="Tagging Inconsitencies: See Revenue Column" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Here, it is obvious that the query for `revenue` didn't use the right xBrl tag. Looking into it, that column was made with `"RevenuesTotal"` as the API endpoint. So, below are two more graphics. One is another AAPL query with a different `Revenues` endpoint. Another is a query on a different company, *still* with the "RevenuesTotal" endpoint tag.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/aaplstats2.png" title="Changed AAPL Tag" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/peristats.png" title="xBrl Insanity" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

So here, we see the root of the issue: while companies tend to be *self consistent* in their business tags (but not always), they *differ* from business to business as far as I can tell. Additionally, there does not seem to be a completely standardized selection of which xBrl tag is used -- although there are a few that are the most common, it is entirely possible that some companies will use a completely different tag for a certain accounting number.

I have faced a lot of challenge in trying to think of a *repeatable*, *short*, and *quick to-implement* solution to this problem, and have not had a ton of luck. For this scale of project, I believe it would be a rabbit hole to go down if I were to try and use CV parsing libraries to extract a specific xBrl tag, although larger companies and paid APIs do complete this service, I believe.
# Bootstrap 5 - Introduction & Building a Responsive Website

## Bootstrap

Bootstrap is the most popular **CSS Framework** for developing responsive and mobile first websites.
Bootstrap 5.2 is the newst version of Bootstrap. It supports all major browsers except Internet Explore 11 & down.

To see Bootstrap **Documentation**, [click here](https://getbootstrap.com/docs/5.2/getting-started/introduction/).

## CDN (Content Delivery Network)

CDN stand for Content Delivery Network that been around since the late 90s.  
A CDN brings content closer to the user improving the performance of the web service.  
They have Servers at hundreds of locations around the world. These locations are called **POP (Point of Presence)**.  
A server inside the POP can be called an Edge Server. 
Having many POPs all over the world ensures thatevey user can reach a fast-edged server close to them.

## Setting Bootstrap

Since Bootstrap is a library of Pre-Written CSS and JavaScript (as only CSS is not enough for some styling effects). Hence, we need to connect to that library Database. it is done by Adding CDN links of Bootstrap CSS and Javascript in the index.html file.

```HTML

    <!doctype html>
    <html lang="en">
        <head>
            <meta charset="utf-8">
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <title>Bootstrap demo</title>
            <link href="paste CDN Link for Bootstrap CSS" rel="stylesheet" integrity="given on Bootstrap official site" crossorigin="anonymous">
        </head>
        <body>
            <h1>Hello, world!</h1>
            <script src="paste CDN Link for Bootstrap JavaScript" integrity="given on Bootstrap official site" crossorigin="anonymous"></script>
        </body>
    </html>

```

CDN links are available in Bootstrap 5.2 Document on its official [website](https://getbootstrap.com/docs/5.2/getting-started/introduction/#cdn-links).

 **Bootstrap Library content are categorized majorly in 7 types**

 - Customize
 - Layout
 - Content
 - Forms
 - Components
 - Helpers
 - Utilities

## Layout 

This Category Contain mostly used CSS concepts like Breakpoints, Containers, Grid, CSS grid, Colums, etc.  

### Breakpoints in Bootstraps

In Present, Websites/Webapps are preferred to be Responsive in single code for various devices.
**Breakpoints** are customizable widths that determine how your responsive layout behaves across device or viewport sizes in Bootstrap. 

***Available breakpoints***

Bootstrap includes six default breakpoints, sometimes referred to as grid tiers, for building responsively.

| Breakpoint	    | Class infix	| Dimensions
| ----------------- | ------------- |
| Extra small	    | None	        | <576px
| Small	            | sm	        | ≥576px
| Medium	        | md	        | ≥768px
| Large	            | lg	        | ≥992px
| Extra large	    | xl	        | ≥1200px
| Extra extra large	| xxl	        | ≥1400px

Each breakpoint was chosen to comfortably hold containers whose widths are multiples of 12.

### Conainers and Breakpoint

**Containers**are the most basic layout element in Bootstrap and are required when using our default grid system. Containers are used to contain, pad, and (sometimes) center the content within them. While containers can be nested, most layouts do not require a nested container.

Bootstrap comes with three different containers:

- **.container**, which sets a max-width at each responsive breakpoint
- **.container-{breakpoint}**, which is width: 100% until the specified breakpoint
- **.container-fluid**, which is width: 100% at all breakpoints.

The table below illustrates how each container’s max-width compares to the original .container and .container-fluid across each breakpoint.

| ---- | Extra small | Small | Medium | Large | X-Large | XX-Large |
| ---- | <576px | ≥576px | ≥768px | ≥992px | ≥1200px | ≥1400px |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| .container	| 100%	| 540px	| 720px	| 960px	| 1140px	| 1320px |
| .container-sm	| 100%	| 540px	| 720px	| 960px | 1140px	| 1320px |
| .container-md	| 100%	| 100%	| 720px	| 960px	| 1140px	| 1320px |
| .container-lg	| 100%	| 100%	| 100%	| 960px	| 1140px	| 1320px |
| .container-xl	| 100%	| 100%	| 100%	| 100%	| 1140px	| 1320px |
| .container-xxl	| 100%	| 100%	| 100%	| 100%	| 100%	| 1320px |
| .container-fluid	| 100%	| 100%	| 100%	| 100%	| 100%	| 100% |

**Responsive containers** allow you to specify a class that is 100% wide until the specified breakpoint is reached, after which we apply max-widths for each of the higher breakpoints.

for example :
```

<div class="container-sm">100% wide until small breakpoint</div>
<div class="container-md">100% wide until medium breakpoint</div>
<div class="container-lg">100% wide until large breakpoint</div>
<div class="container-xl">100% wide until extra large breakpoint</div>
<div class="container-xxl">100% wide until extra extra large breakpoint</div>

``` 

above code snippet 
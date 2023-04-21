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

| Breakpoint	    | Class infix	| Dimensions |
| ----------------- | ------------- | ---------- |
| Extra small	    | None	        | <576px |
| Small	            | sm	        | ≥576px |
| Medium	        | md	        | ≥768px |
| Large	            | lg	        | ≥992px |
| Extra large	    | xl	        | ≥1200px |
| Extra extra large	| xxl	        | ≥1400px |

Each breakpoint was chosen to comfortably hold containers whose widths are multiples of 12.

### Conainers and Breakpoint

**Containers**are the most basic layout element in Bootstrap and are required when using our default grid system. Containers are used to contain, pad, and (sometimes) center the content within them. While containers can be nested, most layouts do not require a nested container.

Bootstrap comes with three different containers:

- **.container**, which sets a max-width at each responsive breakpoint
- **.container-{breakpoint}**, which is width: 100% until the specified breakpoint
- **.container-fluid**, which is width: 100% at all breakpoints.

The table below illustrates how each container’s max-width compares to the original .container and .container-fluid across each breakpoint.

| ---- | Extra small (<576px) | Small (≥576px) | Medium (≥768px) | Large (≥992px) | X-Large (≥1200px) | XX-Large (≥1400px) |
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
```HTML
<div class="container-sm">100% wide until small breakpoint</div>
<div class="container-md">100% wide until medium breakpoint</div>
<div class="container-lg">100% wide until large breakpoint</div>
<div class="container-xl">100% wide until extra large breakpoint</div>
<div class="container-xxl">100% wide until extra extra large breakpoint</div>

``` 

Above code snippet shows the use of different Class name for different container size for variuos device screensize.

> **Note :**
> 
> We can use all the Class name under single code as shown below. 
> Also all this class name are present in the Bootstrap Library with Pre-Written CSS code as per its function.
> 

```HTML
<div class="container container-sm container-md container-lg container-xl container-xxl">text / code / CSS styling / Blocks / ETC here</div>

```

## Grid System in Bootstrap (Major Topic)

I hope you all are familiar with the box model in CSS.

So, **Grid system** in Bootstrap uses powerful mobile-first flexbox grid to build layouts of all shapes and sizes thanks to a ***12 column system***, six default responsive tiers, Sass variables and mixins, and dozens of predefined classes.

Grid sysytem 2 main pre-define **Classes** known as "row" & "col". "col" class is nested inside "row" class **always**. Also, both "row" & "col" class is nested inside "Container" as shown below.

***Example 1***

```HTML
<div class="container">
  <div class="row">
    <div class="col">
      Column
    </div>
    <div class="col">
      Column
    </div>
    <div class="col">
      Column
    </div>
  </div>
</div>

```
> Output as 
>  
> | Column | Column | Column |
> | ----- | ----- | ----- | 
> 

The above example creates three equal-width columns across all devices and viewports using our predefined grid classes. Those columns are centered in the page with the parent .container.

### Special Cases and Example

It is to be noted that each "row" class contain a definite **12 Column** and  based on the required no. of col needed for the design. we show column in combination for representing one column. 
Further explanation : As shown in the ***Example 1*** above we can only see 3 column but each column is a combination **4 definite column shown as 1**. hence, adding upto "12" = "4 + 4 + 4". 

we can also define the Number of definite column that are to be combine to repesent a single column in the "col" class by naming the column class as **"col-N"** where N is the number of definite column to be combine.
Please refer to below examples

***Example 2***

```HTML
<div class="container">
  <div class="row">
    <div class="col-1 box"> 1 </div>
    <div class="col-1 box"> 2 </div>
    <div class="col-1 box"> 3 </div>
    <div class="col-1 box"> 4 </div>
    <div class="col-1 box"> 5 </div>
    <div class="col-1 box"> 6 </div>
    <div class="col-1 box"> 7 </div>
    <div class="col-1 box"> 8 </div>
    <div class="col-1 box"> 9 </div>
    <div class="col-1 box"> 10 </div>
    <div class="col-1 box"> 11 </div>
    <div class="col-1 box"> 12 </div>
    <div class="col-1 box"> 13 </div>
    <div class="col-1 box"> 14 </div>
  </div>
</div>

```
> Output as 
>  
> | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 |
> | - | - | - | - | - | - | - | - | - | - | - | - |
> | 13 | 14 |
>  

we can see there are maximum of only 12 column possible in a row, for column 13 and 14 it takes next row. 
Note : "box" is a class present in Bootstrap library for creating box around the content of that tag.

***Example 3***

let there be a responsive  website with 3 case of display devices 
1. Desktop
1. Ipad 
1. Phone

> for Desktop as 
>  
> | .               JOIN US              . |
> | ---- |
> 
> | YouTube | Hashnode | Discord | Twitter |
> | ---- | ---- | ---- | ---- |
> 

> for Ipad as
>  
> | .    JOIN US    . |
> | ---- |
> 
> | YouTube | Hashnode |
> | ---- | ---- |
> | Discord | Twiter |
> | ---- | ---- |
> 

> for Phone
>  
> | JOIN US |
> | ---- |
> | YouTube |
> | Hashnode |
> | Discord |
> | Twiter |
 

The code will be as shown below

 ```HTML
<!--See "col" class properly
and observe changes in them. 
 
for Desktop-->  

<div class="container">
  <div class="row">
    <div class="col-12 box"> 
        <h1> JOIN US </h1>
    </div>
    
    <!-- 12 divided by 3 = 4 column for Desktop
         12 divided by 6 = 2 column for Ipad    
         12 divided by 12 = 1 column for Phone
         Also "lg" "md" "sm" are the Breakpoint for Desktop, Ipad, Phone screen respectively. 
    -->
    
    <div class="col-lg-3 col-md-6 col-sm-12 col-md-6 col-sm-12 box"> 
        <h2> YouTube</h2>
    </div>
    <div class="col-lg-3 col-md-6 col-sm-12 box"> 
        <h2> Hashnode </h2>
    </div>
    <div class="col-lg-3 col-md-6 col-sm-12 box"> 
        <h2> Discord </h2>
    </div>
    <div class="col-lg-3 col-md-6 col-sm-12 box"> 
        <h2> Twitter </h2>
    </div>
  </div>
</div>

 ```

Please see the HTML comment in the code for the explanation of the code

 ## Margin and Padding in the Bootstrap

 Margin and Padding section is inside Spacing under **Utilities**.

*Notation* 

The classes are named using the format **{property}{sides}-{size}** for **xs** and {**property}{sides}-{breakpoint}-{size}** for **sm, md, lg, xl, and xxl**.

> 
> Where property is one of:
> 
> - m - for classes that set margin
> - p - for classes that set padding
> 
> Where sides is one of:
> 
> - t - for classes that set margin-top or padding-top
> - b - for classes that set margin-bottom or padding-bottom
> - s - (start) for classes that set margin-left or padding-left in LTR, margin-right or padding-right in RTL
> - e - (end) for classes that set margin-right or padding-right in LTR, margin-left or padding-left in RTL
> - x - for classes that set both *-left and *-right
> - y - for classes that set both *-top and *-bottom
> blank - for classes that set a margin or padding on all 4 sides of the element
> 
> Where size is one of:
> 
> - 0 - for classes that eliminate the margin or padding by setting it to 0
> - 1 - (by default) for classes that set the margin or padding to $spacer * .25
> - 2 - (by default) for classes that set the margin or padding to $spacer * .5
> - 3 - (by default) for classes that set the margin or padding to $spacer
> - 4 - (by default) for classes that set the margin or padding to $spacer * 1.5
> - 5 - (by default) for classes that set the margin or padding to $spacer * 3
> - auto - for classes that set the margin to auto
> 

## Conclusion

When you go through all the example and explanations and syntax, we are only studying syntax to write **Class names** of all the different property that we need like Breakpoint, containers, grid system, etc. 

We are not coding any CSS styling in the code or any other .css file on our computer but the class mention in the code are the pre-written class in the bootstrap library with there CSS styling code. 

Hence, we are only learning which Bootstrap library Class name to mention to obtained the required styling instead coding it.

Also, Watch the [Bootstrap video](https://www.youtube.com/watch?v=tiUy-0GpUlY&t=153s) for better understanding this notes.

Have Good Day.
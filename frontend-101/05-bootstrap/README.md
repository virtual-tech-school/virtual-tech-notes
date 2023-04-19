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
            <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-rbsA2VBKQhggwzxH7pPCaAqO46MgnOM80zW1RWuH61DGLwZJEdK2Kadq2F9CUG65" crossorigin="anonymous">
        </head>
        <body>
            <h1>Hello, world!</h1>
            <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-kenU1KFdBIe4zVF0s0G1M5b4hcpxyD9F7jL+jjXkk+Q2h455rYXK/7HAuoJl+0I4" crossorigin="anonymous"></script>
        </body>
    </html>

```

In the above code 
> <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-rbsA2VBKQhggwzxH7pPCaAqO46MgnOM80zW1RWuH61DGLwZJEdK2Kadq2F9CUG65" crossorigin="anonymous">
is for Bootstrap CSS and 
> <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-kenU1KFdBIe4zVF0s0G1M5b4hcpxyD9F7jL+jjXkk+Q2h455rYXK/7HAuoJl+0I4" crossorigin="anonymous"></script>
is for Bootstrap JavaScript.

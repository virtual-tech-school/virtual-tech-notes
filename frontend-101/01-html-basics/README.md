Contribute notes based on [this](https://www.youtube.com/watch?v=JLKy8apeLac&list=PL2kSRH_DmWVbKFpYn3drI8Qf66ZpvZ_3L&index=2) video now!
# HTML #
## Hypertext Markup Language ##
<code>! </code> - > Do this For Emmet Abbreviations.<br>
<br>
HTML has different tags to do different things.<br>
<h3>Types of tags.</h3>
<ul>
 <li> Ones that hold some content &lttag&gt..&lt/tag&gt (requires closing tag). </li>
 <li>Ones that does not hold any content &lttag&gt (self closing tags). </li>
</ul>
Tags are not case sensitive.(good practice to do all in smallcase).   
<br>
<h2>Understanding boilerplate of html.</h2>
<code> &lt!DOCTYPE html&gt </code> (tells the browser that this is an html document)<br>
<code> &lthtml lang="en"&gt </code>  (the root tag of a html document.)<br> 
It contains two main tags
<ul>
 <li> head tag </li>
 <li> body tag </li>
</ul>
<code>&ltmeta charset="UTF-8" &gt</code> (displays all content in ascii text). <br> 
<code>&ltmeta http-equiv="X-UA-Compatible" content="IE=edge"&gt</code> (helps to load in internet explorer). <br>
<code>&ltmeta name="viewport" content="width=device-width, initial-scale=1.0"&gt  </code> (to make your site responsive).<br>
<code>&lttitle&gtDocument&lt/title&gt </code> -> title of your web page. (name of the tab). <br>
<code>&ltbody&gt   &lt/body&gt </code> Things that you see on your webpage.<br>
Anything from the opening tag to the closing tag is known as html element.<br>
All html tags have attributes.<br>
Attributes are way to provide additional information about the tags.It is always defined in opening tag.<br>
Attributes always come in pair  -> name="value"
<h3>Some Common html tags. </h3>
1.Heading -> h1 to h6 where h1 is largest in size and most important and h6 is smallest in size and least important.<br>
2.Paragraph -> to write paragraph texts<br>
3.Links -> a tag (anchor tag) used to add links to web page . Has an attribute href which is used to add links.<br>
target="blank" opens link new tab <br>
4.Images -> img tag for images
<br>
<h5>It has following attribute. </h5>
1. src to add link of the image.<br>
2. alt - alternative text that will appear when image fails to load.<br>
3. width & height  - value default in pixels.<br>
<h4>Types of urls.</h4>
1. absolute url -> Links that are hosted on other websites.<br>
2. relative url -> Links that are hosted within website.<br>
<br>
Title atttribute -> if you hover over the content this title comes.
<h2>Style attribute</h2>
In html style attribute comes in pair
For eg.
<code>&lttag style="color :black";"background-color:blue" &gt&lt/tag&gt</code>
<h3>Some common css style properties</h3>
<ul>
 <li> background-color -> gives background color</li>
 <li> color </li>
 <li> font-family</li>
 <li> font-size </li>
 <li> text-allign </li>
 <li> margin -> adds some space out of box </li>
 <li> padding -> adds space inside of box
</li>
</ul>
<h3> Color representation. </h3>
<ul>
 <li> color (name of color).</li>
 <li> rgb (red green blue) value is from 0-255 of all three. <br>
   rgba - 4th value for opacity. (value 0-1).</li>
 <li> Hexadecimal color rrggbb value each value is between 0 to ff.</li>
 <li>hsl (hue saturation and lightness).<br>
     hsla a for opacity similar to rgba.</li>
 </li>
</ul>
hue -> degree on color wheel (value 0 to 360) 0 is red, 120 is green, 240 is blue. <br>
saturation -> % value to give a shade of grey ( 0% max shade of grey,100% no shade of grey).<br>
lightness -> % value where 0 is black and 100% is white.<br>
<h1> CSS (cascading style sheet) </h1>
css is used to format layout of a web page. <br>
It is very helpful as it helps setting layout for multiple pages at once. <br>
cascading means whatever you apply to parent gets applied to children as well. <br>
<h3>css can be added to html in 3 ways</h3>
1. Inline css -> using style attribute. <br>
2. Internal -> if we add a &ltstyle&gt..&lt/style&gt tag inside head tag.<br>
3. external css -> adds style in different file and add a link in html file.<br>

<h5>Linking css style sheet</h5>
&ltlink rel = "stylesheet" href="style.css"&gt <br>

<h3> To add a comment in html </h3>
<code> &lt!-- ..................... --&gt - </code> 



 






    

    
 

 

Contribute notes based on [this](https://www.youtube.com/watch?v=JLKy8apeLac&list=PL2kSRH_DmWVbKFpYn3drI8Qf66ZpvZ_3L&index=2) video now!
# **HTML** # 
HTML stands for Hyper Text Markup Language. <br>
<code>! </code> = For Emmet Abbreviations(also this brings in the boiler plate in VScode).<br>
<hr>

## **Tags in HTML** ## 
HTML has different tags to do different things.
<h3>Types of tags:</h3>
<ul>
 <li>Ones that hold some content &lttag&gt...&lt/tag&gt (requires closing tag). </li>
 <li>Ones that does not hold any content &lttag&gt (self closing tags). </li>
</ul>
Tags are not case sensitive (good practice to do all in smallcase)
<hr>

## **Understanding boilerplate of HTML** ##
1.<code> &lt;!DOCTYPE html&gt; </code> tells the browser that this is an HTML document.<br>
2.<code> &lt;html lang="en"&gt; </code>  the root tag of a HTML document.<br> 
  It contains two main tags
<ol>
 <li> &lt;head&gt; - contains metadata/information about the document like title, description, charset, link etc.</li> 
 <li> &lt;body&gt; - the body of the document which gets displayed on the web page.</li>
</ol>
3.<code> &ltmeta charset="UTF-8"&gt</code> displays all content in ASCII text. <br> 
4.<code> &ltmeta http-equiv="X-UA-Compatible" content="IE=edge"&gt</code> helps to load in internet explorer. <br>
5.<code> &ltmeta name="viewport" content="width=device-width, initial-scale=1.0"&gt  </code> to make your site responsive.<br>
6.<code> &lttitle&gtDocument&lt/title&gt </code>  title of your web page (name of the tab). <br>
7.<code> &ltbody&gt ... &lt/body&gt </code> content that you see on your webpage.<br>
Anything from the opening tag to the closing tag is known as HTML element. All HTML tags have attributes.<br>
Attributes are way to provide additional information about the tags. It is always defined in opening tag.<br>
Attributes always come in name="value" pairs.
<hr>
<h2><strong>Some Common HTML tags </strong></h2>
1. <strong>Heading</strong> : h1 to h6 , h1 is largest in size and most important whereas h6 is smallest in size and least important.<br>
2. <strong>Paragraph</strong> : to write paragraph texts.<br>
3.<strong>Links</strong> : <code> &lta&gt ... &lt/a&gt</code> tag (anchor tag) used to add links to web page . Has an attribute "href" that specifies the link that you want to redirect to.<br>
(target="_blank" opens link new tab) <br>
4.<strong>Images </strong> : img tag for images.
<br>
<h4>It has following attributes: </h4>
1. "src" to add link of the image.<br>
2. "alt" - alternative text that will appear when image fails to load.<br>
3. "width" & "height"  - value default in pixels.<br>
<h4>Types of urls(Uniform Resource Locator):</h4>
1. <em>absolute url</em> : Links that are hosted on other website.<br>
2. <em>relative url</em> : Links that are hosted within website.<br>
"title" attribute : if you hover over the content this title comes.

<br>
<br>

<strong>details </strong> tag in html :

The <details> element is used to create a disclosure widget, allowing you to provide additional information that can be toggled open or closed by the user. It's often used to hide or show additional content, like a dropdown panel.

<details>
  <summary>Click to reveal more</summary>
  <p>Hidden content here.</p>
</details>

In this example:

The <details> element acts as a container for the hidden content.
The <summary> element provides a clickable title for the disclosure widget.
When the user clicks on the summary, the hidden content (in this case, the paragraph)isrevealed.

you can visit to [mdn-docs](https://developer.mozilla.org/en-US/docs/Web/HTML)for more information.

<hr>
<h2><strong>Style attributes</strong></h2>
In HTML, style attribute comes in pair.<br>
For eg:<br>
<code>&lttag style="color: black; background-color: blue" &gt&lt/tag&gt</code>
<h3><strong>Some common css style properties</strong></h3>
<ul>
 <li> background-color </li>
 <li> color </li>
 <li> font-family</li>
 <li> font-size </li>
 <li> text-align </li>
 <li> margin -> adds some space out of box </li>
 <li> padding -> adds space inside of box
</li>
</ul>
<h3> <strong>Color representation</strong> </h3>
<ul>
 <li> color (name of color).</li>
 <li> rgb (red green blue) value is from 0-255 of all three. <br>
   rgba - 4th value for opacity. (value 0-1).</li>
 <li> Hexadecimal color rrggbb value each value is between 0 to ff.</li>
 <li>hsl (hue saturation and lightness).<br>
     hsla a for opacity similar to rgba.</li>
 </li>
</ul>
1.<strong>hue</strong> : degree on color wheel (value 0 to 360) 0 is red, 120 is green, 240 is blue. <br>
2.<strong>saturation</strong> : % value to give a shade of grey ( 0% max shade of grey, 100% no shade of grey).<br>
3.<strong>lightness </strong> : % value where 0 is black and 100% is white.<br>
<hr>

<h2> <strong>CSS (cascading style sheet)</strong> </h2>
CSS is used to format layout of a web page.It is very helpful as it helps setting layout for multiple pages at once. <br>
Cascading means whatever you apply to parent tag gets applied to children tag as well. <br>
<h3><strong>CSS can be added to HTML in 3 ways:</strong></h3>
1. <strong>Inline CSS</strong> : using style attribute. <br>
2. <strong>Internal CSS</strong> : if we add a &ltstyle&gt..&lt/style&gt tag inside head tag.<br>
3. <strong>External CSS</strong> : adds style in different file and add a link in HTML file.<br>

<h3><strong>Linking css style sheet:</strong></h3>
<code>&ltlink rel = "stylesheet" href="style.css"&gt </code><br>

<h3><strong> Comments in HTML </strong></h3>
<code>  &lt!--...--&gt  </code> <br>
Comments are not displayed in the browsers. You can use comments to explain your code, which can help you when you edit the source code at a later date. This is especially useful if you have a lot of code.
<hr>




 






    

    
 

 

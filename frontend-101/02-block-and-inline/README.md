Contribute notes based on [this](https://www.youtube.com/watch?v=ZYbajSqMrN4&list=PL2kSRH_DmWVbKFpYn3drI8Qf66ZpvZ_3L&index=3) video now!

# Block and Inline Elements

Every HTML element has a default display value, depending on what type of element it is.

## There are 2 display values-

1. Block level elements
2. Inline elements

<hr>

## Block Level Elements

A block level element always starts on a new line, and the browser automatically adds some space (a margin) on top and bottom of it.

A block level element also would always take full width available to it.

### Some block level elements are -

``````html


1. <address> </address>

2. <article> </article>

3. <aside </aside>

4. <blockquote> </blockquote>

5. <canvas>

6. <dl> </dl> (Description List)

7. <dt></dt> (Term / Name in the List)

8. <dd> </dd> (Description of a term / name in the List)

9. <fieldset> <fieldset> (Grouping Elements in a form)

10. <figure> </figure> (For Images with a caption)

11. <figcaption> (Caption of the image)

12. <footer> </footer>

13. <form> </form>

14. <h1> </h1> to <h6> </h6>

15. <header> </header>

16. <hr>

17. <li> </li> (List Item)

18. <ol> </ol> (Ordered List)

19. <ul> </ul> (Unordered List)

20. <main> </main>

21. <nav> </nav>

22. <noscript> </noscript> (Defines alternate content for the users that do not support client side scripts).

23. <p> </p>

24. <pre> </pre>

25. <section> </section>

26. <table> </table>

27. <tfoot> </tfoot>

28. <video> </video>

29. <div> </div>

``````
<hr>

## Inline Level Elements

An Inline Element does not start with a new line and it only takes up as much width as it needs.

### Some of the inline elements are-

``````html


1. <a> </a>

2. <abbr> </abbr>

3. <b></b>

4. <bdo> </bdo> (Overrides the current text direction)

5. <br>

6. <button> </button>

7. <cite> </cite> (Defines the title of the work)

8. <code> </code> (For a piece of computer code)

9. <dfn> </dfn> (The term that is going to be defined within the text)

10. <em> </em>

11. <i> </i>

12. <img>

13. <input>

14. <kbd> </kbd>

15. <label> <label>

16. <map> </map>

17. <q> </q> (Short quotation)

18. <samp> </samp> (Sample Output from a computer program)

19. <script> </script> (client side script)

20. <select> </select> (Drop-downs)

21. <small> </small> (Smaller Text)

22. <strong> </strong>

23. <sub> </sub>

24. <sup> </sup>

25. <textarea> </textarea>

26. <time> </time> (To define specific time)

27. <var> </var> (For variable values)

28. <span> </span> (Commonly used as a container for things)


``````
<hr>

## &lt;div&gt; &lt;/div&gt; Element

It is often used as a container for other HTML elements. It doesn't have any required attributes, but it can usse

1. style
2. class
3. id

It can be used to used to style block of elements with CSS


## &lt;span&gt; &lt;/span&gt; Element

This is an inline container used to mark up a part of a text or a part of a do Again, it has no required attributes but can use the same as above.

It can be used to style parts of text with CSS. 

<hr>

## Class Attribute

As the name suggests, a class can be used to represent a set of elements having similar properties. 

The class can also be used by JavaScript to access and manipulate elements with the specific class name.

A class is represented in CSS with a dot (.)

You can also give multiple classes to an element by separating the class names with a space.


## id Attribute

Unlike a class that can be represent multiple elements, id attribute is used to specify a unique ID for an HTML element.

You should not have more than one element with the same ID in an HTML document.

It can be used to point to a specific style declaration in a style sheet, and it can also be used by JS to access and manipulate the element with the specific ID.

It is represented in CSS with a hashtag (#).

The major difference between a class and an id is that class name can be used by multiple HTML elements, while an ID name must only be used by one HTML element with the page. 

<hr>

## HTML Bookmarks with ID and Links

It is used by a web page to allow readers to jump to a specific part of a web page.

They can be useful if your page is very long.

To use a bookmark, you can give an ID to any element you want to bookmark, and then add a link to it.

You can add the links from the same page or from some other page too.









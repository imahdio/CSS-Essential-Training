# 03-The Box Model
## Introduction to the box model
>-CSS box model is the foundation of layout on the web. It's set of rules that defines how elements are sized, the total amount of space they take up and where they are positioned in relation to each other.  
-In this chapter we'll talk about how elements occupy space based on the type of element, inline or block.  
>-These are five properties that make up the box model:  
>1. Width
>2. height
>3. padding
>4. margin
>5. border 

incorporate-take in or contain (something) as part of a whole
## Inline, block, and display
>-there are two main types of HTML elements: inline and block-level  
>-❶ inline elements like `<a> `, `<span>` , `<strong>`
>1. take up the same space as the content contained within their tags.
>2. are displayed in a line, side by side, starting from the left.
>3. The element's content will only wrap to the next line if the content can't fit on the same line within its container(viewport).
>
>-❷ block elements like `<p>` , `<h1>` , `<article>` , `<section>`
>1. same height as content , same width as container(viewport)
>2. always starts on a new line and stack on top of each other
>3. the majority of elements are block-level.
>
>-check if an element is block or inline ([experiment with example code in here](https://codepen.io/christinatruong/pen/zXvQZE?editors=1100)):
><table>
>    <tr><th>add two elements next to each other</th><th>add a background color to the element</th><th>add width and height</th>
>    </tr>
>    <tr><td><ul><li>if start another line is block level</li><li>if it displays on the same line is inline level</li></ul></td><td><ul><li>if the color stretches all the way across the container(viewport), it's a block element</li><li>If it only spans the width of the actual content, then it's an inline element.</li></ul></td><td><ul><li>it changes the size of the element for block elements</li><li>adding width and height has no effect for inline elements</li></ul></td>
>    </tr>
></table>
>
>-the `display` property change the default behavior of inline and block-level elements, using a value of `block`, `inline`, or `inline-block`.
>* add `display: block` to an inline element will make it display just like block elements
>* add `display: inline` to a block element will give it the characteristics of inline elements.
>* add `inline-block` apply the characteristics of both. it means:
>   1. the width and height values will be applied, just like block elements, but
>   2. the items are displayed side by side, and they only wrap when there's no longer any space in the container, just like inline elements.
>
>-separating content from style means instead of picking an HTML element that looks a particular way, choose the most semantic element for the content, and then change the display with CSS.

stack-a pile of objects, typically one that is neatly arranged

majority-the larger number or part of something

span-the full extent of something from end to end

container-*in my point of view* viewport
## The box model properties
>-The CSS box model describes the rectangular boxes that are generated for each HTML element which consist of:
>1. content box: contains the actual content added between the HTML tags, such as text or an image includes 2 following properties:
>    1. `width` property: sets the width of the content area
>    2. `height` property: sets the height of the content area
>2. `padding` property: adds or removes the space within the element. It surrounds the content area, and this space is included inside of the element.
>3. `border` property: adds between padding and margin. It surrounds the padding area.
>4. `margin` property: adds or removes space around the element. it surrounds the entire element.  
>![image](https://user-images.githubusercontent.com/64577273/148678117-77a2a113-8464-4571-872b-1a0e7eb0967e.png)
>
>-for box properties, the percentage and length data types are used.
>
>percentage unit|absolute length unit|relative length unit
>-|-|-
>it's defined by the size of its containing element. If you change the width of the container, then inside-container width will change as well.|most types of absolute units, are used for print, so for websites stick with pixels.|It dependents on the length of another element.
>![image](https://user-images.githubusercontent.com/64577273/148678538-f5a0d555-7ea4-470f-a125-cbd9f694287a.png)|![image](https://user-images.githubusercontent.com/64577273/148678719-d7966f63-333a-4408-9a93-680d59537069.png)|<ul><li><code>em</code> is defined by the font size of the parent element</li><li><code>rem</code> is defined by the font size of the root element</li></ul>![image](https://user-images.githubusercontent.com/64577273/148679161-0224c4f1-df86-4ab3-a7a6-5468ca9db267.png)
## The box properties syntax and usage
>-aa

omit-leave out or exclude (someone or something), either intentionally or forgetfully
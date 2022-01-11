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
>3. The element's content will only wrap to the next line if the content can't fit on the same line within its container(parent element or viewport).
>
>-❷ block elements like `<p>` , `<h1>` , `<article>` , `<section>`
>1. same height as content , same width as container(parent element or viewport)
>2. always starts on a new line and stack on top of each other
>3. the majority of elements are block-level.
>
>-check if an element is block or inline ([experiment with example code in here](https://codepen.io/christinatruong/pen/zXvQZE?editors=1100)):
><table>
>    <tr><th>add two elements next to each other</th><th>add a background color to the element</th><th>add<code>width</code>and<code>height</code>or<code>margine</code></th>
>    </tr>
>    <tr><td><ul><li>if start another line is block level</li><li>if it displays on the same line is inline level</li></ul></td><td><ul><li>if the color stretches all the way across the container(parent element or viewport), it's a block element</li><li>If it only spans the width of the actual content, then it's an inline element.</li></ul></td><td><ul><li><code>width</code>and<code>height</code>change the size of the element for block elements and<code>margine</code>take effect absolutly</li><li>adding<code>width</code>and<code>height</code>has no effect for inline elements ,<code>margine</code>only take effect on right and left side of the inline elements</li></ul></td>
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

container-*in my point of view* parentelement or viewport
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
>-let's take a closer look at each of the box properties, syntax and usage.  
-the `width` and `height` properties for:
>
>block and inline-block elements|inline elements
>-|-
>change the size of the content box|width and height have no effect unless we use the display property set to block or inline block
>![image](https://user-images.githubusercontent.com/64577273/148683366-16c97c46-af56-40a5-9a06-c1d80bd5190d.png)|![image](https://user-images.githubusercontent.com/64577273/148683385-c544da2b-0190-4db6-ae56-0a1f3927cd72.png)
>
>-the `padding` and `margine` properties:
>
>`padding` property|`margine` property
>-|-
>add or remove space inside of the element but around the content box|add or remove space around an element
>The longhand properties can be used to specify just a particular side to add the padding to.<br>![image](https://user-images.githubusercontent.com/64577273/148684088-e1f566c9-1b0f-4fd8-a32e-dbcab191d1d1.png)|The longhand syntax rules are the same as padding<br>![image](https://user-images.githubusercontent.com/64577273/148696685-0c8e6ec6-f486-4368-91fe-59198414c1e2.png)
>with the shorthand property all four sides can be defined. The values always follow a clockwise order, starting from the top, the second value is always the right, then the bottom, then the left.<br>![image](https://user-images.githubusercontent.com/64577273/148684258-c023f190-9c83-490e-b8f0-f8535cd76942.png)<br><br>The shorthand syntax can be shortened even further<br>![image](https://user-images.githubusercontent.com/64577273/148684588-6bd75870-90f1-474f-a13b-60fcbf43523e.png)|The shorthand syntax rules are the same as padding<br>![image](https://user-images.githubusercontent.com/64577273/148696946-22c9fd0e-9739-429e-bc9e-8b4027dc3ec4.png)
>You can also mix different types of length units<br>![image](https://user-images.githubusercontent.com/64577273/148684638-42ce46ce-3d84-4591-a5bc-8ee98f824b90.png)|mix different types the same as padding
>|<ul><li>zero values will remove the padding space</li><li>if the value is zero you can omit the unit</li><li>all values must be a positive number</li></ul><br>![image](https://user-images.githubusercontent.com/64577273/148684785-176af65e-a5a1-4955-86f5-7b4957c53192.png)|<ul><li>zero values will remove the margine space</li><li>if the value is zero you can omit the unit</li><li>**values can be negative numbers**</li><li>**can also be used with the keyword `auto`**</li></ul><br>
>
>-the `border` property:
>* displays a border between the margin and padding of an element.
>* When using the shorthand syntax for border the order of the values do not matter.
>![image](https://user-images.githubusercontent.com/64577273/148697614-720bca1a-08f2-4c27-8cb7-97b04540f72c.png)
>
>`border-width` property|`border-color` property|`border-style` property
>-|-|-
>Only the following values can be used<br><ul><li>absolute length unit</li><li>the keywords `thin`, `medium`, and `thick`</li></ul>![image](https://user-images.githubusercontent.com/64577273/148697879-eff21279-071c-48e7-a400-0db2cf4a427d.png)|any of the color values available<br>![image](https://user-images.githubusercontent.com/64577273/148697917-8352a4b1-0306-40e4-83e6-1314c03f0faf.png)|there are quite a range of options<br>![image](https://user-images.githubusercontent.com/64577273/148697948-fb4f93b1-b75f-4df7-a0a2-e9f5e3b427d6.png)<br>Notice: for more ways to declare the border values, refers to [this MDN documentation](https://developer.mozilla.org/en-US/docs/Web/CSS/border)
>
>-The dimensions of all of these properties can contribute to the total amount of space an element occupies.  
Notice: Margin does not contribute to the total size of the element since it adds space around the element but it does effect the amount of space that the element takes up. [check one example in here](https://user-images.githubusercontent.com/64577273/148698384-5eb8d7a2-ab5f-4083-8b3b-48802bc5dd09.png)    
>-when we start creating layouts with columns, and sidebars, and grids, understanding how these box properties take up space will be necessary, [check examples in here](https://user-images.githubusercontent.com/64577273/148698533-eb573cca-379c-4565-9af3-898b1c750826.png)

omit-leave out or exclude (someone or something), either intentionally or forgetfully

contribute-If something contributes to an event or situation, it is one of the causes of it
## Debugging the box model
>-there are 2 ways to experiment with the size or spacing of the elements:
>1. change setting the box properties on various elements in CSS file
>2. use the browser developer tools to inspect the element to show the corresponding CSS
>
>-there are 3 ways to inspect a specific element:
>1. hover over on that element in webpage, right-click to open the menu and select inspect.
>2. just select that element from the HTML panel of developer tools to be highlited
>3. use [this pointer icon](https://user-images.githubusercontent.com/64577273/148725918-6e1757b3-fd47-469b-b3c5-9946e1dc8d49.png), hover over the element you want to select and click on it.  
>
>-the box model representation is under the Styles or Layout tab in google chrome or firefox respectively. experiment with it through developer tools on [this html](Debugging-the-box-model/box-model.html) file.
![image](https://user-images.githubusercontent.com/64577273/148728367-a6a4be08-a4a7-458e-9eee-5bf71316e4b3.png)  
**Notice:** there is no default margin space on the left and right side of above demonstrated margin box, and that's why the values say zero in it.  
**Notice:** You can even edit CSS properties values to experiment right in the browser. Refresh the browser to reset the changes that you made in the Dev tool.  
-if you hover over the various properties on visual demonstartion of box model, it will highlight the color-coded corresponding areas, which is super helpful when debugging.  
-<a name="margin-collapsing"></a>margin collapsing **only affects on the top and the bottom margins**. [When I hover over the `H1` in the HTML panel](https://user-images.githubusercontent.com/64577273/148741291-3cf926bc-f48c-4ab2-96d5-b70dc2b4c2a7.png), you can see that there is margin on the top and bottom of the element. The margin bottom space stops right above the content box of the `H2`, but [if I hover over the `H2` element](https://user-images.githubusercontent.com/64577273/148741731-02a093d1-aebf-4347-9b15-47b70b447bbe.png), the margin top stops right below the content box of `H1`. Both of these margins are occupying the same space, even though they're coming from two different elements.

collapse-the process of hiding something or reducing its size, so it's not visible

margine collapsing- The top and bottom margins of blocks are sometimes combined (collapsed) into a single margin. [check MDN documentation for more info](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Mastering_margin_collapsing)
## Padding, margin, and border
>-there are 2 ways to distinguish between margin and padding
>1. inspecting each element with developer tools
>2. adding a background color or border to each element
>
>-experiment with [this code snippet](https://codepen.io/ma400/pen/RwLeowy):
>* the space between the first and second paragraph is created by margin collapsing.
>* following CSS declarations remove any margine between first 2 paragraphs:
>```css
>.first {
>  margin-bottom: 0;
>}
>.second {
>  margin-top: 0;
>}
>```
>-add `padding` in `span` tag as inline element. the padding space has been added to the element, but the horizontal position of the element remains.  
-add `margin` in `span` tag as inline element. it actually will only apply to the left and right side [without margin collapsing](#margin-collapsing). if add `display: inline-block`, to the `span` selector, the margin is applied horizontally and vertically.  
-add `margin: 0;` to `span` selector. there's still some space between the inline elements which actually coming from the line break in the html. these solutions are available if you would need to remove the space:
>1. if we put `<span>` tags on the same line, that will remove the space. [result](https://codepen.io/ma400/pen/poWxprq)
>2. use `margin-left` on second `<span>` tag with a negative value. Just to nudge it over. this technique will only work with `margin` because `padding` does not accept negative values. [result](https://codepen.io/ma400/pen/RwLexjg)
>3. make a container just around `<span>` elements. set `font-size: 0;` in parent container. so it reduces all the characters down to zero, including the space. But `font-size` is an inheritable style. So we'll have to re-declare the `font-size` for the child elements to override this inherited style. [result](https://codepen.io/ma400/pen/xxXypME)
>4. But now there are newer layout techniques that will work better for this scenario and will be discussed later on, in this course

quirk-an unusual habit or type of behavior, or something that is strange and unexpected

nudge-the act of pushing someone or something gently

aesthetic-concerned with beauty or the appreciation of beauty

as if-in such a way that something seems to be true

would need to-*in my point of view* only expressing hope and wish

So aside from aesthetics, another time you would need to remove the space as if you were using inline elements that were a specific width within a specific container size-*in my point of view* another time you want to remove the space of inline elements with a specific width and container size , regradless of attending to appreciation of beauty , use the taught direction of this lesson. [check here for more info](https://github.com/imahdio/CSS-Essential-Training/issues/10)
## 
# Layouts: Float and Position
## Introduction to float
>-Prior to the introduction of Flexbox and Grid Layout Modules, the Float property was used for creating entire document layouts such as adding a sidebar to the main content area or creating multiple columns.  
-there's only partial support for Grid and Flexbox in Internet Explorer.  
-global market share for Internet Explorer is less than 3%, and Microsoft has dropped support for it.  
-you need to support layouts with floats in:
>1. projects using an old code base, usually referred to as legacy code
>2. applications that were originally built for Internet Explorer
>3. simple layouts such as floating an image to have the text flow around it

sidebar-a vertical or horizontal column placed to the right or left of a webpage's primary content area, below or above the content area, footer, header, or any where in the theme.
## The float and clear properties
>-The float property allowed us to create magazine-style layouts with floated elements and text flowing around those elements.  
-The majority of structural HTML elements used to create page layouts are:
>* block-level elements
>* displayed at full width and stacked on top of each other
>
>-The float property can be used to change the normal document flow by floating elements to the left or right side of its container, resulting in the change of the positioning of the surrounding elements.  
>-experiment with [this codepen example](https://codepen.io/christinatruong/pen/ROQdZJ):
>1. uncomment `float: left;` to the image. This will place the image to the left side of its container. The text in the following paragraphs will fill the available area and line up right to the edge of the image.
>2. uncomment `margin: 10px;` to the image. it adds some margin in, to create a little space between the image and the text.
>3. comment out long html paragraph. Now the remaining two paragraphs will flow around the image since they both fit within its space.
>4. add clear class to the second paragraph to return it back to its normal flow.   
Notice: `clear` property clear the float of each element to return the normal flow. The values for `clear` can be `left` , `right` or `both` to specifically clear a left , right or left and right floats.

realize-become fully aware of (something) as a fact; understand clearly.

pave the way (for something/someone)-to make it possible or easier for something or someone to follow

majority-most of the people or things in a group

structural HTML elements-[Good definition](https://ixd-res.clintio.us/web/html/structural.html)

used to-refers to something familiar or routine [Great definition](https://www.merriam-webster.com/words-at-play/is-it-used-to-or-use-to)
 
line up-to arrange people or things in a straight line or row

take (someone or something) out of (someone or something)-To remove someone or something from something or some place

take it out from the normal flow-*based my study friend opinion* they are treated as if they don't exist in the flow of html then they are positioned as the user required

make room-to provide space for someone or something

fill up-become completely full

flow across (something)-To move across something in a smooth, fluid manner, as of a liquid
## Float and collapsed container
>-clearing the float of a specific element means return the remaining page back to its normal flow.
>![image](https://user-images.githubusercontent.com/64577273/151829804-a554f94a-ba90-4a53-a4ed-6b2ba232a680.png)  
>-<i>based my point of view and after many test and tries</i>, self-clearing the float of a specific element means take consider to size of floated elements including:
><table>
>    <tr><th>height</th><th>both height and width</th>
>    </tr>
>    <tr><td>If all the elements within the parent is floated, the height of the parent container will collapse to zero.<br><img src="https://user-images.githubusercontent.com/64577273/151859367-75204b9f-f8ac-4600-bf74-921512044ac4.png"></td><td><ul><li>The parent does not recognize the height of the floated element, and will only wrap around the non-floated child elements the paragraph, in this example.</li><li>the paragraph area does not fully recognize the weight of the floated elements, and its background stretchs alongside of images. <a href="https://codepen.io/imahdio/pen/PoOPgVZ">codepen example</a><img src="https://user-images.githubusercontent.com/64577273/151862516-f62fe8ec-d110-47c9-9766-0bc00305bce6.png">or<img src="https://user-images.githubusercontent.com/64577273/151858989-874408ad-094d-4b83-b723-7f0c6925ceb5.png"><br>or<br><img src="https://user-images.githubusercontent.com/64577273/151859969-7995fa6d-a5fd-46b2-a1ce-5d21e6698d18.png"></li></ul></td>
>    </tr>
>    <tr><td colspan=2><b>self-clearing option 1:</b><br><code>overflow: hidden;</code> or <code>overflow: auto;</code> property is a common technique for self-clearing floats.<br><img src="https://user-images.githubusercontent.com/64577273/151918836-78e7d4cf-8294-40f0-b400-eefd29994209.png"></td>
>    </tr>
>    <tr><td><b>self-clearing option 2:</b><br>add a specific CSS snippet, often referred to as the clearfix hack<br><pre><code>
.clearfix:after {
    content: "";
    display: table;
    clear: both;
}
</code></pre><img src="https://user-images.githubusercontent.com/64577273/151920898-daeb1b22-bf18-480a-9f44-6c60b6d71c87.png"><br>Note: <code>clearfix</code> is just the class name. If you want to use another class name, just make sure it matches in the CSS and the HTML.</td><td>this option only applicable to self clear the height of containers, not suit to clear the width of paragraph area</td>
>    </tr>
>    <tr><td colspan=2><b>self-clearing option 3:</b><br><code>display: flow-root;</code> property is newer way for self-clearing floats but it's not currently supported by all modern browsers and is still in the draft phase.</td>
>    </tr>
></table>
>
>-[caniuse.com](https://caniuse.com/) is a great reference to check browser support for any CSS property.  
>-`overflow` is actually used to specify how to display content that doesn't fit in its container.
>`overflow: hidden;`|`overflow: auto;`|`overflow: scroll;`|
>-|-|-
>clips the overflow of content|Auto adds a scroll bar, but only when there is overflowing content|always show a scroll bar on the X and Y axis, even when the content does not flow outside of its container
>may be used for decorative content, like an image, but isn't useful for text since clipped content can't be accessed|-|-
>
>-try out these 3 self clearing options with [this codepen example](https://codepen.io/christinatruong/pen/dLjeVV):  
>1. add the `float: left;` to the blue box. This will make the container collapse, since the only child elements are now floated.
>2. add the `overflow: hidden;` to containing element to self-clear the float of blue boxes.
>3. hide the `overflow` property and add newest option `display: flow-root;` instead.
>4. comment on the `display` property and try the clear-fix option. add this class to the parent element.  
Notice: The `:before` and `:after` pseudo-elements in CSS allows you to insert content onto a page without it needing to be in the HTML. It is often used to add fantasy content to an element with the content property.
>```css
>/* Add an arrow after links */
>a:after {
>  content: "→";
>}
>```

clearing or self-clearing floats mean take considering to size of float elements.

overflow-if a container or a place overflows, whatever is inside it starts coming out because it is too full

overflow property-it specifies what should happen if content overflows an element's box

past-beyond in something, farther than

clip-the act of cutting something in order to make it tidy or shape it

recap-to repeat the main points of an explanation or a description

stack-a pile of objects, typically one that is neatly arranged

underneath-directly under and usually hidden by something else
## Layouts and the box model
>-`box-sizing` property change how the box model interprets the size of an element based on various box properties
><table>
>    <tr><th><code>box-sizing: content-box;</code></th><th><code>box-sizing: border-box;</code></th>
>    </tr>
>    <tr><td><ul><li>Width and height values change the size of the content-box.</li><li>padding and border increase the size of the elements</li><li>Margin just adds the space around the element.</li></ul></td><td><ul><li>width and height values set the element dimensions include the padding and border space</li><li>this makes the content-box smaller, but the overall element will maintain the same width and height values without any adjustments.</li></ul><b>Notice:</b> even in this state, in lack of determination a specific height or weight for an element, add padding or border just increase the size of element and don't make the content-box smaller.</td>
>    </tr>
>    <tr><td><img src="https://user-images.githubusercontent.com/64577273/151974218-d67b7850-a653-4910-bc8d-2d15642bcbb3.png"></td><td><img src="https://user-images.githubusercontent.com/64577273/151974359-e1bd7e9d-316f-418c-b198-2a03ea3b23e8.png"></td>
>    </tr>
>    <tr><td>it's initial and default box-sizing value, so donot need to be specified.</td><td>Use <b>The Box Model Fix</b> by adding this code snippet to your projects<pre><code>
/* border box fix */
html {
    box-sizing: border-box;
}
*, *:before, *:after {
    box-sizing: inherit;
}
</pre></code>Notice: The asterisk (&midast;) is known as the CSS universal selectors. It can be used to select any and all types of elements in an HTML page.</td>
>    </tr>
></table>
>
>-use floats to create full page layout on [this codepen example](https://codepen.io/christinatruong/pen/OepEEP):
>1. set `width: 200px;` to sidebar and `width: 600px;` to main content area.  
Notice: because the wrapper has a width of 800 pixels. So the total of the two sidebar and main content columns has to be equal to 800 pixels or less.
>2. add `float: left;` to aside element.  
Notice: see how the main content box moves up underneath floated sidebar area. but its little text that says "main content" wraps next to the edge of the sidebar.
>3. add `float: left;` to article element to align it next to the sidebar.  
Notice: see how the footer background is just trying to stack underneath the non-floated element, the header. but its little text that says "footer" wraps around the floated elements.
>4. add `clear: both;` to the footer to return the layout back to the normal flow.
>
><table>
>    <tr><th><code>box-sizing: content-box;</code></th><th><code>box-sizing: border-box;</code></th>
>    </tr>
>    <tr><td><ol start="5"><li>keep adjusting the width and the height of the content box every time we change some padding to account for total box size</li></ol></td><td><ol start="5"><li>add the box model fix. Now if set the height and width back to 600px and 200px values respectively, it will fit within the container even with the padding values.</li></ol>Notice: since margin adds space around the element, It's still not included in the total size of the element in <code>box-sizing: border-box;</code> So if I was to add some margin to <code>&lt;article&gt;</code> element, the box will no longer fit.</td>
>    </tr>
></table>

aside-to or toward the side
# Project: Float and box model fix
>-experiment with float and box model fix on our project:
>1. add box model fix to [styles.css](project-float-and-box-model-fix/css/styles.css)  
Notice: this should be something that you add as the base CSS for all your projects.
>2. add `class="project-item"` to each project block in [index.html](project-float-and-box-model-fix/index.html), so that we can float the image to the left and have the text flow around it.
>3. create a new descendant selector `.project-item img` and add `float: left;`
>4. to nicely line up each project section, self clear the float of parent element of each project image by adding:
>```css
>.project-item {
>    overflow: hidden;
>}
>```
>5. to add a little space between the project image and surrounded text, add `margin-right: 20px;` to `.project-item img`
>6. to add a border between the project items, add `border-bottom: 1px dashed #343434;` to `.project-item`
>7. add `padding: 25px 0;` to `.project-item`
>8. to put each project title with the rest of the text, switch it around in HTML and put the image before the h3 tag. So, image will float left and everything will follow after it, including the heading.  
**Notice:** When you're copying, pasting and moving items around, it's easy to get unorganized. So, just make sure that your indentation stays the way it should and delete any extra spaces that you don't need.
>9. to nicely line up the project heading with the image, create a new descendant selector `.project-item h3` and add `margin-top: 0;`
>
>-the Legacy techniques, to create a two column layout with floats, a container would need to be created for the image and the text. Then both containers would be floated to create a two column layout.
>
>float|flexbox and grid<br>as newer layout techniques
>-|-
>mostly be used for floating text around the image|creating column layouts
>if your text is longer than your image, the remaining text will flow underneath<br>![image](https://user-images.githubusercontent.com/64577273/152190336-d421c427-9064-4b5f-9530-e8f033ba87ac.png)|To get the image on the left and all the text on the right<br>![image](https://user-images.githubusercontent.com/64577273/152190806-a95808f9-d0eb-4915-9b73-3822ad2b67f1.png)

line up-to arrange things in a row

point out-to direct someone's attention to (someone or something) by pointing
# Position
>-the position property specifies different type of positioning that can also be used to change the flow of the document. there are 5 different values includes:
><table>
>    <tr><th>static</th><th>relative</th><th>absolute</th><th>fixed</th><th>sticky</th>
>    </tr>
>    <tr><td><ul><li>default and initial value</li><li>elements not positioned</li></ul></td><td>relative to current position</td><td><ol><li>relative to its closest positioned ancestor element</li><li>if a positon not defined, it will be relative to the body element.</li><li>if body element not positioned, relative to initial viewable area (doesn't move along with page scrolling)</li></ol></td><td><ul><li>relative to the view port</li><li>stays in the same spot even on page scroll</li></ul></td><td><ul><li>relative to containing elements and viewport</li><li>it's still in the working draft phase and not recommendation</li><li>partial support in most modern browsers</li></ul></td>
>    </tr>
>    <tr><td></td><td colspan=4>any of the the top, right, bottom, or left properties must also be used to specify the placement of the positioned elements.</td>
>    </tr>
>    <tr><td></td><td><ul><li>does not affect the flow of the other elements at all</li><li>remain in the same spot until define any offset properties</li></ul></td><td><ul><li>remove from the normal flow once be declared</li><li>remain in the same spot until define any offset properties</li><li>it's relative to its nearest positioned container</li></ul></td><td><ul><li>remove from the normal flow once be declared</li><li>not affected by any positioned ancestor elements</li></td><td><ul><li>does not affect the flow of the other elements at all</li><li>stays in the initial spot until scroll the page then it becomes fixed when the value in the offset property has been met</li><li>will no longer be fixed once you scroll past its containing element</li></ul></td>
>    </tr>
>    <tr>
>    </tr>
></table>
>
>-experiment with above values on [this codepen example](https://codepen.io/christinatruong/pen/zXLemj):  
>1. scroll down to the relative class, and add in `position: relative;`. add `top: 10px;` and `right: 30px;` will push the box 10 pixels away from the top of its current position, and 30 pixels away from the right of its current position.
>2. add `position: absolute;` to the absolute class.
>
>affects|instruction
>-|-
>the absolute box removes from the normal flow|the fixed box was stacked below the absolute box, but has now moved behind it, to see, add `width: 100px;` to fixed class.
>The absolute box is currently positioned relative to the non positioned body|add `right:25%` and `bottom: 5%;` to absolute class, so it's 25% from the right, and 5% from the bottom of the initial viewable area (when it was initially loaded).
>add position to the ancestor of absolute element|add `position: relative;` to wrapper class. Now absolute element is 25% from the right, and 5% from the bottom of the wrapper container.
>add position to the closest ancestor of absolute element|add `position: relative;` to parent class, Now the absolute box is positioned to the parent container.
>3. go down to the fixed class and add `position: fixed;` and the offset properties `top: 0;` and `right: 0;`. it stays in the same spot even on scrolling down the page.
>4. add `position: sticky;` and `top: 10px;`. when scroll the page, sticky element going to stay where it is until it gets to 10 pixels away from the top of the view port. And then it turns into fixed positioning. Once you scroll past its containing element it will no longer be fixed.
>
>-based [caniuse.com](https://caniuse.com/) report, `position: sticky;` is still in working draft stage.  
-it may be tempting to use the position property for page layouts, but positioning shouldn't be used in this way, since it takes the element out of the stacking order and the normal flow, with the exception of relative. Stick to using position for styling smaller page components such as a fixed navigation bar, rather than large page layout blocks.

tempt-to encourage someone to want to have or do something, esp. something unnecessary or wrong
# Position and z-index
>-[this article](https://webdesign.tutsplus.com/articles/what-you-may-not-know-about-the-z-index-property--webdesign-16892) provides great definition for stacking context and stacking level  
-an element with a higher stack level is rendered in front of the element with the lower stack level. to see how the elements stack on the z-index, overlap them on each other.  
-experiment with [this codepen example](https://codepen.io/imahdio/pen/RwjoJJE):
>
>default stacking order|corresponding selector|explanation
>-|-|-
>5-positioned elements|`div.position`|
>4-inline elements, non-positioned|`span.inline`
>3-floated elements, non-positioned|`div.float`
>2-block level elements|`div.block 1`, `div.block2`|block 2 displays on top of block 1 because it comes after it in the HTML
>1-html and body||they are always at the bottom of the stack because all other elements are always nested within these tags. 
>
>-`z-index` property changes the default stacking order. it only works if the element has some type of position applied to it.
>1. add `position: relative;` to `.block1`, changes stacking level while keep it in the natural flow.  
Notice: The orange positioned element is still displaying on the very top because it comes after block1 in the HTML.
>2. add `z-index: 1;` property to `.block1`. Now, it's at the top of the stack. It doesn't matter what number you choose, but the higher the value, the higher the stacking level.
>3. add `z-index: 2;` property to `.position` to back on top of the stack.
>
>-Changing the stacking order with `z-index` is most useful for elements that always need to be displayed on top of other elements, such as drop down menus, tool tips, or a pop-up box.

remainder-a part of something that is left over when other parts have been completed, used, or dealt with.
## Chapter Quiz
>-`clear` property prevent other elements from floating beside an element.  
-on sites where the grid property is used, you have little expectation to see that the `float` property is used.  
-remember box model fix:
>```css
>html {
>  box-sizing: border-box;
>}
>*, *:before, *:after {
>  box-sizing: inherit;
>}
>```
>-the parent container (assigned with the class "parent") of a floating element is showing as collapsed. the available solutions include:
>state|fix
>-|-
>✔️|![image](https://user-images.githubusercontent.com/64577273/152738999-6ff6ac47-a8d9-4430-bac0-914cd8b23ce2.png)
>✔️|![image](https://user-images.githubusercontent.com/64577273/152739062-d3a3753e-1dee-4e9a-a61f-455c5a33712e.png)
>✔️|![image](https://user-images.githubusercontent.com/64577273/152739134-d24b6e09-82f7-4dce-a0ab-54e4266f4c11.png)
>❌|![image](https://user-images.githubusercontent.com/64577273/152739162-db02f2be-d378-4877-bafe-65fa1a0301cf.png)
>
>-while an absolute element is positioned **relative to its closest positioned ancestor**, a fixed element is positioned **relative to the viewport**.  
>-put adjacent text elements in two containers and float them both when you want to show the text elements in two separate columns.

adjacent-very near, or with nothing in between
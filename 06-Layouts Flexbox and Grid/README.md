# Layouts: Flexbox and Grid
## Introduction to Grid and Flexbox
>-Both Flexbox and Grid are new layout modules that can be used to create layouts that are more advanced than previous techniques.
><table>
>    <tr><th>Flexbox</th><th>Grid</th>
>    </tr>
>    <tr><td><ul><li>items are aligned on a single axis, to arrange items as rows or columns.</li><li>only deals with one dimension at a time.</li></ul></td><td><ul><li>arrange items into rows and columns at the same time</li><li>two-dimensional</li></ul></td>
>    </tr>
>    <tr><td>space distribution of items within the same axis</td><td>ideal for layouts that require more control with rows and columns.</td>
>    </tr>
>    <tr><td colspan=2><ul><li>supported in all modern web browsers and are currently a W3C Candidate Recommendation</li><li>introduce flexible solutions with whole new layout modules, terminology, properties, and rules.</li></ul></td>
>    </tr>
></table>

specialty-plural specialties, someone's specialty is a particular type of work that they do most or do best, or a subject that they know a lot about.

think of as-think of somebody/something as somebody/something, to consider someone or something in a particular way

space-the area of the div, so if you have an element with width 400px and height 400px, flexbox will utilize(use) that 400 x 400 space evenly

terminology-special words or expressions used in relation to a particular subject or activity
## Introduction to Flexbox
>-create various page layouts, aligning and sizing elements by
>* historically, float and sometimes displaying position
>* the flexible box layout or Flexbox for short with flexible layouts over all
>![image](https://user-images.githubusercontent.com/64577273/153207028-9d8acddd-e8cd-4536-8aa4-54883d359e3c.png)
>
>-make a basic layout with
>
>float<br>as legacy technique|flexbox
>-|-
>[require additional CSS hacks](https://github.com/imahdio/CSS-Essential-Training/blob/8888df0011aabde43777a916c98aac974578a81d/05-Introduction%20to%20float/README.md#float-and-collapsed-container) to make each item<ul><li>the same height as its content</li><li>equal height columns</li></ul>|the height of each flex item automatically adjusts to be the same height as the longest item without adding any additional CSS<br>[like this codepen example](https://codepen.io/imahdio/pen/GROWMBB)<br><img src="https://user-images.githubusercontent.com/64577273/153255971-110682d0-214b-42ac-a068-a457760d73fd.png">
>
>-to use Flexbox, the flex-container must be defined with one of these two values:
><table>
>    <tr><th>flex</th><th>inline-flex</th>
>    </tr>
>    <tr><td colspan=2>they're only added to the parent element<br><br><img src="https://user-images.githubusercontent.com/64577273/153211290-35e5cff3-0144-4284-823f-830d18543c90.png"></td>
>    <tr><td colspan=2>each <b>direct child element</b> within the <b>flex-container</b> is a <b>flex item</b>.<br><br><img src="https://user-images.githubusercontent.com/64577273/153258062-a853820d-1110-4703-9805-a28ca2bda073.png"></td>
>    </tr>
>    <tr><td colspan=2><b>by default</b>, flex items will automatically<ul><li>be displayed in a row</li><li>have the same size as their content</li></ul>Notice: you can set a specific size for flex items as well</td>
>    </tr>
>    <tr><td>flex-container will still span the width of its container<br><br><img src="https://user-images.githubusercontent.com/64577273/153248839-09c320b8-14b2-4735-ae57-efb443d60e46.png"></td><td>the flex-container<ul><li>will span the width of its content, the flex items</li><li>displays inline to other flex-containers</li></ul><img src="https://user-images.githubusercontent.com/64577273/153248613-80fa1c4a-f284-430a-a578-8f567c70d16f.png"><br>-Notice: <code>display: inline-flex;</code> doesn't change how the flex items are displayed. instead, it makes the flex-container display inline.</td>
>    </tr>
></table>
>
>-The two axis of flexbox includes
><table>
>    <tr><th>main axis</th><th>cross axis</th>
>    </tr>
>    <tr><td>flex items are laid out along the main axis.</td><td>the cross axis will always run perpendicular to the direction of the flex items.</td>
>    </tr>
>    <tr><td>The direction is horizontal by default, meaning flex items are arranged in rows</td><td></td>
>    </tr>
>    <tr><td>use the <code>flex-direction</code> property to change the direction of the main axis to run vertically</td><td></td>
>    </tr>
>    <tr><td colspan=2>Both axis also have start and end points.<br><img src="https://user-images.githubusercontent.com/64577273/153277606-b1823823-07e2-4173-bd86-94ce5533492c.png"></td>
>    </tr>
></table>

displaying position-*based my study friend opinion*, refer to the positioning properties

overall-taking everything into account

terminology-special words or expressions used in relation to a particular subject or activity

lay out-to spread something out, or to arrange things so you can see them easily

perpendicular-At an angle of 90° to the ground; vertical
## Flexbox: Orientation and ordering
>-experiment the orientation and ordering items on:
>* `flex-direction: column;` with [this codepen example](https://codepen.io/imahdio/pen/rNYwLBV)
>* `flex-direction: row;` with [this codepen example](https://codepen.io/imahdio/pen/dyZRXyR)
>
>-The `flex-direction` property determines the direction of the main axis using one of four values:
><table>
>    <tr><th colspan=2>1-<code>row</code></th><th colspan=2>3-<code>column</code></th>
>    </tr>
>    <tr><td colspan=2><ul><li>It's the default value.</li><li>The main start and main end depends on the writing mode of the document.</li><ul></td><td colspan=2>flex items:<ul><li>stack from top to bottom with vertical direction</li><li>expand the width of its container</li></ul><img src="https://user-images.githubusercontent.com/64577273/153773495-052bb365-55ae-4035-ac69-2f164eb53e43.png"></td>
>    </tr>
>    <tr><td><code>dir="rtl"</code><br>right to left language</td><td><code>dir="ltr"</code><br>left to right language</td><td><code>dir="rtl"</code><br>right to left language</td><td><code>dir="ltr"</code><br>left to right language</td>
>    </tr>
>    <tr><td>the main start, and the main end, will run right to left.<br><img src="https://user-images.githubusercontent.com/64577273/153773425-33dd8769-3500-450b-a8e2-41077e3ee0cf.png"></td><td>the main start, and the main end, will run left to right.<br><img src="https://user-images.githubusercontent.com/64577273/153773320-089dad74-f047-4cf6-aaab-bd23f30b8f50.png"></td><td>the cross start, and the cross end, will run right to left.</td><td>the cross start, and the cross end, will run left to right.</td>
>    </tr>
>    <tr><th colspan=2>2-<code>row-reverse</code></th><th colspan=2>4-<code>column-reverse</code></th>
>    </tr>
>    <tr><td colspan=2><ul><li>flip the order of horizontal items by reversing main start and main end</li><li>This re-ordering is only visual. The HTML is not changed.</li></ul></td><td colspan=2><ul><li>flip the order and alignment of the vertical items by reversing main start and main end</li><li>This re-ordering is only visual. The HTML is not changed.</li></ul><img src="https://user-images.githubusercontent.com/64577273/153773826-ed19aa9a-ec48-4911-a92a-9babd29f8b4a.jpg"></td>
>    </tr>
></table>
>-By default, Flexbox only aligns the flex items on a single axis.
>
>`flex-wrap: nowrap;`|`flex-wrap: wrap;`|`flex-wrap: wrap-reverse;`
>-|-|-
>it's the default value meaning flex items will not wrap.|layout the items over multiple rows|simultaneously wrap and reverse
>|<ul><li>there will be some space left, if there aren't enough flex items to fit within the whole container</li><img src="https://user-images.githubusercontent.com/64577273/153807221-cbdb60f7-4f00-44b0-98c1-a4f30cbf1a8d.png"><li>the items will automatically shrink to fit into one line, if the total width of the items are larger than the container.<img src="https://user-images.githubusercontent.com/64577273/153807331-f91f7984-08fd-4706-842f-b2b2001116bd.png">|the items will wrap into the next line, if there are more items to fit the container<br>![image](https://user-images.githubusercontent.com/64577273/153807705-ce39273b-de03-462a-9670-9f22ce2808f2.png)|<ul><li>reverse the cross start and cross end</li><li>The items are still in the same order on the main axis</li></ul>![image](https://user-images.githubusercontent.com/64577273/153807883-c973ea43-bd61-41ec-beb6-ee159a2bc4c2.png)
>
>-in the next lesson, we'll talk about additional flex properties we can use to determine how items expand and shrink.  
-`flex-flow` is the shorthand property for `flex-wrap` and `flex-direction`:  
![image](https://user-images.githubusercontent.com/64577273/153808766-6b98bf6f-631c-40b1-a672-fb94bc95a0db.png)

orientation-the position of something in relation to its surroundings

flip-turn over with a sudden quick movement

substitute-a person or thing acting or serving in place of another

shrink-become or make smaller in size or amount

feel like something-to seem to be something
## Flexible sizing
>-there are three properties used together to set the sizing of the flex-items
><table>
>    <tr><th>flex-grow</th><th>flex-shrink</th><th>flex-basis</th>
>    </tr>
>    <tr><td>determines how items will expand if there is extra space in the container</td><td>determines how items will shrink if there isn't enough space in the container</td><td>sets the initial size of the flex-items</td>
>    </tr>
>    <tr><td colspan=3>The W3C recommends using the shorthand property<br><code>flex: grow shrink basis;</code><br><code>flex: 0 1 100px;</code></td>
>    </tr>
>    <tr><td colspan=2>defined with a unit-less numeric value</td><td>used either with<ul><li>link values</li><li>percentages</li><li>key words</li></td>
>    </tr>
>    <tr><td><ul><li>defaults to zero, means if there's extra space in the container, do not expand to fill the space.</li><br><img src="https://user-images.githubusercontent.com/64577273/153839390-61bceec8-6a23-4769-bc2b-5cf7859a5d80.png"><li>If change the value to one, all the flex items will expand by the same amount to fill up the space.</li><br><img src="https://user-images.githubusercontent.com/64577273/153839682-841572ea-987f-4a09-96f7-01d55f78e924.png"></ul></td><td><ul><li>defaults to one, means if there isn't enough space in the container, shrink all the flex items by the same amount.</li><img src="https://user-images.githubusercontent.com/64577273/153840314-b933b86d-119f-4c0c-be42-63d45fc43bf1.png"><li>if set it to zero, means it won't shrink at all. So if there's not enough space in the container, it will overflow, unless you set the flex wrap to wrap.</li><a href="https://codepen.io/imahdio/pen/vYWJxjw">codepen example</a><br><img src="https://user-images.githubusercontent.com/64577273/153840472-154d14c7-aa67-43ff-a181-12f438f7ec2d.png"></ul></td><td><ul><li>It's ideal sizing. If there's enough space, make all the flex items the size declared with this value</li><img src="https://user-images.githubusercontent.com/64577273/153842232-d6300db2-d4c6-4d38-9fcf-c9871e1d1a9c.png"><li>If not, then shrink or grow according to the first two values.<img src="https://user-images.githubusercontent.com/64577273/153844716-592b0692-4179-4b8a-b5a4-a597f0282a28.png"></li></ul></td>
>    </tr>
>    <tr>
>    </tr>
></table>
>
>-`flex` property must be applied to the flex items directly, not in the container.
>to have the same size flex items|to have the different sizes flex items
>-|-
>apply the `flex` property to a selector that matches to all the flex items<br>![image](https://user-images.githubusercontent.com/64577273/153820766-6ec7bf86-835f-40d6-b7e1-0379dbde4e84.png)|`flex` property must be applied to the individual flex items.<br>![image](https://user-images.githubusercontent.com/64577273/153820872-b607c2ba-549d-4af5-a1ea-ff860b63f792.png)
>
>-[check out the MDM documentation](https://developer.mozilla.org/en-US/docs/Web/CSS/flex) to see many other types of flex values.

voice over-words that describe or comment on a film, advertisement, or video, which are spoken by a person who is not seen

link value-*based my study friend opinion*, the values that are linked to other related elements like inherited from the parent component, for example `auto`, `em`, `px`
## Flexbox exercise
>-create a basic flexbox layout [with this codepen example](https://codepen.io/imahdio/pen/BamwyGy):
>1. add `display: flex;` into flex-container to enable the flexbox layout mode.  
The flex items will now align horizontally.
>2. add `width: 500px;` into flex-container and `flex: 1 1 100px;` into flex-item.  
Since the container is 500 pixels, and there are five flex items, the flex-basis value of 100 pixels is applied.
>3. change `width: 600px;` in flex-container.  
because the flex-grow amount of one, the items will now be wider to filled up the extra space.
>4. change `flex: 0 1 100px;` in flex-item.  
flex-items won't expand, and there will be extra space.
>5. change `width: 400px;` in flex-container.  
the items will shrink
>6. change `flex: 0 0 100px;` in flex-item.  
the items will not shrink and will be sized to 100 pixels, according to the flex-basis value but will overflow, because the container is smaller than the total width of all the flex items.
>7. add `flex-wrap: wrap;` into flex-container.  
The item that doesn't fit, will now wrap onto the next row.
>8. change `flex: 1 0 100px;` in flex-item.  
Since it's the only item on the new second row, all the extra space in the row is applied to it.

feel like something-to seem to be something

incorporate-to include something as part of something larger
## Flexbox: Alignment
>-like already mentioned in [this summary](https://github.com/imahdio/CSS-Essential-Training/blob/f86f00131dfb1ac245975717bbfd7af6d59512a8/03-The%20Box%20Model/README.md#margin-and-layouts) and [this another one](https://github.com/imahdio/CSS-Essential-Training/blob/af46cb01a5f7e3ea419a0885e4a310c329bb569d/04-Typography/README.md#text-decoration-text-align-and-line-height), Prior to Flexbox, we used `margin: length auto;` and `text-align: center;` for center aligning elements horizontally, but  getting elements to align vertically required flexbox.  
-flexbox has two properties for aligning elements.
><table>
>    <tr><th>justify-content</th><th>align-items</th>
>    </tr>
>    <tr><td>aligns items on the main axis</td><td>aligns items on the cross axis</td>
>    </tr><td colspan=2>to center align the item vertically and horizontally, set the values for both properties to center<br><img src="https://user-images.githubusercontent.com/64577273/154042942-79be6510-87b2-4f31-b464-d0f5a8cf8bc9.jpg"></td>
>    <tr><td>experiment with below values on <a href="https://codepen.io/imahdio/pen/qBVPVNO">this codepen example</a>:<ul><li><code>start</code> : aligns flex items flush to each other at the start of the axis</li><li><code>center</code> : center-align the flex items</li><li><code>space-between</code> : distributes items evenly with the first item at the start of the axis and the last item at the end</li><li><code>space-around</code> : distributes the same space just on the left and right side of each item</li><li><code>Space-evenly</code> : distributes equal space around the items.</li></ul>check full list of possible values <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content">on MDN docs</a></td><td>experiment with below values on <a href="https://codepen.io/imahdio/pen/oNoGozx">this codepen example</a>:<ul><li><code>stretch</code> :  stretches the flex items along the cross axis.</li><li><code>center</code> :  center align items vertically along the cross axis.</li><li><code>start</code> : aligns the items from the top, <b>if the cross axis is vertical</b></li><li><code>end</code> : aligns items from the bottom, <b>if the cross axis is vertical</b></li></ul>check full list of possible values <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/align-items">on MDN docs</td>
>    </tr>
></table>

flush-on the same level so that no part is higher or lower or sticks out more than another

stick out-to go past (beyond) the surface or edge of something
## Project: Flexbox alignment
>-use flexbox to style contact info of the exercise file:
>1. change contact list container to `<ul class="contact-list">` in [index.html](Project-Flexbox-alignment/index.html)
>2. add below class to contact section of [style.css](Project-Flexbox-alignment/css/styles.css) to remove the bullets and left-side extra space from list.
>```css
>.contact-list {
>    list-style-type: none;
>    padding: 0;
>}
>```
>3. add `display: flex;` to contact-list class to align items horizontally.
>4. add `justify-content: center;` to center-align items within the container.  
Notice: `justify-content: space-between;` will distribute the flex items evenly by adding space between the items.
>5. add below class to contact section of [style.css](Project-Flexbox-alignment/css/styles.css) to target links.
>```css
>.contact-list a {
>    padding: 15px;
>    display: inline-block;
>}
>```
>Notice: we choose padding instead of margin to help with accessibility because it will make the click area bigger.  
>Notcie: links are inline elements. [based last table of this summary](https://github.com/imahdio/CSS-Essential-Training/tree/master/03-The%20Box%20Model#inline-block-and-display), to adjust links position vertically and horizontally when the padding is added, need to change its desplay to `display: inline-block;`
>
>6. add `text-align: center;` to footer selector of [style.css](Project-Flexbox-alignment/css/styles.css) to center-align inner contents while won't affect on flex items.  
>Notice: For any block-level element, I can apply `text-align: center;` to the element itself or I can add it to the container so all the elements will inherit this style.
>7. add `text-align: center;` to header of [style.css](Project-Flexbox-alignment/css/styles.css) to center-align all of its contents.  
>Notice: We didn't need to lay out the content in rows or columns or resize them, so there was no need to initiate a Flexbox layout for the header.  
>
>-CSS and programming in general is about learning how to use a bunch of different tools and then figuring out which tool is best for each scenario.

space out-position two or more items at an equal distance from one another

lay out-to arrange in a pattern or design
## Introduction to CSS Grid
>-CSS Grid is a layout method that includes new CSS properties and rules.  
>-prior to it, using grid-based layouts have been a common part of web design for a long time that required hacks and other workarounds.  
>-Let's go over some grid terminology.  
><table>
>    <tr><th>grids</th><th>gutters</th><th>grid lines</th><th>grid cell</th><th>grid track</th><th>explicit or implicit grid</th>
>    </tr>
>    <tr><td>broken down into evenly spaced columns and rows<br><img src="https://user-images.githubusercontent.com/64577273/154850962-1013a992-84d7-45ac-9b71-fcd4ea8679d1.png"></td><td>often included to add consistent spacing between columns</td><td>the horizontal and vertical lines that divide the grid into columns and rows<br><img src="https://user-images.githubusercontent.com/64577273/154853967-f93fe406-1c68-47db-b069-7e0d479f0e17.png"></td><td>refers to a single unit, defined by where the grid row and column intersect<br><img src="https://user-images.githubusercontent.com/64577273/154856516-2276398e-876e-469d-98af-ff3cb18170d8.png"></td><td>the space between two adjacent grid lines which is basically the columns and rows<img src="https://user-images.githubusercontent.com/64577273/154856861-6d2c00b3-ff2f-428a-bf2d-26d24a40096a.jpg"><br>Notice: grid tracks can optionally be separated by a gutter.</td><td>define the columns and rows, collectively known as the grid tracks, into flexible and adaptive ways</td>
>    </tr>
>    <tr><td>Page components are arranged within the columns<br><img src="https://user-images.githubusercontent.com/64577273/154851013-35e855cb-c5af-4d8f-9c38-e20eb9fdedc0.png"></td><td></td><td>determine the position of the grid items and are referred to by<ul><li>custom name</li><li>numerical index</li><li>negative numerical index which allows you to reference the opposite end of the grid</li></ul><img src="https://user-images.githubusercontent.com/64577273/154856367-3eb12a58-d25d-4be8-adfe-f5e14ce08e0f.jpg"><br>Notice: When using a numerical index, both the vertical and horizontal grid lines start at one.</td><td></td><td></td><td></td>
>    </tr>
></table>
>
>-Similar to flexbox
>* the grid container is the parent element.
>* The direct child elements are the grid items.
>* Grid can be used with two values, grid or inline-grid
><table>
>    <tr><th><code>display: grid;</code></th><th><code>display: inline-grid;</code></th>
>    </tr>
>    <tr><td colspan=2><img src="https://user-images.githubusercontent.com/64577273/154852768-3dd4e5ab-ae2c-448f-8f5f-4934cc9a1e91.jpg"></td>
>    </tr>
>    <tr><td>unless specified, the items will span the width of its container</td><td>the items will span the width of its content</td>
>    </tr>
>    <tr><td>the container will be displayed as block-level element and stacked on top of other block element<br><img src="https://user-images.githubusercontent.com/64577273/154852492-a32a15ce-ef70-4a48-984e-0e53a8b32eef.png"></td><td>the whole container will display inline next to other inline containers<br><img src="https://user-images.githubusercontent.com/64577273/154852542-b5997efa-cf70-4838-912a-f1a1974949b9.png"></td>
>    </tr>
></table>

grid-a pattern or structure made from horizontal and vertical lines crossing each other to form squares

break down-to separate something into smaller parts

consistent-always happening or behaving in a similar way

terminology-special words or expressions used in relation to a particular subject or activity

designate-indicate; show; specify

adjacent-very near

collectively-as a group; as a whole

adaptive-changing quickly to suit different conditions
## The explicit grid
>-`grid-template-columns` and `grid-template-rows` create an explicit grid with specific number of grid lines and tracks.  
>-their values expressed as a track list separated by a space to designate the number of tracks.  
![image](https://user-images.githubusercontent.com/64577273/155324012-7889d790-1c77-47df-bffa-90528dc9d94d.jpg)  
-These 2 properties can be defined using a variety of value types, like:
>
>fr|repeat()|mixed different units
>-|-|-
>represents a fraction of the available space in the grid container|repeat ([number of tracks], [size of tracks])|The repeat function can also be used to repeat part of the track listing
>the value of `1fr 1fr 1fr` split the grid into three equal columns/rows<br>![image](https://user-images.githubusercontent.com/64577273/155294518-3fcdf397-d7b5-41b8-81af-22776bf7c073.png)|the value of `repeat(3, 1fr)` includes 3 tracks with size of each track `1fr`<br>![image](https://user-images.githubusercontent.com/64577273/155296207-da054df4-2dba-4bce-b035-36d41baaf4cf.png)|the value of `50px repeat(2, 1fr)` makes first track 50px, while next two tracks are equally spaced.<br>![image](https://user-images.githubusercontent.com/64577273/155297920-eb9ebab4-a9ad-4cf4-a329-84f936cb7691.png)
>the value of `1fr 2fr 1fr` split the grid into three columns/rows while the second track will take up twice the amount of the first and third track<br>![image](https://user-images.githubusercontent.com/64577273/155294479-989e2e5b-3b25-46fb-9556-05e785ec8fd5.png)||
>
>-Gutters can also be added between grid items using the gap property.
><table>
>    <tr><th>gap</th><th>example</th>
>    </tr>
>    <tr><td><ul><li>One value adds the same amount of space between the rows and columns.</li><li>Two values sets the gutter for the rows then the columns.</li></td><td><img src="https://user-images.githubusercontent.com/64577273/155316415-9e384d6a-f99b-4170-b2b6-102f020312ac.png"></td>
>    </tr>
>    <tr><td>it can be used with any<ul><li>length unit</li><li>percentage</li><li>the calc function</li><li>but not the fr unit</li></ul></td><td><img src="https://user-images.githubusercontent.com/64577273/155299878-7f5b3b50-422e-48a4-a1e3-b30dcb82139a.png"></td>
>    </tr>
>    <tr><td>support longhand properties include <code>row-gap</code> and <code>column-gap</code></td><td><img src="https://user-images.githubusercontent.com/64577273/155301979-c99c13db-3075-4695-b056-a35ab33505b5.png"></td>
>    </tr>
>    <tr><td>When grid first shipped, in browsers the <code>column-gap</code>, <code>row-gap</code> and <code>gap</code> were prefixed with the <code>grid-</code> prefix as <code>grid-column-gap</code>, <code>grid-row-gap</code> and <code>grid-gap</code> respectively.<br>they have been updated to be used for both Flexbox and grid.</td><td><img src="https://user-images.githubusercontent.com/64577273/155320543-7e97ddce-384e-4d7d-9fcc-7677d5c05383.png"></td>
>    </tr>
></table>
>
>-All of these properties are declared in the grid container
>```css
>.grid-container {
>    display: grid;
>    grid-template-columns: 100px 100px 100px;
>    grid-template-rows: 100px 100px;
>    gap: 10px 20px;
>}
>```
>-experiment with [this codepen example](https://codepen.io/imahdio/pen/qBVKKNO):
>1. add `display: grid;` into grid-container to apply the grid properties
>2. add `grid-template-columns: 100px 100px 100px;` into grid-container to add three columns set to 100 pixels in width.
>3. add `grid-template-rows: 100px 100px;` into grid-container to add two rows set to 100 pixels each.
>4. update columns with `grid-template-columns: repeat(3, 100px);`  
Notice: The grid should look the same since we're only changing the way we set the value.  
Notice: To add or remove columns, just change the first value of `repeat` function.
>5. update columns with `grid-template-columns: repeat(3, 1fr);` to split the space into three equal and flexible parts.  
Notice: resize the view port to see how it scales.
>6. update columns with `grid-template-columns: 100px repeat(2, 1fr);` so the first column has a fixed size of 100 pixels, then the remaining space could be split evenly into two columns.
>7. update rows with `grid-template-rows: 100px;`. now the second row is the same height of its content because we've only declared one explicit row.
>
>-Any items that are within the grid container but are placed outside of the explicit grid will be placed into an implicit grid and will be sized according to those explicit rules which we'll discuss in the next lesson.

express-to show a feeling, opinion, or fact; convey (a thought or feeling) in words or by gestures and conduct

fraction-a number that results from dividing one whole number by another
## The implicit grid
>explicit grid|implicit grid
>-|-
>defines a fixed number of tracks in a grid layout using<ul><li>`grid-template-rows`</li><li>`grid-template-columns`</li></ul>![explicit-grid](https://user-images.githubusercontent.com/64577273/155834651-3dd8664a-5434-481f-9373-2339d7ddba6a.jpg)|defines the size of grid tracks in a grid layout using<ul><li>`grid-auto-rows`</li><li>`grid-auto-columns`</li></ul>![image](https://user-images.githubusercontent.com/64577273/155837916-eb5afd63-f295-4a84-914d-d2d5ee53840b.png)
>use it if<ul><li>YOU know how many items there are to display</li><li>YOU know the minimum amount of grid items you could use an explicit and implicit grid together</li></ul>|<ul><li>use it if<ul><li>YOU don't know how many items your grid needs to display</li><li>YOU know the minimum amount of grid items, you could use an explicit and implicit grid together</li></ul></li><li>grid container will generate it automatically once<ul><li>there are more grid items than the number of explicit tracks</li><li>no explicit grid has been defined</li></ul></li></ul>
>if don't have enough items to fill that grid, it will still take up the space that has been defined<br>![image](https://user-images.githubusercontent.com/64577273/155833861-8fabffec-be9c-4d95-a57f-343ff6df2f5c.png)|can be used in dynamic content like a news feed, search results or a list of comments
>based my test and tries,<br>they be defined explicitly one by one|based my test and tries,<br>they be defined for repetitive patterns of implicit grids
>
>-Let's continue with [the pen used in the previous lesson](https://codepen.io/imahdio/pen/zYPJpQL)
>1. We had six grid items but only three columns and one row defined in the explicit grid. That means the last three items are placed within the implicit grid.
>2. Items four to six in this example are the same width of the columns defined in the explicit grid. But since only one explicit row has been defined, the items in the implicit row will adjust to the height of the content contained within.
>3. add `grid-auto-rows: 200px;` in grid-container to set the height for implicit grids.
>4. hide the last three items in the HTML. Since there are now no extra items outside of the explicit grid, there are no empty tracks either because the implicit grid will only apply when there are items placed outside of the explicit grid.
>5. put those items back in the HTML
>6. add `grid-auto-columns: 50px;` in grid-container to add a size for the implicit columns. Since the items wrap automatically, we'll have to use one of the grid placement properties, to create an implicit fourth column. 

ahead of-in front of

anticipate-regard as probable; expect or predict

anticipate-to imagine or expect that something will happen
## Grid placement properties
>-So far, we've been looking at properties that are applied to the grid-container. These properties define the structure of the grid.  
![image](https://user-images.githubusercontent.com/64577273/156116769-ab1b72ad-8ed3-4f60-a4a2-58df209eaf60.png)  
-Position-based properties must be applied to the grid items to determine their placement within the grid. The properties used for placing grid items are
><table>
>    <tr><th>grid-column</th><th>grid-row</th>
>    </tr>
>    <tr><td>shorthand for<ul><li>grid-column-start</li><li>grid-column-end</li></ul></td><td>shorthand for<ul><li>grid-row-start</li><li>grid-row-end</li></ul></td>
>    </tr>
>    <tr><td colspan=2><ul><li>A number value is used to specify the the start and end of the grid-item's position based on the grid lines.</li><li>When using the shorthand property, the value start and end value must be separated with a forward slash.</li></ul></td>
>    </tr>
>    <tr><td>Grid items, by default, start on line one and span the size of one grid cell. To change them, use:<ul><li><code>grid-column-start</code> to change the start position</li><li><code>grid-column-end</code> to make the grid items span more than one column</li></ul><img src="https://user-images.githubusercontent.com/64577273/156119877-58022c96-8ecb-47ef-834e-f6f2c01e91f5.png"></td><td>for the positioning of the grid items within rows, use:<ul><li><code>grid-row-start</code></li><li><code>grid-row-end</code></li></ul><img src="https://user-images.githubusercontent.com/64577273/156121083-1ad0833f-068d-4872-b836-74845fb8507a.png"></td>
>    </tr>
></table>
>
>-in previous lesson, We were able to see how grid items were displayed in the implicit rows. in this lesson, we'll have to use `grid-column` to specifically place an item into the implicit grid. Let's continue with [the pen used in the previous lesson](https://codepen.io/imahdio/pen/GROwRXy):  
>1. add `example` class to 3th grid item in html to change its default placement.
>2. add `grid-column: 4;` to example class to star it on line 4 and automatically end on line 5.  
Notcie: This column is now showing with a width of 50 pixels which is what we declared at `grid-auto-columns`. This property sets the width of the columns for the implicit grid.
>3. update implicit column with `grid-column: 4 / 6;` to span across two implicit columns.
>
>-explore more of what grid has to offer on [this MDN resource](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Grids).
# Project: Grid columns and Firefox Grid Inspector
>-aa

toggle-to switch a feature on a computer on and off by pressing the same button or key

overlay grid-
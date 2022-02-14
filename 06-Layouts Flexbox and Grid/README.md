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
>-aa

flush-on the same level so that no part is higher or lower or sticks out more than another

stick out-to go past (beyond) the surface or edge of something
## Project: Flexbox alignment
>-aa
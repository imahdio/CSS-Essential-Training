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
>-create various page layouts with aligning and sizing elements by
>* historically, float and sometimes displaying position
>* the flexible box layout or Flexbox for short with flexible layouts over all
>![image](https://user-images.githubusercontent.com/64577273/153207028-9d8acddd-e8cd-4536-8aa4-54883d359e3c.png)
>
>-make a basic layout with
>
>float<br>as legacy technique|flexbox
>-|-
>require additional hacks to make each item<ul><li>the same height as its content</li><li>equal height columns</li></ul>|the height of each flex item automatically adjusts to be the same height as the longest item without adding any additional CSS<br><img src="https://user-images.githubusercontent.com/64577273/153255971-110682d0-214b-42ac-a068-a457760d73fd.png">
>
>-to use Flexbox, the flex-container must defined with one of these two values:
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
>-The two axes of flexbox includes
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
>-aa

substitute-a person or thing acting or serving in place of another

shrink-become or make smaller in size or amount

feel like something-to seem to be something
## Flexible sizing
>-aa

voice over-words that describe or comment on a film, advertisement, or video, which are spoken by a person who is not seen

link value-
## Flexbox exercise
>-aa

## Flexbox: Alignment
>-aa

flush-on the same level so that no part is higher or lower or sticks out more than another

stick out-to go past (beyond) the surface or edge of something
## Project: Flexbox alignment
>-aa
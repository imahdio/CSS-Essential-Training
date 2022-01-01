# 02-Core Concepts
## CSS specifications and the W3C
>-The World Wide Web Consortium, or W3C for short develop web standards and guidelines including the technical specifications for CSS.  
-W3C guidelines is a little intimidating, because it includes a lot of jargon and quite extensive terms for newbies but since the W3C is responsible for establishing these rules, you'll probably end up looking at it at some point.  
-The first two versions of CSS, Level 1 and Level 2, published all the specification as one whole document. After Level 2, the W3C decided to split the specification into independent modules to allow for faster incremental changes. Each module can level up independently. [*therefore CSS does n't have versions in the traditional sense; instead it has levels.*](https://dev.to/afif/when-we-will-have-css4-o9o)  
-[on W3C table of CSS specifications](https://www.w3.org/Style/CSS/current-work) You may see some marked as Level 3 if it's an update from CSS2. New modules such as flexbox start out at Level 1. There are others marked at Level 4. So these levels have no relation to the version of CSS. So while CSS3 basically refers to any updates after CSS Level 2, there's really no need to make the distinction. It's all just CSS. [check here for more info](https://dev.to/afif/when-we-will-have-css4-o9o)  
-All of the past, current, and working drafts are published on the W3C website. Status codes are included to indicate what phase the particular module is at. [status code reference](https://www.w3.org/Style/CSS/current-work)  
><table>
><tr><td><img src="https://user-images.githubusercontent.com/64577273/147824363-2c93a478-70f3-4743-a6b3-8df8baef41b5.png"></td><th>First Public Working Draft</th><td rowspan=2>they're still experimental and may not be supported by all browsers and are subject to be changed or even removed altogether. </td>
></tr>
><tr><td><img src="https://user-images.githubusercontent.com/64577273/147824456-9558d0c8-a455-476d-ac1e-c6edb464e08b.png"></td><th>Working Draft</th>
></tr>
><tr><td><img src="https://user-images.githubusercontent.com/64577273/147824551-0f8db5cc-b5c4-46c4-b24f-a97291c32105.png"></td><th>Candidate Recommendation</th><td rowspan=2>they're requires some time for feedback and approval. Standards at this phase are usually okay to start implementing but just be aware that they're still technically a work-in-progress.</td>
></tr>
><tr><td><img src="https://user-images.githubusercontent.com/64577273/147824603-4db98348-47e1-4c0e-8cc9-74977a75c8f5.png"></td><th>Proposed Recommendation</th>
></tr>
><tr><td><img src="https://user-images.githubusercontent.com/64577273/147824642-b988a454-32c6-4208-83ea-d1479e0453ea.png"></td><th>Recommendation</th><td>It's good to go, and are the current standards for the latest browsers</td>
></tr>
><tr><td><img src="https://user-images.githubusercontent.com/64577273/147824696-a7d92b6e-d318-4876-b8e3-d3f3bb200db4.png"></td><th>Superseded Recommendation</th><td>It is a spec that has been replaced by a newer version</td>
></tr>
></table>
>-in this course , you learn core concepts for writing CSS so it's good to have a few go-to resources. I recommend the Mozilla Developer Network's CSS Guide.

member organizations-*based on my study friend opinion and me* participated organzations

public-*based on my study friend opinion and me* volunteers all over the globe

turn out-to happen in a particular way or to have a particular result, especially an unexpected one

intimidating-making you feel frightened or nervous

jargon-words and phrases used by particular groups of people, esp. in their work, that are not generally understood

extensive-covering or affecting a large area

end up-to reach or come to a place, condition, or situation that was not planned or expected

distinction-a difference between two similar things

incremental-happening gradually, in a series of small amounts

independently-in a way that is free from outside control or influence

In the traditional sense-It isn't quite/technically what you're calling it, but it serves the same purpose or it's similar. [Check full descriptions in here](https://hinative.com/en-US/questions/18870237)

start out-to begin to do something in business or a job, or to begin your working life in a particular way

go to-the best person, thing, or place for a particular purpose or need

proposed-suggested as a possible plan or action for people to consider

set to-to start doing something in a determined or enthusiastic way

formalize-to make something official , give (something) legal or formal status

supersede-to replace something, especially something older or more old-fashioned

experimental-relating to tests, especially scientific ones
## CSS syntax and terminology
>-CSS Syntax
>```css
>img {
>    width: 300px;
>}
>```
>image|descriptions
>-|-
>![image](https://user-images.githubusercontent.com/64577273/147845179-a977b901-1c15-496d-a839-ad04df594875.png)|`img` is a selector, and selectors are used to determine which html element to apply the styles to.
>![image](https://user-images.githubusercontent.com/64577273/147845238-29a108a0-4c4d-4ab0-b1ef-12b3aca1bdc1.png)|This whole snippet is called a declaration block and may include one or more style rules wrapped in curly braces to contain the styles to the specific selector.
>![image](https://user-images.githubusercontent.com/64577273/147845224-fcbdfdd2-ecdf-4421-bcf6-96d3e83f46f2.png)|Declarations are the style rules and are written using a property-value pair, separated with a colon and ending with a semi-colon to indicate that the rule is complete.
>![image](https://user-images.githubusercontent.com/64577273/147845273-9d27b66e-2e65-4c59-b4f4-ae3e0a7c1142.png)|`width` is a property which refers to the style characteristic to be applied to the element. And values are specific to that property and vary depending on the property type.
>
>-Many CSS properties can be written using a shorthand or longhand syntax. For example, a property we'll be using frequently is padding, which is shorthand for four other padding properties.  
>```css
>/* longhand */
>padding-top: 10px;
>padding-right: 5px;
>padding-bottom: 10px;
>padding-left: 5px;
>
>/* shorthand */
>padding: 10px 5px;
>```
>-The majority of CSS is selecting elements and applying styles to them. But we can also add comments to the code.  
-The syntax for comments start with a slash and an asterisk and closes in the opposite order.
>```css
>/* Write your comment between here. */
>
>/* This is valid.
>--------------------------- */
>
>/*
>* Multi-line comments
>* are also valid.
>*/
>
>/**********************
>Comments styles can be personal.
>***********************/
>```
>
>the goals|syntax
>-|-
>leave notes for yourself and others|![image](https://user-images.githubusercontent.com/64577273/147845822-9d7f3033-ef51-41e6-82ec-3cab6fcdc32f.png)
>Organize code blocks|![image](https://user-images.githubusercontent.com/64577273/147845856-9fdc1d1c-8505-462a-a76c-d1b26a78499a.png)
>comment out code to hide it temporarily<br>**This is often used for debugging by temporarily removing different declarations to test an experiment without actually deleting the code.**|![image](https://user-images.githubusercontent.com/64577273/147845864-9f41a19a-354e-4686-8bda-fbd8ec54547b.png)
>
>-When writing CSS, there will be times when adding or removing a space will be part of the syntax requirement. Other times, white space and tab spacing are used just for formatting and readability.
>
>it's not required to include any spaces within your declaration blocks|it is convention to use white space for readability
>-|-
>![image](https://user-images.githubusercontent.com/64577273/147846038-b162f2cd-1ec0-4db1-a3af-c97ca2baabb3.png)|![image](https://user-images.githubusercontent.com/64577273/147846048-d969a476-0fcb-4c5e-9fca-232b4c29ba5d.png)
>
>-[codeguide.co](https://codeguide.co/) is one of the many code style guides you can refer to.

syntax-the structure of statements or elements in a computer language

terminology-special words or expressions used in relation to a particular subject or activity

countless-very many

debate-to discuss a subject in a formal way,to try to make a decision about something

consistent-always behaving or happening in a similar, especially positive way

tend-to be likely to behave in a particular way or have a particular characteristic
## CSS values and units
>-this lesson will provide an overview of the various data types, the values and units.
><table>
>    <tr><th>Some numeric data types can be used with:</th><th>syntax</th>
>    </tr>
>    <tr><td>whole numbers only</td><td rowspan=3><img src="https://user-images.githubusercontent.com/64577273/147858626-0a8ce5e4-21a8-4066-b701-5f63a19802ea.png"><br><img src="https://user-images.githubusercontent.com/64577273/147858682-4b45361c-b188-469d-b2f6-313ce73b9be3.png"><br><img src="https://user-images.githubusercontent.com/64577273/147858674-e6f2c2a4-c170-4d13-b242-3b6b62226888.png"></td>
>    </tr>
>    <tr><td>Some can be used with decimal points</td>
>    </tr>
>    <tr><td>Others specify dimension and require a unit attached to it, such as degrees or milliseconds</td>
>    </tr>
></table>
>
>-The `<length>` data type is used to specify sizing with two types of units: absolute and relative.  
><table>
>    <tr><th>Absolute <code>&#60;length></code> values</th><th>Relative <code>&#60;length></code> values</th>
>    </tr>
>    <tr><td><ul><li>Fixed unit, always the same size</li><li>Not affected by values in related elemnts</li><li>Example: px, cm, mm, pt</li></ul></td><td><ul><li>Relational sizing, not fixed</li><li>dependent upon values declared in parent and ancestor elements</li><li>Example: em, rem, vw, vh</li></ul>
>    </td>
>    </tr>  
></table>
>
>-Some numeric values don't require a unit.
>unitless values|code example
>-|-
>Many properties which use number values can be declared with just the number only if the value is 0|![image](https://user-images.githubusercontent.com/64577273/147857848-521a9c85-6954-44bd-a553-25fcf31dbafd.png)
>There are also some properties which use keywords, so units aren't required|![image](https://user-images.githubusercontent.com/64577273/147857863-e9c93584-29b2-4fa0-9f37-4e88babc1282.png)
>
>-there are many functions in CSS that can be used as property values. the syntax always includes the function name and parenthesis, for example:
>for example|syntax
>-|-
>the `transform` property uses the `rotate` function defined by degrees|![image](https://user-images.githubusercontent.com/64577273/147859029-551c3074-dbeb-4c3b-af97-9ebd9835ebd8.png)
>The `calc` function performs calculations with a mixture of units|![image](https://user-images.githubusercontent.com/64577273/147859038-2842e59f-3f89-4fb8-a27c-2c3922bb9d42.png)
>the `background-image` uses an image file name as its value.|![image](https://user-images.githubusercontent.com/64577273/147858007-4115f5c5-2161-4bbf-84eb-72d53e54e74a.png)
>
>-When reading CSS documentation, you may see references to a property's initial value. **This refers to the default style, the way the element is displayed before adding any CSS.** If you want to use the default styles as is, you don't have to declare this property with the initial value.  
![image](https://user-images.githubusercontent.com/64577273/147858217-7682bb6a-9df2-4330-a58e-743ab596bd7d.png)  
>-if you want to do a deep dive into all the specifics of CSS values and units, I would recommend this [Mozilla developer network article](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units).

css data types- data types are denoted by a keyword placed between the inequality signs "<" and ">"

interchangeable-(of two things) capable of being put or used in the place of each other

dependent upon-dependent on

ancestor-a person related to you who lived a long time ago

ancestor element-an element that contains (at any level) other elements is an ancestor of the elements that it contains. [check here for more info](https://www.littlewebhut.com/css/info_element_relationships/)

descendant-a person who is related to you and who lives after you, such as your child or grandchild

descendant element-an element that is contained (at any level) within another element is a descendant of the element that contains it. [check here for more info](https://www.littlewebhut.com/css/info_element_relationships/)

syntax-the structure of statements or elements in a computer language

in a nutshell-very briefly, giving only the main points

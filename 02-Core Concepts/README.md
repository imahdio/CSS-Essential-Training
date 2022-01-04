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
## The color and property values
>-the `color` property can be used with many different types of values:
>- use keyword values to define colors
![image](https://user-images.githubusercontent.com/64577273/147875804-443e0cf6-1b31-4d36-8ac7-f01968eca4c0.png)
>
>Notice: [colours.neilorangepeel.com](https://colours.neilorangepeel.com/) is a great visual reference and lists all of the available keywords, including the corresponding color value type.
>- either use  
>    1. RGB values to define colors according to it's red, green, and blue components using a **hexadecimal value** or a **functional value**
>    2. HSL values which defines a color by its hue, saturation, and lightness and also includes an optional alpha component.
>
>RGB values<br>using a hexadecimal value|RGB values<br>using a functional value|HSL values <br> another functional value
>-|-|-
>they are prefixed with a number sign # followed by six characters using a combination of numbers from zero to nine and the letters A to F|The RGB function is defined using three comma-separated numbers between 0-255 or 0%-100%|it defines a color by its hue, saturation, and lightness ![image](https://user-images.githubusercontent.com/64577273/147877886-597bed21-fc2c-49e1-b010-3509e8b1a02a.png) <br> ![image](https://user-images.githubusercontent.com/64577273/147877872-6fb357fa-6ec6-49dd-aa17-9ac75500dcef.png)
>The first two values represent the red, followed by the green and blue values.<br>![image](https://user-images.githubusercontent.com/64577273/147876298-bc04341e-cf8d-4229-a4ed-7d6a76b7c3bc.png)|to set the red, green, and blue color channels.<br>![image](https://user-images.githubusercontent.com/64577273/147884132-9fd30219-dfb9-4dec-9699-63c397b720ee.png)<br>![image](https://user-images.githubusercontent.com/64577273/147876756-e90c6591-8b1c-4f4d-a515-d17be728c5a8.png)|● [The Hue is specified as an angle within the color wheel, relative to red.](https://upload.wikimedia.org/wikipedia/commons/f/f7/Hsv-hues-cf-lch-hues.png) So red equals zero degrees or 360 degrees and the other colors are spread around the circle. Green equals 120 degrees and so on. <br>● Saturation is the second value, and is represented with a percentage. 100% is full saturation and 0% is a shade of gray.<br>● Lightness is the third value and is also represented as a percentage. 100% lightness is white, 0% lightness is black, and 50% lightness is normal.<br>[compare HSL parameters in 1 diagram](https://vanseodesign.com/web-design/hue-saturation-and-lightness/)
>-|use `rgba()` and a fourth value (alpha channel) to change the opacity of the color. Zero or 0% is no opacity, one or 100% is full opacity. [check it practically at all over down side of this article](https://www.w3schools.com/html/html_colors_rgb.asp)<br>![image](https://user-images.githubusercontent.com/64577273/147877001-34cf731a-cc18-443e-b691-aea579a8f57f.png)|also includes an optional alpha component. The Alpha Channel can be represented as a decimal or a percentage.<br>![image](https://user-images.githubusercontent.com/64577273/147878074-cd6ffda2-7702-4b0d-9dc8-5dc98a9d262b.png)
>The hex value can also be abbreviated if the RGB pairs or all the values are the same. [check it practically](https://www.rapidtables.com/web/color/RGB_Color.html)<br>![image](https://user-images.githubusercontent.com/64577273/147876626-7e7486b0-4824-41d2-8279-f4f10976e1aa.png)||
>The letters in the hexadecimal notation are case-insensitive.<br>![image](https://user-images.githubusercontent.com/64577273/147876354-c6a6ee84-f422-4315-a184-e93ccf517c4b.png)||
>
>-[This tool on css-tricks.com](https://css-tricks.com/examples/HSLaExplorer/) is a good one for both HSL and RGB colors.  
>-[Randoma11y.com](https://www.randoma11y.com/) is great for creating color combinations that provide high contrast for those with color blindness.  
>-[coolors.co generates projects' color palette.](https://coolors.co/generate) You can press the space bar to generate new color palettes. You can click on the colors that you want to use to lock it, and press the space bar to get more colors.

quite often-Used for things that happen less frequently than "very often", but more frequently than "sometimes" or "occasionally"

lace-a fine cloth made with patterns of many very small holes

old lace-a very pale yellowish orange like the color of an old lace tablecloth

corresponding-analogous or equivalent in character, form, or function; comparable

number sign-the sign # is known variously as the number sign, hash, or pound sign, used to introduce a number (as in question #2)

hexadecimal-often shortened to "hex", is a numeral system made up of 16 symbols. The standard numeral system is called decimal (base 10) and uses ten symbols: 0,1,2,3,4,5,6,7,8,9. Hexadecimal uses the decimal numbers and six extra symbols.(A, B, C, D, E and F)

opacity-the quality of lacking transparency

relative to-in comparison with

ally-someone who helps and supports someone else

palette-the range of colours used in the decoration of a house, etc.

textile-it refers to any material made of interlacing fibres

upcoming-about to happen; forthcoming
## Type and universal selectors
>-CSS uses different types of selectors to create pattern matching rules to determine which element to apply the style to.  
![image](https://user-images.githubusercontent.com/64577273/147886355-33c26665-42f9-4ae4-95bb-295b63a0e0a6.png)
>-Type selectors are the most basic kind of selector. They match to HTML elements by using the element name. For example, to apply a style to the h1 tags, h1 is the selector.  
![image](https://user-images.githubusercontent.com/64577273/147886492-4cf6c526-a783-4a32-8146-3cd75bc40121.png)  
>-The universal selector selects every single element in the whole document. The syntax is expressed as a single asterisk.  
![image](https://user-images.githubusercontent.com/64577273/147886538-9aa746fe-a372-414b-8171-936344b86878.png)  
>-[experiment both above selectores in here practically](https://codepen.io/imahdio/pen/wvrmNOm?editors=1100)

best practice-a working method, or set of working methods, that is officially accepted as being the best to use in a particular business or industry

sparingly-in an economical or limited way,in a restricted or infrequent manner; in small quantities

too general-not specific enough
## Class and ID selectors
>-class and ID are two attributes that can be used to attach extra information to any HTML element.
>
>class selector|ID selector
>-|-
>add the class attribute to the opening HTML tag of the element you want to apply the style to. its value is defined by you.<br>![image](https://user-images.githubusercontent.com/64577273/147904753-6a161132-7c52-497a-942b-b66abacc7ecb.png)|add the ID attribute to the HTML element with a custom value.<br>![image](https://user-images.githubusercontent.com/64577273/147906271-8acbf88c-11ff-4215-bb5f-4afff2a3b6ca.png)
>The value of the class becomes the selector and must begin with a leading period.<br>![image](https://user-images.githubusercontent.com/64577273/147904902-6ffc26b8-7b9b-4eed-9f64-df50a1c9f641.png)|the CSS selector for IDs has a different syntax. ID selectors begin with a number sign (#) symbol.<br>![image](https://user-images.githubusercontent.com/64577273/147906427-c411042c-7414-4410-ae3b-6110cd65c2fd.png)
>Class selectors can be reused throughout the document. Add the class to any element to apply the style.<br>![image](https://user-images.githubusercontent.com/64577273/147905302-1fd476dd-67c5-4d01-85fe-37b7f9b71b13.png)|there is a good convention that ID selectors are not reusable and highly recommend only be used once per page.<br>![image](https://user-images.githubusercontent.com/64577273/147906510-4d201e93-0426-464a-ac44-df7ed8f71933.png)
>You can also use more than one class in the same element by adding another class name to the value. The values must be separated with a space and contained within the quotes.<br>![image](https://user-images.githubusercontent.com/64577273/147905536-37605ca9-c13b-40f4-a8a6-ecf354ae6bd8.png)|`id` is a global attribute that is similar to `class` but we’re only allowed to use one specific id in each HTML element. <br>[for more example check here](https://github.com/imahdio/HTML-Essential-Training/blob/ddf4faedd53a8157ce1037e28706f01821649c7e/03-Understanding%20the%20Power%20of%20HTML/README.md#html-attributes)
>With multiple classes, you can apply styles to each class independent of each other or apply a style only when all of the classes are included.<br>![image](https://user-images.githubusercontent.com/64577273/147905811-d8231f80-5e07-4594-b42b-d555681c7e4e.png)|
>
>-IDs can be used for in-page linking by using the ID value in the link's href attribute. When you click the link it will automatically scroll down or up to the matching element on the page.  
![image](https://user-images.githubusercontent.com/64577273/147907489-b3ad864b-4c7c-4d9f-9128-a5098c7dbbe4.png)
Notice: You can use the same ID value for both in-page linking and for CSS but, for organization, it's recommended to keep these functions separate.  
Notice: Some prefer not to use IDs at all for CSS and reserve it just for in-page linking.  
-use the following naming conventions When choosing a class or ID name:
>* don't use spaces. If you want to choose a certain value that is more than one word use an underscore or dash to separate the words.  
![image](https://user-images.githubusercontent.com/64577273/147907843-9c2ee088-118d-42ef-910b-4cb3b0627f55.png)
>* use meaningful and descriptive names that describe the purpose of the style, that can make it easier to read and understand why it's being used.  
![image](https://user-images.githubusercontent.com/64577273/147908021-923428df-66cb-4e29-a33f-0208ff7f8644.png)
>* use easily undrstood abbreviations which fairly common or pretty self-explanatory  
![image](https://user-images.githubusercontent.com/64577273/147908147-1559e254-8c91-4a6d-b708-17e11f40b5c5.png)

leading-in the first position

hyphen-the mark (-) used in writing to join two words together, or between the syllables of a word when it is divided at the end of a line of text

underscore-to underline ;the character (_) on a computer keyboard, used to draw a line under a letter or word, and also used in file names where a space is not allowed

corresponding-similar to, connected with

explanatory-serving to explain something; giving an explanation about something

get good-or GIT GUD , improve yourself
## Class and ID selector exercise 
>-Using the previous code pen exercise, [let's practice using class and ID selectors](https://codepen.io/imahdio/pen/dyVmxQL?editors=1100):
>1. make a change to just the first h2 element by adding a class attribute
><table>
>    <tr><th>html</th><th>css</th><th>result</th>
>    </tr>
>    <tr><td>
>    <pre><code>...
>&lt;h2 class="example">Sub-heading&lt;/h2>
>...</code></pre><td><pre><code>...
>.example {
>  color: orange;
>}</code></pre><td><img src="https://user-images.githubusercontent.com/64577273/147919829-e0c86c8b-bbb6-4519-a8e3-f777489a6d15.png">
></table>
>
>2. Since classes can be reused and applied to any HTML element, Let's put it in the `h1`.
><table>
>    <tr><th>html</th><th>css</th><th>result</th>
>    </tr>
>    <tr><td>
>    <pre><code>
>&lt;h1 class="example">Heading&lt;/h1>
>&lt;h2 class="example">Sub-heading&lt;/h2>
>...</code></pre><td><pre><code>...
>.example {
>  color: orange;
>}</code></pre><td><img src="https://user-images.githubusercontent.com/64577273/147920410-6d2f3684-e14c-438a-ae0c-ed5764a13230.png">
></table>
>
>3. add example2 class in the `h2` element and add another CSS style using the example2 selector.
><table>
>    <tr><th>html</th><th>css</th><th>result</th>
>    </tr>
>    <tr><td>
>    <pre><code>
>&lt;h1 class="example">Heading&lt;/h1>
>&lt;h2 class="example example2">Sub-heading&lt;/h2>
>...</code></pre><td><pre><code>...
>.example2 {
>  background: black;
>}</code></pre><td><img src="https://user-images.githubusercontent.com/64577273/147921306-801daffc-7191-4b64-820e-f2d57a22e404.png">
></table>
>
>4. apply a style to both classes. So it'll only apply if both classes are present.
><table>
>    <tr><th>html</th><th>css</th><th>result</th>
>    </tr>
>    <tr><td>
>    <pre><code>
>&lt;h1 class="example">Heading&lt;/h1>
>&lt;h2 class="example example2">Sub-heading&lt;/h2>
>...</code></pre><td><pre><code>...
>.example.example2 {
>  font-size: 50px;
>}</code></pre><td><img src="https://user-images.githubusercontent.com/64577273/147922208-9318cbd0-9bad-4e7a-8dfe-341b29357e1f.png">
></table>
>
>5. add example ID to the `h1`. let's use the same name with its class value.
><table>
>    <tr><th>html</th><th>css</th><th>result</th>
>    </tr>
>    <tr><td>
>   <pre><code>
>&lt;h1 id="example" class="example">Heading&lt;/h1>
>&lt;h2 class="example example2">Sub-heading&lt;/h2>
>...</code></pre><td><pre><code>...
>#example {
>  font-size: 100px;
>}</code></pre><td><img src="https://user-images.githubusercontent.com/64577273/147922943-7419758a-147d-4370-8c2a-656ba77c6e6e.png">
></table>
>
>Notice: So while it's possible to use the same name for classes and IDs, it might get a bit confusing so it's probably better to give them different names.  
>-[check full code example in here](https://codepen.io/imahdio/pen/dyVmxQL)

even though-despite the fact that
## Descendant selectors
>-Document object model (DOM) represents the relationship between HTML elements.  
>1. The first level creates a parent child relationship
>2. anything nested further is referred to as an ancestor descendant relationship.
>3. The relationship between elements nested within the same parent are referred to as sibling elements.  
![image](https://user-images.githubusercontent.com/64577273/147952160-88d8c5bf-5bee-4a82-8c05-5ad5ceea14e8.png)  
>
>-Descendant selectors are used to apply styles specifically to elements nested within other elements. To select a descendant element, use a space between the selectors to denote the nested relationship.
>
>2 selectores|more than 2 selectores to match two descendant elements|mix different selector types or even skip levels
>-|-|-
>The selector on the left is the ancestor element. The selector on the right is the descendant element.<br>![image](https://user-images.githubusercontent.com/64577273/147975861-abea93f7-f12d-42e9-af6e-ee1795fc300f.png)|In this example, `section p a` will select a link nested inside of a paragraph inside of a `section` element. the outside links will not be affected.<br>![image](https://user-images.githubusercontent.com/64577273/147976501-7b46cd57-2789-4eb9-9c84-a57e026e0c1e.png)|You're not required to follow the exact nested path of the HTML structure to select a descendant element.<br>![image](https://user-images.githubusercontent.com/64577273/147976858-1a81d8d3-fc27-4118-b448-aa5c48bdfd10.png)
>
>-[In this example](https://codepen.io/christinatruong/pen/KEyzNo?editors=1100), we'll look at different ways to select the links depending where they are in the HTML.  
>Notice: control forward slash <img src="https://user-images.githubusercontent.com/64577273/148019766-3887ed26-c958-4dbc-add5-bb14e6621a5d.jpg"> is keyboard shortcut for comment or uncomment  to the selected lines of code.
>1. uncomment the color value in the `a` type selector. This will apply to all the links anywhere in the document.
>2. `section a` is a descendant selector and we'll select only links nested within a section element. this selector skip levels and match to the link within the paragraph which within the section element.
>3. `.container a` use different types of selectors together. this is similar to `section a`, except it uses the class name instead of the element name.
>4. `section p a` descendant selectors go more than two levels to be even more specific. It select links contained within a paragraph within a section element. but it not change color and still showing the color declared in `.container a` because of specificity concept which refers to how to determine which styles will take precedence when the selectors conflict.
>5. `.container p a` select the link in the paragraph whithin container class.
><table>
>    <tr><th>html</th><th>css</th><th>results</th>
>    </tr>
>    <tr><td rowspan=6><pre><code>
>&lt;section class="container">
>	&lt;p>&lt;a href="#">Link inside a paragraph.&lt;/a>&lt;/p>
>	&lt;a href="#">Link outside of a paragraph.&lt;/a>
>&lt;/section>

>&lt;a href="#">Link outside of section.&lt;/a>
></code></pre>
>    </tr>
>    <tr><td><pre><code>
>a {
>  color: black;
>}
></code></pre></td><td><img src="https://user-images.githubusercontent.com/64577273/148023590-902eeff2-5ec1-4c91-96d7-0ab3e9819219.png"></td>
>    </tr>
>    <tr><td><pre><code>
>section a {
>  color: green;
>}
></code></pre></td><td><img src="https://user-images.githubusercontent.com/64577273/148023663-8aca6936-d157-4379-9c04-fe4bea74ebb2.png"></td>
>    </tr>
>    <tr><td><pre><code>
>.container a {
>  color: orange;
>}
></code></pre></td><td><img src="https://user-images.githubusercontent.com/64577273/148023773-860f6b24-bc6e-4ae0-be26-28be2b16a7ea.png"></td>
>    </tr>
>    <tr><td><pre><code>
>section p a {
>  color: pink;
>}
></code></pre></td><td>because of specificity concept it doesn't take effect unless comment out the <code>.container a</code>in perivous step.
>    </tr>
>    <tr><td><pre><code>
>.container p a {
>  color: green;
>}
></code></pre></td><td><img src="https://user-images.githubusercontent.com/64577273/148023873-56caa320-4755-4b8b-b6ac-e83c77291fd3.png"></td>
>    </tr>
></table>
>
>-With descendant selectors, you can go as many levels as you need, but it's a good rule of thumb to stick to a maximum of two or three levels to avoid making your selectors more specific than it needs to be

ancestor-a person related to you who lived a long time ago

ancestor element-an element that contains (at any level) other elements is an ancestor of the elements that it contains. [check here for more info](https://www.littlewebhut.com/css/info_element_relationships/)

descendant-a person who is related to you and who lives after you, such as your child or grandchild

descendant element-an element that is contained (at any level) within another element is a descendant of the element that contains it. [check here for more info](https://www.littlewebhut.com/css/info_element_relationships/)

mesh with something-to fit with something

specificity-the quality of being specific (= clear and exact)

precedent-an action or event in the past that is used as an example or reason for a present action or event

precedence-priority in importance, order, or rank

upcoming-about to happen; forthcoming

determine-to control or influence something directly, or to decide what will happen

rule of thumb-a broadly accurate guide or principle, based on practice rather than theory


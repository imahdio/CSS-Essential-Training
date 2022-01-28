# 04-Typography
## Typography for the web
>-typography is the art of arranging type for readability and to engage and communicate with the reader  
-Typeface, often referred to as font or font family, is a set of fonts designed with common characteristics and composed of glyphs   
-When choosing a typeface, it must be
>* easy to read
>* conveys certain feelings or a tone appropriate for the content  
>
>-Times New Roman is often used for legal documents. they're thought to convey a traditional formality  
-Comic Sans was designed to be a casual font. It's childlike with fun appearance  
-<a name="five-categories-of-typefaces"></a>**Here are five categories of typefaces**
><table>
>    <tr><td>script</td><td>decorative</td><td>monospace</td><td>serif</td><td>sans-serif</td>
>    </tr>
>    <tr><td colspan=3>more specific usages, and are used sparingly</td><td colspan=2>are used the most often</td>
>    </tr>
>    <tr><td>have a hand-lettered look and tend to be harder to read and convey an elegant feel</td><td>ornamental and tend to have big personalities</td><td>each character uses the same amount of horizontal space whether it's a narrow I or a wider O</td><td>distinguished by small, decorative lines, usually at the top or at the bottom of the letters and tend to be viewed as traditional and formal.</td><td>do not have decorative lines, and are often thought of as contemporary and modern</td>
>    </tr>
>    <tr><td>often used for wedding invitations or greeting cards<br>For the web, it's usually reserved for headlines or small, decorative text details</td><td>For the web, reserved for headings and decorative details</td><td>often used for displaying code</td><td></td><td></td>
>    </tr>
>   <tr><td><img src="https://user-images.githubusercontent.com/64577273/149468760-54071da2-ce04-455a-8b41-00bd80ae77e0.png"></td><td><img src="https://user-images.githubusercontent.com/64577273/149468926-c37eff0d-f585-4223-99a9-9044bd42fe24.png"></td><td><img src="https://user-images.githubusercontent.com/64577273/149468984-ac97501c-dcc4-4b67-8b98-7fb17ff3432c.png"></td><td><img src="https://user-images.githubusercontent.com/64577273/149469118-c8938389-f5f9-4435-b7b9-4f2344711f0c.png"></td><td><img src="https://user-images.githubusercontent.com/64577273/149469195-12a8ce7b-93a4-4f73-8686-166786c3945f.png"></td>
>   </tr>
></table>
>
>-though trends may change, you should make sure you're using legible fonts

typeface or font family-It's the design of lettering that can include variations in size, weight (e.g. bold), slope (e.g. italic), width (e.g. condensed), and so on.

font-It refers to a particular weight, width, and style within that typeface.
<table>
    <tr><td>For example, Helvetica is a well known typeface. So, 12 point Helvetica is a font, and 10 point Helvetica is a separate font. The same goes for different weights – a 14 point Helvetica Bold is a different font than a 14 pt Helvetica Light. They are different fonts, but the same typeface. <br><a href="https://hobancards.com/blogs/thoughts-and-curiosities/difference-between-font-and-typeface">Full descriptions</a></td>
    </tr>
</table>

glyph-a small symbol; it can represent a word, letter, or number, and it can also be a mark that tells you how to pronounce a letter

tone-the mood or general feeling of something

traditional-describe a usual way of doing things; following or belonging to the customs or ways of behaving that have continued in a group of people or society for a long time without changing

casual-informal; relaxed in style or manner

gain popularity-become popular [more info](https://english.stackexchange.com/questions/169734/gain-in-popularity-vs-gain-popularity)

gain in popularity-become more popular [more info from macmillan dictionary](https://www.macmillandictionary.com/dictionary/british/popularity)

childlike-associated with a child; (of adults) showing the good qualities that children have, such as trusting people, being honest and enthusiastic

spread-extend over a large or increasing area

invoke-to cause something to be used; bring into effect

elegant-graceful and attractive in appearance or behaviour

monospace-letters and characters each occupy the same amount of horizontal space

serif-it's a decorative stroke that finishes off the end of a letter (sometimes also called the feet of the letters)

sans-without

sans serif-a style of type without serifs

script fonts-they are beautiful typefaces that resemble handwritten and calligraphic lettering styles; It's written with rounded letters that are joined together in a flowing manner(also know as cursive)

sparingly-in a restricted or infrequent manner

resemble-look like

calligraphy-(the art of producing) beautiful writing, often created with a special pen or brush

ornamental-serving or intended as an ornament; decorative

ornament(noun)-an object that is decorative rather than useful

think of as-*in my point of view* tend to be; to consider someone or something in a particular way

contemporary-belonging to or occurring in the present

trend-a fashion

rise-to increase in number, amount, or value

legible-(of writing or print) able to be read easily
## Changing the font-family
>-To set the typeface in CSS, use the `font-family` property. The first value is your first choice. The following options are fallback alternatives. This list is referred to as a **font stack**.
>```css
>body {
>    font-family: Helvetica, Arial, sans-serif;
>}
>```
>-There's no limit to the number of font options to include but two or three is pretty standard. You should at least have your preferred font, followed by a generic font last. If the user's OS doesn't have a particular font-family installed, it will default to the next item on the list.  
>-<a name="five-categories-of-generic-typefaces"></a>**here are five categories of generic typefaces**
><table>
>    <tr><td>cursive</td><td>fantasy</td><td>monospace</td><td>serif</td><td>sans-serif</td>
>    </tr>
>    <tr><td>usually matches to script or decorative fonts</td><td>usually matches to more unconventional decorative fonts</td><td colspan=3>match up to the typefaces within the same category</td>
>    </tr> 
></table>
>
>-web safe fonts are a number of fonts that are generally pre-installed on the majority of computers and devices, such as Arial and Times New Roman.  
-[cssfontstack.com](https://www.cssfontstack.com/) lists all of the web-safe fonts and also categorizes them by typeface.  
-CSS expand font options using web fonts with `@font-face` or online web services.  
>-If font-family names contain numbers or characters, other than a hyphen, do either of the following:
>* wrap the font-family name in single or double quotes (recommended)
>* escape character must be used before those invalid characters. [more example](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family#valid_family_names)  
![image](https://user-images.githubusercontent.com/64577273/149621608-1474bfc7-b777-44e2-aa7d-aaced7186efd.png)
>
>-it's not required, but recommended to add quotes to font-family names that contain spaces.  
>-generic font names must always be declared without quotes
![image](https://user-images.githubusercontent.com/64577273/149621753-f5a18d5e-7b1e-4d04-b477-9e9e1d32c14b.png)

generic-shared by, relating to a whole group of similar things, rather than to any particular thing

cursive-It's written with rounded letters that are joined together in a flowing manner(also known as script)

fallback-something that can be done if the original plan does not succeed, or that can be used if the thing that you want is not available

hyphen-a short line sign (-) used to join words and to separate syllables of a single word

escape character-It's a backslash \ followed by the character you want to insert [more info](https://www.w3schools.com/python/gloss_python_escape_characters.asp)
## Font-weight and font-style
>-The `font-weight` property sets the weight (or boldness) of the font through following values ([great explanations on W3C](https://www.w3.org/TR/2018/REC-css-fonts-3-20180920/#propdef-font-weight)):
>* numbers, ranging from 100 to 900, [like this example font](https://fonts.google.com/specimen/Montserrat?query=montserr)
>```css
>font-weight: 100;  /* lightest or thinnest */
>font-weight: 200;
>font-weight: 300;
>font-weight: 400;
>font-weight: 500;
>font-weight: 600;
>font-weight: 700;
>font-weight: 800;
>font-weight: 900;  /* darkest or thickest */
>```
>Notice: Quite often there are only a few weights available for a particular typeface. When you use a value to specify a weight for which no font file exists, the face with the nearby weight is used.
>* in CSS, there are only two keyword values that correspond to a specific number:
>    * `normal` is equal to 400, and is also the default for body text
>    * `bold` is equal to 700, and is the default for headings and other bolded styles like strong text
>   ```css
>   font-weight: normal;
>   font-weight: bold;
>   ```
>* keyword values that relative to the inherited font-weight from a parent element according the following table:
>    * `bolder` specifies a bolder weight than the inherited value
>    * `lighter` specifies a lighter weight than the inherited value
>    ```css
>    font-weight: lighter;
>    font-weight: bolder;
>    ```
>![image](https://user-images.githubusercontent.com/64577273/149636999-7a0b98e4-7dbf-4769-8219-6ede3dcb3d2b.png)  
>-`font-style` property includes three values:
>* `italic` tend to appear slightly more cursive
>* `oblique` are generally sloped versions of the regular face.  
>Notice: it's often hard to see these differences and vary among typefaces.
>* `normal`value will remove the italic or oblique style
>```css
>p {
>    font-style: italic; /* add italic style */
>}
>em {
>    font-style: normal; /* removes italic style */
>}
>```
>-both of these properties are inheritable. experiment with them [in here](https://codepen.io/christinatruong/pen/drQeqa) through the following steps:
>1. add `font-weight: bold` to the `header` selector:
>    * the paragraph will be bolded
>    * The `<h1>` looks the same because it's already bold by default
>2. add `font-weight: 400;` to `header h1`:
>    * remove the bold style from the heading
>    * because the `normal` keyword is 400, so if I change this to "normal", it will look the same.
>3. add `font-style: normal;` to `i` selector
>    * remove the default italic style from its element by setting it to "normal"
>
>-above sample code is another example of separating semantic html content from style and CSS properties to add or remove any styles.

roughly-approximately

correspond-to match or be similar or equal
## Web fonts with @font-face
>-font files can be downloaded along with the website to expand typeface options.  
-add any font to your webpages with `@font-face` rule within 2 steps:
>1. declare font files in stylesheet
>```css
>@font-face {
>    font-family: "My Font";
>    src: url(my-font.woff); /* relative path */
>    /* or */
>    src: url(http://example.com/fonts/my-font.woff); /* absolute path */
>}
>```
>Notice: if `url` functional datatype contains any special characters like the parenthesis, commas, white space, single quotes, or double quotes it must be enclosed in quotes or escaped with a backslash.  
![image](https://user-images.githubusercontent.com/64577273/150672242-a2673faf-3ad0-49b0-a917-b6c7fbd4e3a0.png)
>
>2. set specified font-family name to the html elements
>```html
>body {
>    font-family: "My Font", Helvetica, sans-serif;
>}
>```
>-review relative path formats through the 2 following examples:
>1. When we linked to our CSS file, the file path was relative to the location of the HTML file.  
![image](https://user-images.githubusercontent.com/64577273/150676805-1010ec65-35d8-424e-b1a3-4df243d83517.png)
>
>2. Since the `@font-face` declaration is made in the CSS file, the font file path must be relative to location of styles.css  
![image](https://user-images.githubusercontent.com/64577273/149827073-a77d644f-f1c8-4643-8385-ded9a725746a.png)  
Notice: Use `../` to move up and out of the CSS folder first, then `fonts/` to move into the folder, then the font file name.
>
>-although the `woff` and `woff2` formats are supported in most modern browsers but for some older browsers, different formats are required. To list multiple font files, add a comma between each `url` value. if curious about the reason of 2 `src` in following `@font-face` declaration, [check this clarifications](https://teamtreehouse.com/community/why-there-is-two-src-in-a-fontface).
![image](https://user-images.githubusercontent.com/64577273/150681161-4521bd0c-fd28-4566-814a-b1405615eb03.png)  
-[Font Squirrel](https://www.fontsquirrel.com/tools/webfont-generator) has a free font generator that can create different file types. [based this guidance](https://www.fontsquirrel.com/blog/2010/12/how-to-use-the-generator) it only allow to upload TrueType (.ttf) or OpenType (.otf) fonts.  
-to learn more about `@font-face` and support for older browsers, [check out this article by CSS-Tricks.](https://css-tricks.com/snippets/css/using-font-face-in-css/)
## Web fonts with Google Fonts
>-with web font online services you don't need to download any font files or use the `@font-face` rule. Instead, you link directly to their CSS font files, which are hosted on their servers.  
-[Adobe Fonts](https://fonts.adobe.com/) require subscription service and [Google Fonts](https://fonts.google.com/) is a free alternative.

caveat-a warning or caution; admonition

flare-to become wider, or to make something wider

drawer-It is a box-shaped container inside a piece of furniture that can be pulled out horizontally to access its contents

drawer component-It is a panel that slides out from the edge of the screen
## Project: Google Fonts
>-to load Google font style sheet, we can use [the standard `<link>` option](https://fonts.google.com/share?selection.family=Caveat|Montserrat:wght@400;600). the names of the font are at the end of the URL.  
-Under "CSS rules to specify families" section, the example shows the font-family name to be used when referencing the Google fonts.  
![image](https://user-images.githubusercontent.com/64577273/150959195-a7e3033e-243c-450b-af5f-3f34221d05d0.png)  
-when choosing more font styles the web page has to load more resources which slow down your website. Usually a font in a regular weight and a bold or a semi-bold is enough.  
-through the following steps, use a couple of google fonts on our project:
>1. choose the regular 400 and semi-bold 600 for Montserrat and just regular for Caveat in [google fonts](https://fonts.google.com/)
>2. add generated `<link>` to the `<head>` section of your [index.html](Project-Google-Fonts/index.html) file. Put it right before the styles.css file so it can load before our style sheet loads.  
>3. add "Montserrat" as base font family to the `body` selector in [styles.css](Project-Google-Fonts/css/styles.css) so all the elements can inherit the style.
>4. add "Caveat" for the `h1` and the `h2` headings while stick with the "Montserrat" font for the `<h3>` headings.
>```css
>h1, h2 {
>    font-family: 'Caveat', cursive;
>}
>```
>-When using different font families, the way the default sizing of the characters are rendered will vary.  
-experiment with font styles in diffrent conditions:
><table>
>    <tr><th>condition</th><th>font styles</th><th>sample code example</th><th>hint</th>
>    </tr>
>    <tr><td rowspan=2>the default font-weight for:<ul><li>all heading levels and bold texts are 700</li><li>other texts are 400</li></ul>the size of each element vary due to different font size.</td>
>    <td>Regular 400 + Bold 700</td><td><a href="https://codepen.io/imahdio/pen/ZEazJgG">sample code 1</a></td><td>there is not any significant difference with next sample code, except the typography of italic style due to lack of "Regular 400 italic" style</td>
>    </tr>
>    <tr><td>all 9 available styles included</td><td><a href="https://codepen.io/imahdio/pen/jOaNLzd">sample code 2</a></td><td>among all 9 available styles, only 3 styles are used including: regular and italic 400 and regular 700</td>
>    </tr>
>    <tr><td>common paragraph, bold, headings map to closest available font weight.</td><td>Thin 100 + Black 900</td><td><a href="https://codepen.io/imahdio/pen/bGYbrPz">sample code 3</a></td><td><ul><li>For all the text, other than the headings and bolds, the default font-weight 400 map to next closest available font-weight of 100.</li><li>For the headings, the default font-weight 700 map to next closest available font-weight of 900.</li></ul></td>
>    </tr>
>    <tr><td rowspan=2>when any bold or italic styles are not available, browser will generate a computed bold or italic styles based regular font style.</td><td>Thin 100</td><td><a href="https://codepen.io/imahdio/pen/WNXeOxR">sample code 4</a></td><td>bold and italic styles can be generated based regular style</td>
>    </tr>
>    <tr><td>Thin 100 italic</td><td><a href="https://codepen.io/imahdio/pen/jOaNLzd">sample code 5</a></td><td>regular style couldn't be generated based italic style while bold is still generated.</td>
>    </tr>
></table>

montserrat-serrated mountain; a British territory in the Caribbean Sea that is an island

serrated-having a row of sharp points along the edge

moderate-being within a middle range in size, amount, or degree; neither great nor little

beforehand-before an action or event; in advance

end up-to reach some conclusion, state, or situation due to a particular course of action

distinct-clearly separate and different (from something else)

upcoming-about to happen; forthcoming
## The font-size property
>-the font size property defines the size of the font. In this lesson we'll focus on two types:
><table>
>    <tr><th colspan=2>1-relative</th><th>2-absolute</th>
>    </tr>
>    <tr><td colspan=2>it is calculated in relation to the parent's or nearest ancestor's font size</td><td>It's fixed and not affected by any ancestor element</td>
>    </tr>
>    <tr><td colspan=3>Both relative and absolute font sizes are inherited by descendant elements.</td>
>    </tr>
>    <tr><td>font-size: em</td><td>font-size: rem</td><td>font-size: px</td>
>    </tr>
>    <tr><td>it's a size in relation to its closest ancestor element font size.</td><td>rem stands for root em. it's only relative to the <code>&lt;html&gt;</code> root element font size.<br>The sizing of the parent or ancestor element does not affect the rem unit.</td><td>It's an ideal unit for accuracy. computer screens are measured in pixels.</td>
>    </tr>
>    <tr><td colspan=2>can use whole numbers or decimal points to calculate more precise font size.</td><td>use whole numbers, avoid decimals because different browsers interpret decimal values inconsistently.</td>
>    </tr>
>    <tr><td><b>1em = inherited font-size</b><br>If no font-size is declared anywhere, then 1em is equal to the default browser font size.</td><td><b>1 rem = inherited root element font-size</b></td><td>The default size of the document text is equivalent to 16 pixels, with the exception of headings.<br><a href="https://codepen.io/imahdio/pen/LYOYLvK">inspect elements with developer tools on this example code</a><br><img src="https://user-images.githubusercontent.com/64577273/151112586-66201562-7e56-4006-bf46-4ea293a52db0.png"></td>
>    </tr>
></table>
>
>Notice: although the em unit was originally based on the width of the letter "M", this is no longer the case, and now the em unit generally refers to the point size of the font.  
>-experiment with this [example code](https://codepen.io/christinatruong/pen/gEQWMw):
>1. set `font-size: 2em;` of child element, it will be equivalent to 32 pixels.
>2. set `font-size: 2em;` of the parent, the child element will now be twice the size of parent value.
>3. set `font-size: .5em;` of the child, now it will be half the size of the parent element.
>4. set `font-size: 60px;` of the parent, the child element will be half the size of 60px.
>5. set `font-size: 1rem;` of the child element, it will be equivalent to 16 pixels.  
Notce: In tools like CodePen, `<html>` or `<body>` tags are already loaded behind the scenes so we can still use them as selectors.
>6. set `font-size: 2rem;` of html element, the rem unit in the child element will now be relative to that.
>
>-rem is usefull if you want to reduce the font sizes for smaller screens. Instead of changing the size for various elements, you can use rem for these elements and then just change the html value.  
-see more length and keyword values that can be used for font sizes in [the MDM documentation](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size).

varity-many different types of things or people

ancestor-a person related to you who lived a long time ago

ancestor element-an element that contains (at any level) other elements is an ancestor of the elements that it contains. [check here for more info](https://www.littlewebhut.com/css/info_element_relationships/)

descendant-a person who is related to you and who lives after you, such as your child or grandchild

descendant element-an element that is contained (at any level) within another element is a descendant of the element that contains it. [check here for more info](https://www.littlewebhut.com/css/info_element_relationships/)

accuracy-It is closeness of the measurements to a true value

inconsistently-in a way that does not stay the same

name after-to give someone or something the same name as someone or something else, especially the same first name as a member of your family

precision-It's the closeness of the measurements to each other.
## Font shorthand
>-`font` property is shorthand for:
><table>
>    <tr><th><code>font-style</code></th><th><code>font-variant</code></th><th><code>font-weight</code></th><th><code>font-size</code></th><th><code>line-height</code></th><th><code>font-family</code></th>
>    </tr><td>optionally included</td><td>optionally included</td><td>optionally included</td><td><b>must included</b><br>Order matters!</td><td>optionally included</td><td><b>must included</b><br>Order matters!</td>
>    <tr><td colspan=3>Must precede <code>font-size</code><br>but the order among themselves do not matter</td><td></td><td>must immediately follow <code>font-size</code>, proceeded by a forward slash</td><td>must be the last value specified</td>
>    </tr>
>    <tr><td><ul><li>normal</li><li>italic</li><li><a href="https://www.w3schools.com/cssref/pr_font_font-style.asp">etc</a></li></td><td><ul><li>normal</li><li>small-caps</li><li><a href="https://www.w3schools.com/cssref/pr_font_font-variant.asp">etc</a></li></td><td><ul><li>normal</li><li>bold</li><li>numbers, ranging from 100 to 900</li><li><a href="https://www.w3schools.com/cssref/pr_font_weight.asp">etc</a></li></td><td><ul><li>length (relative or absolute values)</li><li>Percentage</li><li>keyword values</li><li><a href="https://www.w3schools.com/cssref/pr_font_font-size.asp">etc</a></li></ul></td><td><ul><li>number</li><li>length (relative or absolute values)</li><li>Percentage</li><li><a href="https://www.w3schools.com/cssref/pr_dim_line-height.asp">etc</a></li></ul></td><td>family-name</td>
>    </tr>
></table>
>
>![shorthand-longhand](https://user-images.githubusercontent.com/64577273/151174986-78beed17-3c70-429c-b272-9e4410c17933.jpg)  
>-to find more information, [review the font properties on MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/font).

precede-to be or go before in order or position

proceed-move forward, to continue as planned

philosophy-the philosophy of a subject is a group of theories and ideas related to the understanding of that subject

get the hang of something-to learn how to do something, esp. when it is not simple or obvious
## Text-decoration, text-align, and line-height
>-`text-decoration` actually represents three longhand properties:
><table>
>    <tr><th><code>text-decoration-line</code></th><th><code>text-decoration-color</code></th><th><code>text-decoration-style</code></th>
>    </tr>
>    <tr><td colspan=3>the order of properties among themselves don't matter</td>
>    </tr>
>    <tr><td>experiment with its various values in <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-line">related MDN documentation</a>, including:</td><td>experiment with its various values on <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-color">related MDN documentation</a>, including:</td><td>experiment with its various values on <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-style">related MDN documentation</a>, including:</td>
>    </tr>
>    <tr><td><ul><li>none</li><li>underline</li><li>overline</li><li>line-through</li><li>underline overline</li><li>underline line-through</li><li>etc</li></ul></td><td><ul><li>keywords</li><li>rgb()</li><li>hex color codes</li><li>etc</li></ul></td><td><ul><li>solid</li><li>double</li><li>dotted</li><li>dashed</li><li>wavy</li><li>etc</li></ul></td>
>    </tr>
></table>
>
>![shorthand-longhand](https://user-images.githubusercontent.com/64577273/151306956-da54d182-d36f-48f6-82f0-c606a3f65ed2.jpg)  
>-the `text-align` property can be used to align content within a block element.You can add it to the HTML element itself, or set the property in the parent element, so the style can be inherited.  
-`line-height` property sets the amount of space between the lines of the content. It can be used with length values(e.g. px, rem), unitless numeric values, or percentages.  
>-experiment with [this example](https://codepen.io/christinatruong/pen/YggdKN?editors=1100):
>1. center align the `<h1>` heading using `h1` selector.  
Notice: this only works for `block` elements, not `inline` or `inline-block` elements, unless you use the `display` property to change the behavior.
>2. add `text-align` to the `header` selector and set it to `right`, `center`, `left` or `justify`. all the nested elements will inherit this style, including images, blocks, and inline elements.  
**Notice:** `justify` add spacing between the words to evenly space the text to the left and right of the containing element. this style is usually used for text displayed in narrower columns. But it can be hard to read for wider blocks of text.
>3. add `line-height` property. cons of absolute values is problem of no space or overlapping between the lines when font-size vary. So, to be more flexible to changes, use a relative unit, such as a percentage or uniyless values.  
**Notice:** if I set this value to 150%, it will always be 150% of whatever the font-size is. if I set this value to 1.5, it will also be one and a half times the size of the font size.

evenly-covering or affecting all parts of something equally [Great definition](https://www.mathsisfun.com/definitions/divide-evenly.html)

go to-the best person, thing, or place for a particular purpose or need
## Project: Typography styles
>-let's incorporate some CSS properties into [our projects](https://codepen.io/christinatruong/pen/YggdKN?editors=1100):
>1. set `font-size: 15px;` to the body element  
Notice: The browser default is 16 pixels, but you can choose to go a little smaller or a little bigger, or keep it as is.
>2. add `line-height: 1.5;` to body element to increase the spacing between the every lines one and a half times the size of my font size.  
Notice: based my test and tries on [this example code](https://codepen.io/imahdio/pen/gOXpGQz) and [this table](https://codepen.io/imahdio/pen/eYeNeXE), there are 2 significant differences between `height` and `line-height`.
><table>
>    <tr><th><code>height</code></th><th><code>line-height</code></th>
>    </tr>
>    <tr><td>not inherited by nested elements</td><td>inherited by nested elements</td>
>    </tr>
>    <tr><td>adjust the element area from top of the context and stretch in down side regardless of symmetrical expansion</td><td>adjust the element area from center line of the context and evenly stretch to add proportional space around the top and bottom of each line</td>
>    </tr>
>    <tr><td colspan=2>both adjust the height of element content area</td>
>    </tr>
></table>
>
>3. set `font-size: 100px;` to h1 selector and set `font-size: 45px;` to h2 selector.
>4. set `font-weight: 400;` to h1, h2 elements. it maps the computed bold style of caviet to the normal weight that I chose for my Caveat Regular 400 font.
>5. set `margin: 0;` to h1, h2 shared block. it removes the extra space around those 2 headers. so remove the duplicated remained `margin: 0;` from h2 element too.  
Notice: The bigger the font, cause the bigger margins proportionally.
>6. set `line-height: 1;` to h1 element to override the inherited line height value from the body styles. It causes h1 to be closer to the h2.

incorporate-take in or contain (something) as part of a whole; include

as is-in the state that something is in at the present time

subtle-not loud, bright, noticeable, or obvious; small but important

make all the difference-to be very important

run small-(especially for clothes)tend to be smaller than most brands with the same label size [Great definition 1](https://hinative.com/questions/2867700?locale=en-US#answer-7422262) | [Great definition 2](https://forum.wordreference.com/threads/run-small-fit-smaller-to-size.3193627/#post-18943187)

bump up-to increase something

quite-absolutely; completely
## Chapter Quiz

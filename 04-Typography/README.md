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
>* numbers, ranging from 100 to 900
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
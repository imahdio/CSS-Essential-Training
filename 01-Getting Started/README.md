# 01-Getting Started
## HTML and CSS
>-Though HTML elements are displayed with basic styling, choosing a particular element because of the way it looks should be avoided. That's what CSS was created for.
><table>
>    <tr>
>        <th>HTML</th><th>CSS</th>
>    </tr>
>    <tr>
>        <td><ul><li>defines the structure of content</li><li>Semantic meaning (adds meaning to the contents)</li></ul></td><td><ul><li>Controls the appearance of the HTML elements</li><li>separate presentation from content with styling</li></ul></td>
>    </tr>
></table>

throughout-in every part, or during the whole period of time
## Browser developer tools
>-every modern browser includes a set of browser developer tools, which can be used to inspect the HTML, CSS and JavaScript on any webpage.  
-you can access developer tools a few different ways, but the most consistent way across browsers is to right click anywhere on the page and select inspect element. The HTML will appear on the left, and the CSS will appear on the right.  
>-in Safari and Chrome, the default styles are listed under, User Agent Style Sheet. This refers to the browsers style sheet. The one custom style I added was to this `<h1>` Heading. We can see color green listed under example.html. Which refers to the file name where the CSS is located.  
![image](https://user-images.githubusercontent.com/64577273/147471314-0aa650fc-cddd-4df1-b550-24b376549459.png)  
-The Dev tools in Firefox is a little bit different, but you can access it in the same way. The HTML displays on the left, but the default styles displays in this third panel under layout. The custom CSS is shown in this middle panel. You can also select the specified arrow icon, to collapse last two panels together then Rules tab for the custom CSS and layout tab for the default. Also notice that instead of showing that the custom CSS is located in the example.html file, it just says inline, which means that the CSS is in the same file as the html file.  
![image](https://user-images.githubusercontent.com/64577273/147471657-f380466e-e008-4050-a872-85b54df51c83.png)  
-for more information about developer tools, [check out this article](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_are_browser_developer_tools) from the Mozilla Developer Network, or MDN for short.

daunting-to make someone feel slightly frightened or worried about his or her ability to achieve something; to discourage

consistent-always happening or behaving in a similar way

the ins and outs-It's all the detailed points and facts about it

trackpad-another term for touchpad

inline-having parts arranged in a line
## Referencing CSS
>-There are three different methods for referencing CSS including 1-External 2-inline 3-internal  
>-External CSS which refers to using a separate CSS file and must be saved with the `.css` file extension. There are two ways to load the external CSS file into the HTML, with a `<link>` tag or using the `@import` method. 
>1. The `<link>` tag is added to the head of the document with two attributes, `rel` and `href`. `rel` stands for the relationship and uses the value of > stylesheet, the `href` value is the path to the CSS file.  
>```html
><head> 
>   <link rel="stylesheet" href="css/styles.css">
></head>
>```
>Notice: You may see above snippet with additional attribute, `type="text/css"` this was required in the previous versions of HTML, but it's no longer needed in HTML5.  
>![image](https://user-images.githubusercontent.com/64577273/147503430-8a489c3d-b530-442f-a541-4b03b80434bd.png)  
><table>
><tr><th>pros</th><th>cons</th>
></tr>
><tr><td><ul><li>Using an external stylesheet is recommended because it separates the CSS from the HTML making it easier to manage.</li><li>one CSS file can be linked to any HTML files and any changes made to the CSS file will be reflected on all the HTML pages that it's being loaded into.</li><li>You can use more than one CSS file</li></ul><td><ul><li>for larger projects and code bases , using too many .css files may defeat the purpose of having separate stylesheets and having one giant CSS file can also become unruly , the @import method can be used to import all the smaller CSS files into a single CSS file, which is then loaded into the HTML document. <img src="https://user-images.githubusercontent.com/64577273/147507302-31d1d408-91e9-4a07-a7f7-63dbcaecc7fd.png"></li></ul></td>
></tr>
></table>
>
> 2. text

void element or empty element-container elements consists of `opening tag+content+closing tag` While void or empty element is an element without content and closing tag

defeat-to win against someone in a fight, war, or competition

unruly-difficult to control or manage

defeat the purpose-to fail to achieve the result you want

downside-a disadvantage or problem 

relevant-connected with what is happening or being discussed

sparingly-in small amounts, in a restricted or infrequent manner

if at all-it is often used to make negatives stronger. [more example](https://www.gymglish.com/en/gymglish/english-grammar/if-at-all)

upcoming-about to happen; forthcoming

inefficient-not organized, skilled, or able to work in a satisfactory way
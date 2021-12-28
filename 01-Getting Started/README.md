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
>-There are three different methods for referencing CSS including External ,inline and internal.  
>-❶ **External CSS** which refers to using a separate CSS file and must be saved with the `.css` file extension. There are two ways to load the external CSS file into the HTML, with a `<link>` tag or using the `@import` method. 
>1. The `<link>` tag is added to the head of the document with two attributes, `rel` and `href`. `rel` stands for the relationship and uses the value of  `stylesheet`, the `href` value is the path to the CSS file.  
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
><tr><td><ul><li>Using an external stylesheet is recommended because it separates the CSS from the HTML making it easier to manage.</li><li>one CSS file can be linked to any HTML files and any changes made to the CSS file will be reflected on all the HTML pages that it's being loaded into.</li><li>You can use more than one CSS file</li></ul><td><ul><li>for larger projects and code bases , using too many .css files may defeat the purpose of having separate stylesheets<br>and having one giant CSS file can also become unruly therefore<br>the <code>@import</code> method can be used to combine the files.</li></ul></td>
></tr>
></table>
>
> 2. The `@import` rule as second external method imports one or more stylesheets into HTML files or into another CSS file. This method can be used to import all the smaller CSS files into a single CSS file, which is then loaded into the HTML document between a style tag in the `<head>` of the document.  
>![image](https://user-images.githubusercontent.com/64577273/147554441-49acc81e-0369-451f-9345-0835826f844b.png)
>
><table>
><tr><th>pros</th><th>cons</th>
></tr>
><tr><td><ul><li>The <code>@import</code> method is however, commonly used with CSS preprocessors such as SASS or LESS</li><li>or when CSS files are compiled into one file before loading it into the page.</li></ul><img src="https://user-images.githubusercontent.com/64577273/147554580-f87ffb81-6054-4dcf-947e-71cb31cd2fbb.png"></td><td>This method isn't used often these days because the downside to using <code>@import</code> is the potential for slowing down your page speed. <code>@import</code> does not allow for parallel downloads, meaning the page must download an entire stylesheet before it loads the rest of the page.<br><a href="https://www.stevesouders.com/blog/2009/04/09/dont-use-import/">for more info , check detailed blog posts in here</a><br>that's why we'll be using the link method for our projects. </td>
></tr>
></table>
>
>-❷ **inline CSS** uses a style attribute which is added to the opening HTML tag.
>```html
><p style="color:red;">red paragraph</p>
>```
><table>
><tr><th>pros</th><th>cons</th>
></tr>
><tr><td>The CSS style rules are added as the value, which applies style directly to the HTML element.<br><br><img src="https://user-images.githubusercontent.com/64577273/147554724-7ca7cb53-025f-4341-a2c3-49a8fb540a3a.png"></td><td><li>The inline method should be used sparingly, if at all, because it is hard to manage.</li><li>CSS added by any other method is overwritten by the inline styles, creating more potential for conflict with other CSS style rules.</li><li> The inline method is also not reusable since it's applied directly to each element.</li></td>
></tr>
></table>
>
>-❸ **internal CSS** is added between the `<style>` tag in the head of the document.  
>```html
><head>
>    <style>
>        h1 {
>            color: green;
>        }
>        h2 {
>            color: blue;
>        }
>    </style>
></head>
>```
><table>
><tr><th>pros</th><th>cons</th>
></tr>
><td>This method is more flexible than the inline method because instead of adding styles to each individual element, CSS selectors are used to apply a style to all the matched elements.</td><td>If you had multiple HTML pages, you would have to copy this style block to every single page to duplicate the styles. The internal method is best for short blocks of CSS that only need to be applied to one page.</td>
></tr>
></table>
>

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
## Project overview and setup
 >-in this course we'll be learning CSS by applying each concept to the HTML template included in the exercise files. And for some context, [here's how the final project will look.](https://christinatruong.github.io/css-essential-training/css-portfolio/)  
-you can customize the content however you wish by updating the text, copy in images but keep the HTML structure the same so you could follow along with the exercises.  
-When naming folders and files, use lowercase letters and avoid using spaces or special characters just to ensure that everything displays properly.  
-the html homepage is always named index.html  
-[let's open the index.html file to see what we can customize in here](Project-overview-and-setup\index.html) and start by updating the `<title>` tag to describe your page. throughout the body section there are organizational comments as well as instructions for how to customize the HTML content while maintaining the page structure.  
-[meettheipsums.com](https://meettheipsums.com/) links to various text generators that you can use to add some realistic text.

for context-for(in order to provide) additional related facts which can give you some **perspective** on the length of time involved. Similar to putting a person next to a very large object in a photo so you can sense how big it actually is in real life.

potfolio-It's a compilation of materials that exemplifies your beliefs, skills, qualifications, education, training and experiences. It provides insight into your personality and work ethic.

resume-a written statement of your educational and work experience

descriptive-describing something, especially in a detailed, interesting way

whichever-any one from a limited set

Hands on learning-learning by doing

versus-used to compare two things or ideas, especially when you have to choose between them

upcoming-happening soon, about to happen

revise-to change or correct something, esp. a piece of writing
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
## Optimizing images and retina displays
>-*based on my point of view , this lesson has some incomplete concepts which incompatible with [this lesson](https://github.com/imahdio/HTML-Essential-Training/blob/ddf4faedd53a8157ce1037e28706f01821649c7e/05-Images%20and%20Graphics/README.md#responsive-images) , that's why I try to gather my own assumptions based the instructor clues.*  
>-when using images within your websites, there are many ways to optimize for performance and search engine optimization. [for more info read this post with 10 must known image optimization tips](https://christinatruong.github.io/css-essential-training/css-portfolio/)  
-there are 2 ways to fit a 4000 x 3000 pixels image into an image area with 300 pixels width:
>1. resize it to 300 pixels width with CSS, which would take an unnecessary load on the webpage.
>2. cropping image to appropriate size width
>
>-apple's Retina display is a trademarked term coined by Apple, and is used to describe their high pixel density screens. Other manufacturers have their own high pixel density screens.  
-pixel density refers to how many pixels are contained within a space , usually measured by pixels per inch, or PPI for short (**which determine actual resolution**), and sometimes referred to as dots per inch or DPI. 
>- [more info about PPI calculation method is in here](https://www.calculatorsoup.com/calculators/technology/ppi-calculator.php)
>- [this source demonstrate PPI(actual resolution) vs DPI(*in my point of view , common or general resolution*) concepts for each specific mobile phone.](https://devhints.io/resolutions)
>
>-2X Retina displays have double the number of pixels per inch and can fit two pixels within the same width and height of a non-Retina display.  
-The more pixels there are within the same area, the smaller the pixels are, which is how text and images appear smoother, clearer, and show more detail.  
-there are 2 ways to support retina and non-retina screens simultaneously:
>1. to use an image twice the size. For example, in our project if we use an image file that is 600 pixels wide, then resize it to 300 pixels with CSS, we are adding double the amount of pixels within the same dimension, just like Retina displays. For both Retina and non-Retina screens, the image will display as 300 pixels wide. But in the Retina display, the image will appear more crisp.
>2. list the images with screen density, like 2X, 3X, 4X. the browser will swap out one version of this image for another based on what it thinks is best. [for more info check the related lesson in here](https://github.com/imahdio/HTML-Essential-Training/blob/ddf4faedd53a8157ce1037e28706f01821649c7e/05-Images%20and%20Graphics/README.md#responsive-images)  
>
>-The placeholder images included in the exercise files are already sized accordingly. But if you want to use your own images, resize the thumbnails to 600 pixel width. For the background image, anywhere between 1400 pixels to about 2000 pixels wide should work. 

coin-invent (a new word or phrase)

crisp-a crisp sound or image is very clear

apparent-able to be seen or understood
## Project: Relative paths
>-Building websites often involves linking different files together, such as embedding an image in the html, or referencing a css file. When linking to files within the same project, use a relative path.  
-in following image, the index file is in the same folder as the css and image files. So, from index.html, the file path can map directly to the corresponding file names.  
![image](https://user-images.githubusercontent.com/64577273/147644997-f484cf98-5dfa-4ed4-8766-8d6bfa8227cd.png)  
-if the file you're linking to is contained within a folder, like the following image, the folder name must also be included in the file path.  
![image](https://user-images.githubusercontent.com/64577273/147645180-4acba4ed-5435-4bfb-aa66-5a1177ba2501.png)  
-in this lesson , we do the following modifications
>* from [index.html](Project-Relative-paths\index.html) update the image `src` value and `alt` attribute as well to provide a description for screen readers and make the images accessible.  
>```html
><img src="images/project-courses.jpg" alt="Lynda & LinkedIn Learning course list">
>```
>Notice: Once your file path is updated to point to the correct image file, open it in your browser.  
Notice: By default, images are displayed in the same dimensions as the file size which is currently 600 pixels wide.
>* create a css file to resize the images. It can be named anything, but some common conventions are simply styles, or global, or the project name, like portfolio. I'm going to call mine `styles.css` and save it to CSS folder.
>* let's add a `<link>` tag in the `<head>` section of [index.html](Project-Relative-paths\index.html). It can go anywhere in the `<head>` section, but I like to put mine just before the closing tag like this:
>```html
><link rel="stylesheet" href="Project-Relative-paths\css\styles.css">
>```
>Notice: There is this autocomplete feature for writing html. Type in the element you want to add, in this case it's `link`, but without the angled brackets, and press tab. The editor completes the tag, and all I have to do is update the `href` value to point to our css file.
>* add the style in `styles.css`
>```html
>img {
>    width: 300px;
>}
>```
>
>Notice: in above code snippet , `img` select the images in [index.html](Project-Relative-paths\index.html)

embed-to include text, sound, images, video, etc. in a computer file, email message, or on a website

declaration-when you declare something, you just tell what it is. [Check here for more info](https://stackoverflow.com/a/48892360)

definition-when you provide how it actually works, that's the definition of it. [Check here for more info](https://stackoverflow.com/a/48892360)

miss-to not see or hear something or someone , to not notice someone or something

there we go-We have performed an action successfully
## Absolute paths
>-absolute paths refers to a resource located on a server so the entire URL, including the HTTP and full domain name must be referenced. we can use this technique either for linking to pages outside of your website or within your own project files (root relative path)
>```html
><a href="http://website.com"></a>
><a href="http://website.com/posts/"></a>
><a href="http://website.com/posts/page.html"></a>
>```
>-embedding external image resources into your own pages is called hotlinking and should be avoided. Hotlinking is known as the act of stealing someone's bandwidth by linking directly to their website's assets, such as images or videos. The only time it is acceptable is when services are created for the purpose of hosting web resources for people to use.
>```html
><a href="http://notmywebsite.com"></a> //common linking is OK
><img src="http://notmywebsite.com/images/photo.jpg"></a> //Hot linking , Not Ok!
>```
>-with placeholder image services Instead of using a relative path that references a file in your project directory, an absolute path can be used to link directly to a hosted image.  
-most placeholder services will include options and usage instructions for setting the width and height, picking a specific image and more.  
-placeholders are meant to be temporary. So if you want to use a more permanent option, use your own images or a stock photo.  
-you can use something similar to an absolute path within your own project files. It's also sometimes called a root relative path. By adding a forward slash at the beginning of the href value, it assumes the URL is the same as whatever your current URL is, but you need to view your website on a local server during development.  
![image](https://user-images.githubusercontent.com/64577273/147727197-01a7f71d-897c-4508-8edd-f6c7d1529084.png)
>absolute path|root relative path|relative path
>-|-|-
>link directly to an external hosted files|similar to an absolute path but link within your own project files|references a file in your project directory

image placeholder service-designers can use it for quick and efficient display of custom image

Stock photos-they're professional grade photographs that are already taken, edited, and ready to be used
## Chapter Quiz
>-You have a large image that needs to fit into a 400 x 200 pixel area. I should crop the image to 800 x 400 pixels if your users are using 2X Retina displays.  
-In Chrome's Developer Tools view, the default styles listed under the User Agent Stylesheet section on the right.  
-While HTML controls document structure, CSS controls content appearance.  
-`images` is the recommended name you should give the folder that holds your project's images.  
-inline CSS can be used to quickly test local CSS overrides.
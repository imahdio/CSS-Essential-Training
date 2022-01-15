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

script fonts-they are beautiful typefaces that resemble handwritten and calligraphic lettering styles

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

fallback-something that can be done if the original plan does not succeed, or that can be used if the thing that you want is not available

hyphen-a short line sign (-) used to join words and to separate syllables of a single word

escape character-It's a backslash \ followed by the character you want to insert [more info](https://www.w3schools.com/python/gloss_python_escape_characters.asp)
## Font-weight and font-style
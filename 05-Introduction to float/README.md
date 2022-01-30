# Layouts: Float and Position
## Introduction to float
>-Prior to the introduction of Flexbox and Grid Layout Modules, the Float property was used for creating entire document layouts such as adding a sidebar to the main content area or creating multiple columns.  
-there's only partial support for Grid and Flexbox in Internet Explorer.  
-global market share for Internet Explorer is less than 3%, and Microsoft has dropped support for it.  
-you need to support layouts with floats in:
>1. projects using an old code base, usually referred to as legacy code
>2. applications that were originally built for Internet Explorer
>3. simple layouts such as floating an image to have the text flow around it

sidebar-a vertical or horizontal column placed to the right or left of a webpage's primary content area, below or above the content area, footer, header, or any where in the theme.
## The float and clear properties
>-The float property allowed us to create magazine-style layouts with floated elements and text flowing around those elements.  
-The majority of structural HTML elements used to create page layouts are:
>* block-level elements
>* displayed at full width and stacked on top of each other
>
>-The float property can be used to change the normal document flow by floating elements to the left or right side of its container, resulting in the change of the positioning of the surrounding elements.  
>-experiment with [this codepen example](https://codepen.io/christinatruong/pen/ROQdZJ):
>1. uncomment `float: left;` to the image. This will place the image to the left side of its container. The text in the following paragraphs will fill the available area and line up right to the edge of the image.
>2. uncomment `margin: 10px;` to the image. it adds some margin in, to create a little space between the image and the text.
>3. comment out long html paragraph. Now the remaining two paragraphs will flow around the image since they both fit within its space.
>4. add clear class to the second paragraph to return it back to its normal flow.   
Notice: `clear` property clear the float of each element to return the normal flow. The values for `clear` can be `left` , `right` or `both` to specifically clear a left , right or left and right floats.

realize-become fully aware of (something) as a fact; understand clearly.

pave the way (for something/someone)-to make it possible or easier for something or someone to follow

majority-most of the people or things in a group

structural HTML elements-[Good definition](https://ixd-res.clintio.us/web/html/structural.html)

used to-refers to something familiar or routine [Great definition](https://www.merriam-webster.com/words-at-play/is-it-used-to-or-use-to)
 
line up-to arrange people or things in a straight line or row

take (someone or something) out of (someone or something)-To remove someone or something from something or some place

take it out from the normal flow-*based my study friend opinion* they are treated as if they don't exist in the flow of html then they are positioned as the user required

make room-to provide space for someone or something

fill up-become completely full

flow across (something)-To move across something in a smooth, fluid manner, as of a liquid
Readme:

Christopher Chung (cc733) and Ryan Gerber (ryan1105)

Changes:
1) Removed 
/* main level link :hover */
#main-nav a:hover {
	background: #eee;
	color: black;
	cursor: pointer;
}
/* current link :hover 
#main-nav .current_page_item a:hover, #main-nav .current-menu-item a:hover {
	color: #000; background: #eee;
}
*/

This makes the link not visually distinct which can make it difficult for visually impaired users to differentiate clickable from unclickable text.

2) Removed
a:hover {
	text-decoration: underline;
}

This makes the link not visually distinct which can make it difficult for visually impaired users to differentiate clickable from unclickable text.

3) Reduced
line height for paragraph <p> text from 1.8em to 1em

This makes the text difficult to read for people with cognitive disabilities like Dyslexia. Losing the space between lines of text makes it harder to separate individual letters.

4) Changed
body background color from white (#ffffff) to a light purple with 30% opacity if the browser supports it(rgb(25, 25, 128); rgba(25, 25, 128, .3);)

This makes it hard for color blind users with deuteranomaly and protanomaly, also known as red-green color blind, to differentiate the blue text and boxes from the purple background as they have trouble differentiating blue and purple hues.

5) Changed
Sublevel navigation link color to black (#000) and removed the border on the dropdown submenu when hovering over a main navigation link, while matching the color of the dropdown submenu to match the change in body background color (rgb(25, 25, 128); background: rgba(25, 25, 128, .3);)

The purple transparency and link color change to black creates a low contrast which makes it hard for users with low vision to differentiate the black text from the purple background of the dropdown submenu.

6) Removed
The background:none change for body content text upon hovering over a link
(#content.clearfix p a:hover{ })

This makes the link not visually distinct which can make it difficult for visually impaired users to differentiate clickable from unclickable text.

Pre-existing Issues:
After playing with the different accessibility tools, we found Google's Accessibilty Developer Tools worked well in detecting pre-existing issues with the site code. Through the tool we found several issues. The most severe was that the email address input was missing a label which should be included with all controls and media elements. Another issue was that text elements should have a reasonable contrast ration. This was directed at the navigation bar submenu links which didn't meet the contrast ratio rule from Google's tool. A final warning dealt with the semantics tied to several of the links on the page, specifically those in the header and logo. The tool felt that the purpose of each link was not clear from the included link text.

Design Process:
We chose to approach this assignment by going through the different disabilities discussed in class, and focusing on several we felt we could replicate best through the use of the different tools provided in class (i.e. ChromeVOX, NoCoffee, etc.) After first brainstorming the different accessibility changes we wanted to make, we decided on visual and cognitive impairments such as low-vision, color blindess, dyslexia, etc. This was because we could test these disabilities by using ChromeVox to see how a speech reader would read contextual text in the HTML and NoCoffee to see how a screen would appear to a visually impaired user. Once we figured out the appropriate changs, we implemented and then tested them to see how effective they were.

Work Breakdown:
We worked together in the beginning, by brainstorming what sorts of changes we could make that would affect accessibility. After generating several ideas for both style changes in the CSS and contextual changes in the HTML, we separated and implemented the work. Ryan worked on the HTML changes while Chris worked on the CSS changes. This was all managed on Github. Once all the changes were implemented, we merged the code and tested it ourselves, comparing it with the original MHCID version. Finally, we completed the readme.

Documentation:
https://www.w3.org/WAI/demos/bad/before/annotated/home.html
(The before and after feature of this site, to see the changes from inaccessible and accessible were extremely useful in redesigning the MHCID home page to be less accessible. This is a great tool to see how minute changes can make a large difference on the user experience for users with disabilities.)

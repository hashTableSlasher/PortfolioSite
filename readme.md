Recap of initial Acceptance Criteria from Module 2
--------------------------------
Responsiveness
--------------
I basically said that responsiveness should not be based solely on media queries and flexible baselines would be given so resources and styling stretched further and were only implemented based on desired layout changed that made sense (text size, etc) would limit the amount of media queries needed and would fit within the smallest and largest width provided on the dropdowns provided by browsers in Devtools. 

Accessibility
--------------
I stated that accessibility would look like good rich descriptions in the alts of images on the site and with good semantic HTML

Browser Support
--------------
I stated that there would be a fallback font-list that was backed by MDN's documentation of browser supported fonts, and approximate layout would remain the same.

Metadata or Discoverability 
--------------
All I stated was the need to properly link to CSS files for styling

Performance
--------------
I stated that I wanted a green (indicating good) performance audit on lighthouse auditing tools on Chrome

Release Quality
--------------
I states I wanted good clear ,visible feedback on state changes like hover/active, etc.




Any Changes and Additions in Acceptance Criteria from original Acceptance Criteria Starter
---------------------------------
Responsiveness
--------------
Change: In the original starter for Acceptance Criteria I stated that I would use Media queries based on width to change the layout, this before I had a good understanding of the repeat grid and we had an assignment and lessons indicating that container queries were better. I also said that I would do a hamburger menu, but instead I opted for a flexible menu that still works in mobile.

Accessibility
--------------
Additions: I additionally would like to ensure there is further accessibility with good media queries that indicate user preference vs original plan to use them for responsiveness. Media queries take into account
site change based on preferences for contrast.

Metadata and discoverability
--------------
Additions: Site should have rich metadata that lends itself to site sharing as well as rich descriptions and page titles as well as original 



Changes I did in Checklist Sprint from Release Plan
---------------------------------------------------
CSS Validation: I did not get rid of all errors 
but errors seems to be due to lack of recognition for modern syntax of container type being inline-Size. Most changes in inline-Size statement adapt to larger vs smaller layouts and so content is still readable in single column format. Smaller columns, like that in skills for content remain in small columns or are blocked in a layout that is still highly readable on large and small monitors. Simultaneously, inline-size still seems to enjoy good support as layout remains consistent for most popular Desktop browsers: Bing, Firefox, Chrome and Opera(I figured if Chrome produced the layout so would Opera given they're both Google but it's good to be thorough). I felt that that was appropriate given mobile users would not be using the layout that container query covers.

Font-Size: I did get the responsiveness that I wanted. Content works on most pages on most devices,
but there are some things I'd still like to tweak. I'd like to work on on the education section headings specifically which are a bit long and fold over in a way that has a bit too much spacing. I'd also need to change the font-size of form text, and maybe the profile card to the new clamp body font and see if that feels appropriate or it needs it's a special value.

Font-fallback: I still need to reorder or change values in font-fallback to be compliant with Firefox's 
ordering system for fonts. Specifically it says that "Book Antiqua" is in the wrong place. I'd like to use that above system default fonts but I know there's sometimes better performance for that on older browsers.





Release Evidence:
--------------------
TESTS: 
Performance:
 I wasn't passing performance audit on all pages due to images not having a set width and height on all images according to page, I added aspect ratio to see if that was the problem but it wasn't, I looked it up and realized I needed to add a max-inline size on container images were in so it would pass inspection which worked. I actually ended up forcing aspect ratio in grid pictures on projects page because it dictates their containment in grid to be even and doesn't actually distort the photos ratio there.

Accessibility:
- I tested changed writing modes in css to see if format looked good and it maintained good appearance in vertical formatting. 


Responsiveness:  
(All checked in devtools in chrome and/or Firefox Devtools)
- Elements tab through nicely, font sizes vary when using Firefox devtools to select specific type, card image changes as picture element detects various widths and so does the layout (repeat-grid); Images change can all be trigger and will under various widths in Devtools responsive mode for srcset images. All pages change to single column below certain width, and all repeat grid multiplied columns as necessary under various widths. Elements are given flexible styling to size appropriately when size changes but there is not necessarily a layout change.
-Layout shift is none, and largest contentful paint is good as well which I tested in lighthouse, I further prevented layout shifts by preloading font. Which was explained in web.dev documentation/articles.

Broken Link Checks: 
-All links go where they're intending to when I manually clicked through site.


Accessibility:
-Site had descriptive alts and passes inspection on for good tree formation in lighthouse
-Site has queries for user preference for contrast and no-contrast, tested using Chromes preference indication under rendering.
-Site loads well using zoom and fireFox's 200% text only zoom
-Clear feedback for keyboard controls as well as no keyboard traps
-proper war-aria use in errors for form according to MDN specifications. 

Performance: 
- I wasn't passing for a while because I  didn't give aspect ratio to images, for some reason it wouldn't pass audit inspection unless aspect ratio was in globals (I tried taking it out, doing component specific imgs , and tried several variations on selectors), (it passed picture element in contact because you can give height directly with that syntax). But I got it to pass all inspections.


Browser Support: 
-Layouts seem to work in all major browsers when I opened site using opera, Firefox, Chrome and bing. Site properly styled to do well in smaller media, tested with responsive mode in Chrome and firefox and as it's the default styling when browser doesn't support layout.
-HTML ensures logical layout order when grids don't load.
-There is a fallback font list that is well supported on everything and I've removed book antique from the list as well as system-ui, since I believe everything understands serif.


Metadata and discoverability:
- Test for metadata pass Rich metadata testing, showing image objects for google images with good metadata/copyright information. I also added my name , in author meta for further ties to content.It passes lighthouse standards. 

Release Quality: 
- There is good clear user feedback when tabbing, hovering over and activating interactive elements on the page.





Release Evidence 
---------------------

Accessibility spot checks: 
- I again looked over alts for images, war-aria attributes, etc. and was happy.
Broken links: 
- Tested and confirmed
compatibility notes: 
- I stated this above but essentially not all browsers support certain fonts or container types which is accounted for in the fundamental behavior or default of the site
Known Limitations/Responsive regression tests:
- While I've simulated mobile and all dropdowns for phone options work with the layout,
I cannot account for every mobile device. Though I've tried to build the site in such a way that it does not need to know what a specific devices dimensions are and would adapt to almost any viewport. I have capped the font sizes so there would likely be a limited scale to fonts if it were on a very large tv. 

# Notes for Formula Forge User Guide

## Agenda

Find better arrows than &#11014;, &#11013;, and &#10145;.  These arrows do not have the same width, and Edge displays them with ugly icons.  Try SVG arrows instead of fuzzy PNG images such as ![this](Help/Images/left.png).

Decide whether to put navigation links at the top of the pages of the User Guide, similar to those in the footer.

See <https://www.w3.org/WAI/WCAG21/Understanding/resize-text.html> about using relative rather than absolute sizes in `site.css`.

Write `Screencasts.html`.

Add accessible names to tables.

Investigate appearance on small screens, with other browsers.

Decide what to do about Google Analytics.

## Structure

The User Guide is stored in multiple HTML files rather than in a single monolithic file.

The files in the User Guide, with few exceptions, are styled in the same fashion as the other files on the Formula Forge website.

- The header extends the title _Formula Forge_ to _Formula Forge Help_.
- The footer contains navigation links instead of a link to the privacy notice.

To produce a single monolithic help files, it suffices to extract, anchor, and join the `<div id="content"> ... </div>` sections from the separate files, and to adjust links to use these anchors instead of file names.

## Notes

The screenshots are all taken with PC Excel.

Microsoft has different versions of its help files that contain screenshots (and wording) appropriate for the different versions of its products.  We could emulate this by dividing the `Help` directory into separate subdirectories, `Help/PC`, `Help/Mac`, and `Help/Web`, putting platform-specific images in the `Images` directory of each of these directories, and making small changes in wording wherever appropriate.

The drop-down menu in the header is handled by two functions defined in `site.js`.

## Styles

Style for the help pages defined in `site.css`

- Typeface: Helvetica (because Max OS X does not provide Segoe)
- Fx color: Microsoft’s recommended color #4d82b8
- Title color: #505050
- Header background color: #f0f0f0 (used for Excel’s ribbon)

It's not clear why browsers running under Windows place the logo title _Formula Forge_ somewhat lower than browsers running under Mac OS X.  The top margins for this title and for the header title were reduced by 3px to make the header look better under Windows and still reasonable under Mac OS X.

Microsoft's recommended [typography](https://docs.microsoft.com/en-us/office/dev/add-ins/design/add-in-typography) is problematic because Mac OS X does not provide the Segoe font

- Title: .ms_font-xl, Segoe Light, 21px
- Subtitle: .ms-font-l, Segoe Semilight, 17px
- Body text: .ms-font-m, Segoe Regular, 14px
- Caption: .ms-font-xs, Segoe Regular, 11px

Microsoft's recommended [icon styles](https://docs.microsoft.com/en-us/office/dev/add-ins/design/add-in-icons-monoline)

- rgb(77, 130, 184) or #4D82B8 for icon sizes 32 and above
- rgb(74, 125, 177) or #4A7DB1 for icon size 16

Recommendations in <https://www.64notes.com/design/stop-helvetica-arial/>

- Typefaces
  - Lucida Grande is the author's favorite (but it is not available in Windows)
  - Trebuchet MS is "brilliant" (but it has a strange lowercase g)
  - Verdana, Tahoma look good
  - Helvetica looks better than Arial
  - Georgia is much better than Times New Roman for serifs
- Color
  - Text: #222222 to #555555
  - Background: off white #FAFAFA, #F9F9F9, #F8F8F8

## Out-takes

Users can adjust the heights of the three views by clicking the cursor on one of the horizontal dividing lines and dragging that line up or down.

## Old notes concerning documentation formatted for WordPress

WordPress strips away many HTML tags, strips class information out of other tags, and otherwise mangles the HTML.  This information can be restored, and the HTML cleaned up, as follows.

Remove line breaks from the middle of paragraphs.  These are the same as spaces in raw HTML, but some WordPress themes treat them as actual breaks.

Change the HTML header tags _&lt;h2&gt;_, _&lt;h3&gt;_, and _&lt;h3&gt;_ (which produce headers that were too big) to _&lt;h3&gt;_, _&lt;h3&gt;_, and _&lt;h5&gt;_.

Change the _&lt;blockquote&gt;_ tag, which produces a quotation mark in some themes, to _&lt;p class="centered"&gt;_.

Copy CSS style elements for figures and centered elements from `site.css` into `custom.css`.

Work around a problem with the _&lt;math&gt;_ elements in first sentence in the section on typesetting conventions, which cause line breaks, by replacing them with _&lt;em&gt;_.

Re-cut-and-paste the table in this section if the math markup had disappeared.

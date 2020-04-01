# Notes for Formula Forge Documentation

## Agenda

Find better arrows than &#11014;, &#11013;, and &#10145;.  These arrows do not have the same width, and Edge displays them with ugly icons.  Try SVG arrows instead of fuzzy PNG images such as ![this](Help/Images/left.png).

## Structure

The documentation is stored in multiple HTML files at <https://formulaforge.com/Forge/Help>.  Each file starts with a header that contains a logo, title, and navigation links, and it ends with a trailer that provides the same navigation links.  After the header comes either an `<h1>` tag or an `<h2>` tag,
depending upon whether that page is for a section or a subsection in the table of contents.  The stylesheet, `style.css`, makes the contents of these tags invisible.

If it is ever desired to produce a single document containing all the help files, it suffices to extract (and join) the contents of these files that lie between the header and the trailer, and then to equip the combined document with a new stylesheet that makes the contents of the `<h1>` and `<h2>` tags visible.

The screenshots are all taken with PC Excel.

Microsoft has different versions of its help files that contain screenshots (and wording) appropriate for the different versions of its products.  We could emulate this by dividing the `Help` directory into
separate subdirectories, `Help/PC`, `Help/Mac`, and `Help/Web`, putting platform-specific images in the `Images` directory of each of these directories, and making small changes in wording wherever appropriate.

## Styles

Office font sizes: xxl 210px, title 21px, subtitle 17px, body text 14px, caption 11px

## Out-takes

Users can adjust the heights of the three views by clicking the cursor on one of the horizontal dividing lines and dragging that line up or down.

## Old notes concerning documentation formatted for WordPress

The contents of multiple files were combined into a single file, `FormulaViewHelp.html`, that relied on a simpler CSS stylesheet, `help.css`.

The contents of `FormulaViewHelp.html` were pasted into a new WordPress page.  WordPress stripped away many HTML tags, stripped class information out of other tags, and otherwise mangled the HTML.  This information was restored, and the HTML was cleaned up, as follows.

Removed line breaks from the middle of paragraphs.  These are the same as spaces in raw HTML, but the Definition theme treated them as actual breaks.

Changed the HTML header tags _&lt;h2&gt;_, _&lt;h3&gt;_, and _&lt;h3&gt;_ (which produced headers that were too big) to _&lt;h3&gt;_, _&lt;h3&gt;_, and _&lt;h5&gt;_.

Changed the _&lt;blockquote&gt;_ tag, which produced a quotation mark in the Definition theme, to _&lt;p class="centered"&gt;_.

Copied CSS style elements for figures and centered elements from `help.css` into the Definition `custom.css`.

Worked around a problem with the _&lt;math&gt;_ elements in first sentence in the section on typesetting conventions, which caused line breaks, by replacing them with _&lt;em&gt;_.

Re-cut-and-pasted the table in this section (somehow much of the math markup had disappeared).

The flat bottoms of the letters V and W made the title line appear clipped.  However, the flat bottoms were due to the use of Calibri for the title.  This font was chosen because it had the best italic F for the Fx logo (the only other font with a similar italic F was Trebuchet MS).

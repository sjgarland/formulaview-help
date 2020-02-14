# Notes for Formula View Documentation

## Agenda

Find better arrows than &#11014;, &#11013;, and &#10145;, which Edge displays with ugly icons.  Try SVG arrows instead of fuzzy PNG images such as ![this](Help/Images/left.png).

## Styles

Office font sizes: xxl 210px, title 21px, subtitle 17px, body text 14px, caption 11px

## Out-takes

`Introduction.html`: Users can adjust the heights of the three views by clicking the cursor on one of the horizontal dividing lines and dragging that line up or down.

## Old notes for WordPress documentation

The contents of multiple files were combined into a single file, `FormulaViewHelp.html`, that relies on a simpler CSS stylesheet, `help.css`.

The contents of `FormulaViewHelp.html` were pasted into a new WordPress page.  WordPress seems to have stripped away many HTML tags, stripped class information out of other tags, and otherwise mangled the HTML.  This information was restored, and the HTML was cleaned up, as follows.

Removed line breaks from the middle of paragraphs.  These are treated like spaces in raw HTML, but the Definition theme
treated them as actual breaks.

Changed the HTML header tags _&lt;h2&gt;_, _&lt;h3&gt;_, and _&lt;h4&gt;_ (which produced headers that were too big) to _&lt;h3&gt;_, _&lt;h4&gt;_, and _&lt;h5&gt;_.

Changed the _&lt;blockquote&gt;_ tag, which produced a quotation mark in the Definition theme, to _&lt;p class="centered"&gt;_.

Copied CSS style elements for figures and centered elements from `help.css` into the Definition `custom.css`.

Worked around a problem with the _&lt;math&gt;_ elements in first sentence in the section on typesetting conventions, which caused line breaks, by replacing them with _&lt;em&gt;_.

Re-cut-and-pasted the table in this section (somehow much of the math markup had disappeared).

The flat bottoms of the letters V and W make the title line appear clipped.  However, the flat bottoms are due to the use of the Calibri font for the title line.  This font was chosen because it had the best italic F for the Fx logo (the only other font with a similar italic F is Trebuchet MS).

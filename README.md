HTML Email Template
===================

A template for creating HTML email's which will render consistently across all major email clients. It's designed to reduce time by providing a set of examples for every common email layout.

Structure
----------------------------------------------------------
The template follows this basic structure:

<pre>

&lt;wrapper&gt;
  &lt;spacer /&gt;
  &lt;content&gt;
        &lt;header /&gt;
        &lt;row&gt;
            &lt;column /&gt;
            &lt;column /&gt;
            &lt;column /&gt;
        &lt;/row&gt;
        ...
        &lt;footer /&gt;
    &lt;/content&gt;
    &lt;spacer /&gt;
&lt;/wrapper&gt;

</pre>

The structure uses a wrapping table with `width:100%` and 3 columns, two 'spacer' columns and one in the middle for the email content. Putting the main content in the middle column and setting a width on that column's `<td>` will center the content within the email clients container.

The content then contains a series of nested tables which build the header, footer and multiple content rows. As a general rule it is best to make sure that each row within the email uses just one column for full width content and 3 columns for centered content.

Standards
----------------------------------------------------------
This template uses a few standard rules for it's structure which have all been adopted from various standards inspired from resources shown below.

<strong>1. Nest your tables</strong> <br/>
Every row should contain either 3 or 1 column and the content within must be wrapped inside a table. This isolates the default layout so the number of columns/rows & width settings will only be relevant to that piece of content (it's own table).

<strong>2. Header styles and inline styles</strong> <br/> This template comes with a few styles in the `<head>`, they are all fixes/hacks for particular email clients. Avoid writing any new styles in the `<head>`, instead do all of your element styling <strong>inline</strong>, you'll see below that all text elements are wrapped in a `<span>` tag, you could use another tag but I find this to be the safest as it has no default styles.

<strong>3. No margin or padding</strong> <br/> Avoid using any `margin` or `padding` declarations as email clients render these very differently (or not at all). The best way to get around this is to use a nested table with spacing rows/columns by settings the the `<td>` width or height attribute.

<strong>4. Images</strong> <br/> When adding images to your email make sure you add the `border="0"` attribute when wrapped inside an anchor. Always add the `"display:block"` inline style and define the width and height attributes of the tag according to the image natural dimensions.

<strong>5. Text styles</strong> <br/>
All text elements have a few standard styles:
- font-size(px)
- line-height(px)
- font-family(web safe)
- colour(6 digit hex code)

Using these four styles on every text element ensures consistent rendering on  all major email clients. In addition make sure that you add an inline clolour style to anchor tags separately as some clients will overwrite
any colours set from wrapping elements.

Resources
----------------------------------------------------------
These are some resources I refer to when building HTML emails:
- http://www.campaignmonitor.com/resources/will-it-work/guidelines/
- http://www.campaignmonitor.com/css/
- http://24ways.org/2009/rock-solid-html-emails/
- https://litmus.com/blog/16-tips-troubleshooting-html-email

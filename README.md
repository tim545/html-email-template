HTML Email Template
===================

A template for creating HTML email's which will render consistently across major email clients. It's designed to reduce time by providing common layouts which can reused.


This file contains a basic HTML email structure with 
common fields and rows which can be reused
to reduce build time and ensure email client compatibility.

Structure
----------------------------------------------------------
The template follows this basic structure:
(inline comments have corresponding names for the sections)

<pre>

&lt;wrapper&gt;
  &lt;content&gt;
        &lt;/ header&gt;
        &lt;/ content row&gt;
        &lt;/ content row&gt;
        &lt;/ content row&gt;
        &lt;/ footer&gt;
    &lt;/content&gt;
&lt;/wrapper&gt;

</pre>

The structure uses a wrapping table of 100% width to put 
the content table in the center of the page. The content
then contains a series of nested tables which build the
header, footer and multiple content rows.

Standards
----------------------------------------------------------
This template uses a few standard rules for it's code
which have all been adopted from various standards
available from resources online.

<strong>1. Nest your tables</strong> <br/>
To avoid going crazy and prevent email clients from
applying their own resizing to your rows and columns
always use nested tables and NEVER user "colspan" or
"rowspan", keep it simple.

<strong>2. header styles and inline styles</strong> <br/>
This template comes with a few styles in the <head>,
they are all fixes/hacks for particular email clients
so don't remove them, but at the same time don't add to 
them either unless you have to add another fix. Make sure 
you do all of your element styling INLINE, you'll see below 
that all text elements are wrapped in a <span> tag, you 
could use another tag but I find this to be the safest as it 
has not default styles. Each one has all of it's styles
set on itself, forcing an overwrite to any other styles
that may be applying to it.

<strong>3. No margin or padding</strong> <br/>
You find any CSS margin or padding decleratrions here,
email clients render these very differently (or not at 
all). The best way to get around this is to use a nested
table with spacing rows/columns.

<strong>4. Images</strong> <br/>
There are no example images here, but when you add some
make sure you add the border="0" attribute when wrapped in
a link. Always add the "display:block" inline style, and
define the width and height of the image in the imagaes
attributes.

<strong>5. Text styles</strong> <br/>
All text elements have a few mandatory styles set:

- font-size(px)
- line-height(px)
- font-family(web safe)
- colour(6 digit hex code)

Using these four basic styles on every text element ensures 
a consistent rendering of text on just about all email 
clients. Make sure that you add an inline clolour style
to &lt;a&gt; tags seperately as some clients will overwrite
your colour setting.

References
----------------------------------------------------------
These are a few of the resources I refer to when building
HTML emails, and alot of the standards I use for emails
have come from these.
- http://www.campaignmonitor.com/resources/will-it-work/guidelines/
- http://www.campaignmonitor.com/css/
- http://24ways.org/2009/rock-solid-html-emails/
- https://litmus.com/blog/16-tips-troubleshooting-html-email

I also keep all of my favorite resources in a Kippt
- https://kippt.com/tim545/html-emails

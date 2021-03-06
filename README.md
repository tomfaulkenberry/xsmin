xsmin: A Minimalist Beamer Theme
================================

This is a beamer template that is based on David Dumas' `xsmin` template, which was derived from "Execushares" by Kenton Hamaluik (http://hamaluik.com/posts/better-beamer-themes/). 

Mainly, everything is the same, but I changed the color theme to reflect the official colors of my university (Tarleton State University).  Other university colors can be used as well, either by editing lines 14-18 of the global style file `beamerthemexsmin.sty` or by editing lines 14-18 of the local `.tex` file. 

Status
------

This template is a work in progress and the current version has many
known issues.  Use at your own risk.

Note (11/16/2016): in order to compile in Emacs, one will need to set XeTeX as the default TeX engine.  The easiest way I've found to do this is the following:

* type M-x customize-variable
* type TeX-engine
* select Value Menu and choose XeTeX
* select "Apply and Save"

In my experience, this is a bit easier than directly editing any of the Emacs customization scripts!


Requirements
------------

* xelatex
* Beamer
* tikz
* Note: David's original xsmin used the Adobe fonts below, but I have removed the dependency for now
* ~~Adobe's "Source Pro" Fonts (free):~~
    * ~~[Source Serif Pro](http://store1.adobe.com/cfusion/store/html/index.cfm?store=OLS-US&event=displayFontPackage&code=1966)~~
    * ~~[Source Sans Pro](http://store1.adobe.com/cfusion/store/html/index.cfm?event=displayFontPackage&code=1959)~~
    * ~~[Source Code Pro](http://store1.adobe.com/cfusion/store/html/index.cfm?store=OLS-US&event=displayFontPackage&code=1960)~~

Quick start
-----------

In the linux terminal, a typical command to compile the sample
presentation would be

`xelatex sample.tex`

producing as output `sample.pdf`.

To use xsmin with your own presentation, use documentclass `beamer`
and add the command

`\usetheme{xsmin}`

to your document preamble.  Also copy `beamerthemexsmin.sty` to the
directory containing your tex file, or place this style file in the
xelatex search path.

Known issues
------------

* The title slide is drawn over top of whatever is on slide 1, even if
  that slide is not designated as the title slide.
  
* The square bullets for enumerated or itemized lists do not have the
  correct vertical alignment if a larger font size is used.
  
* The contact info slide in the sample presentation is sometimes not
  rendered correctly.  Recompiling the presentation seems to fix this,
  but the cause is unknown.
  
 * The title slide, frame title, and contact info slide are not beamer
   templates (as they should be), but instead are drawn manually after
   instructing beamer to create a suitable blank area on the slide.


Contributors
------------

Tom Faulkenberry <tomfaulkenberry@gmail.com>

David Dumas <david@dumas.io>

The Execushares theme (from which this one was derived) was created by
Kenton Hamaluik.

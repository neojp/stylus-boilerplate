# My personal Stylus boilerplate #

* Has a custom build task written on [Cake](http://jashkenas.github.com/coffee-script/#cake): `cake build`
* Uses a custom version of [normalize.css](http://necolas.github.com/normalize.css/)
* Uses vendor a gradient modules from Stylus' [Nib framework](http://visionmedia.github.com/nib/)
* Default [WordPress CSS classes](http://codex.wordpress.org/CSS)

* Default values for:
  * **border-radius:** 5px
  * **box-shadow:** 0 0 5px rgba(0, 0, 0, 0.10)
  * **text-shadow:** 1px 1px 1px rgba(0, 0, 0, 0.25)
  * **transition:** all 0.150s linear
  * **transition-property:** all
  * **transform:** translate3d(0,0,0)
  * **white-space:** pre-wrap

* Default mixins for:
  * Image replacement: **ir()**
  * Hidden elements: **hidden()**
  * Visually hidden elements: **visuallyhidden()**
  * Invisible elements: **invisible()**
  * Disable text selection: **noselect()**
  * No markup floats clearing technique: **clearfix()**
  * Forced reset margin: **nomargin()**

## Installation ##
Stylus & Nib are required

    npm install -g stylus nib

Compile your *.styl files using the Stylus executable

    stylus -u nib site.styl

Or compile it using the [Cake](http://jashkenas.github.com/coffee-script/#cake) task

    npm install -g coffee-script
    cake build

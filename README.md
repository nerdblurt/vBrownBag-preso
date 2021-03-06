vBrownBag-preso
==========
luigi Test Pull
My revelator-based presentation for the vBrownBag podcast

the Revelator (by [mpdehaan](https://github.com/mpdehaan/revelator))
=============

Who's That Writin' Reveal.js Slide HTML?

Not me.

Relevator generates Reveal JS presentation decks from simplified (and easier to edit) YAML files.

Various things may be rough here and features are being added as they are needed, and I'm ok with that.
Pull requests will be entertained.

Background
==========

Reveal.js is a pretty awesome framework for generating web-based slides.

This is what Reveal.js looks like: http://lab.hakim.se/reveal-js/#/

HTML you write typically looks like: https://github.com/hakimel/reveal.js/blob/master/index.html

Except with Revelator, you can write simpler things like: https://github.com/mpdehaan/slide-the-revelator/blob/master/test.yml

Which is more the way I want to compose and tweak slides.


Usage
=====

    chmod +x write_it
    vim test.yml
    write_it test.yml my_presentation_directory
    sensible-browser my_presentation_directory

Supported Reveal.js Features
============================

- Setting the Title, Author, and Description
- HTML tags via shorthand
- Class notes
- Nested slides
- Changing background colors
- Changing transitions
- Images
- Hyperlinks
- Formatted Code Blocks
- Ordered and Unordered Lists
- Blockquotes

Helpful Syntax
==============

set_global options:
- fragment
    + true
    + false
    + grow
    + shrink
    + "roll-in"
    + "zoom-in"
    + "highlight-blue|green|red"
    + "highlight-current-blue|green|red"
    + "fade-out" +/- "-visible"
- transition
    + linear
    + concave
    + zoom
    + cube
    + page
    + fade

Writing actual slides: 
- Each starts with a `-` line, then tab in (see examples)
- `h1-h5: *words words words* `
- `p: *words words words* `
- `image: 'https://image.com/url.jpg'`
- `link: [ 'Ansible', 'http://docs.ansible.com' ]`
- `ol:` for an ordered list, following by items indented below
- `ul:` for an unordered list, followed by items indented below
- `nested:` to begin a nested series, then indent below it like a new slide
- `- code: |` followed by lines of code underneath (*note:* the syntax is different here. No `-` on lines, just write the code itself)

    
  
License
=======

GPLv3

Author
======

Michael DeHaan - Original author  
Matt Brender - This presentation

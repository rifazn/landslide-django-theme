Django inspired theme for Landslide
================

A themes for Landslide (https://github.com/adamzap/landslide) that is inspired from Django's website color palette.

Themes
------

  - __simple__: modification of the Landslide default theme
    - no gradient
    - Fira Sans as font
    - improved bullet style
    - no round corners
    - django color palette

Demo
----

![Demo](https://gfycat.com/frequentampleboar)

That slide is made using this markdown:

    !markdown

    # hi!

    ---

    # Demo for Django inspired Landslide theme

    This is your very own presentation created using markdown!

    _Very cool!_

    Lets go to the next slide.

    ---

    # Displaying lists

    Listing important stuff:

    1. Filler text
    2. Lorem ipsum
    3. Filler text
    4. Dolor sit
    5. Last Item.

    End of slide, marked using "---".

    ---

    # Bullet list with a footnote

    I have bullet points:

    - Lorem
    - Ipsum
    - Dolor

    Note: the footnotes

    1. reddit.com
    2. ubuntu.com (Arch better btw?)
    3. wikipedia.org

    .fx: footnote

    ---

    # Images

    ![Elon High](https://goingconcern.com/wp-content/uploads/2018/09/Elon-musk-blunt.jpg)

    ---

    # Main heading
    ## Subheading

    Sadly, haven't themed tables yet.

    ---

    # Landslide

    Check out landslide [(https://github.com/adamzap/landslide)](https://github.com/adamzap/landslide). It lets you create this nice presentation by just using markdown.

    ---

    # FIN


Notes
-----

Some notes which might have nothing to do with the themes.

### Rearranging slides

The only Powerpoint feature that I like is being able to conveniently reorder slides.
Well, you can do the same in Vim+landslide, just give your slides meaningful titles
(this you need for the table of contents anyway) and use folding to reduce them to single lines,
i.e. add something like this to your `.vimrc`.

    function MarkdownLevel()
      let h = matchstr(getline(v:lnum), '^#\+')
    	if empty(h)
    		return "="
    	else
    		return ">" . len(h)
    	endif
    endfunction

    au BufEnter *.md setlocal foldexpr=MarkdownLevel()
    au BufEnter *.md setlocal foldmethod=expr

(The code originates from <http://stackoverflow.com/questions/3828606/vim-markdown-folding#comment16309004_4677454>.)

Toggle folds by `za`, reorder slides by reordeing lines in the usual way.

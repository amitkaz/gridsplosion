# Gridsplosion

Extensible responsive/fluid/sass grid system based on [csswizardry-grids](http://csswizardry.github.com/csswizardry-grids)

## Enhancements / Decisions

* Using numbers instead of words (desk-2-6 instead of desk-two-sixes).
* Grid explosion & media queries via functions- easily extensible.
* Addition of 16, 24 grids.
* Addition of visible/hidden imitating bootstrap.
* Media queries via phone, device (phones+tablets), laptop, desktop.
* Changing font size percentage for media queries.
* Using sass silent-classes by default (as the explosion generates *a lot* of classes)
* Using em/percentage for spacing

## Basic usage

html:

    <div class="navigation" />
    <div class="page">
            <div class="main" />
            <div class="side" />
    </div>


Sass:

    .navigation { @extend %phone-hidden; }
    .page { @extend .grid; }
    .main {
      @extend .gi;
      @extend %s-2-3;
      @extend %phone-full;
    }
    .main {
      @extend .gi;
      @extend %s-1-3;
      @extend %phone-full;
    }

* Will hide navigation on phones
* Will make the side below the main on phones
* Will make the main twice as big as the side (side by side) on everything else

## Motives

* I wanted to play with semantic/responsive/fluid grid system for [RiddleDribble](http://riddledribble.com)
* Found [Responsive grid systems; a solution?](http://csswizardry.com/2013/02/responsive-grid-systems-a-solution/)
* Harry choose the path of numbers-as-words (which I find too verbose) and gave his blessing to fork the project to change it.
* On the way I've changed the scss to be more "codeable", and added responsive font sizing from [handling-typography-responsive-design](http://www.netmagazine.com/tutorials/handling-typography-responsive-design)

## Todo

* Make it mobile first by default?
* Check usage of floats/margins instead of inline-blocks/padding

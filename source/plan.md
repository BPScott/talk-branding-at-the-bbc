* ITV summary
* BBC programmes summary
* Separation of concerns in css - components / layout / theme
  * Theme is what we're focusing one
* Design Systems - creating common names for conventions
  * Typography heading names
  * stock common colors - iPlayer pink, news red, sport yellow, share tools green
  * common colors - page primary, secondary, highlight
  * Simplifies interaction with design team
  * Now you've got a name for these items, you can make variables for them
  * and then you can change the content of these variables
  * thus you can build a new color schemes


* Building Design systems in Sass (ITV)
  * variables
  * new theme files that change those variables for every site

* But that doesn't work for BBC
  * Not got the time to build new a new theme for everything
  * So it can't be the responsibility of the devs to create themes
  * Need to write a tool for editorial staff to generate themes

* What is a BBC theme?
  * CSS colors
  * Masthead
  * Application agnostic, can be used in progs / events / playlister

* BBC Branding v1
  * Custom CSS preprocessor using JIT parsing on page-load
  * Devs wrote CSS that referenced theme variables
  * Complex build process that intertwined app and theme css
  * Only support 'programme' masthead
  * Process was arkward and non-standard, meant devs couldn't use more well
    established preprocessors

*  BBC Branding v2
  * Defines br-* classes that defines boxes and custom classes
    * boxes define text, background and link colors for an area
    * helpers lets people fix colors on a defined property
  * Defines multiple variants - programme, event
  * Logic is split
    * Global variables
    * Per-breakpoint variables
    * Per-variant variables
  * A particular theme version can be long-cached


* Example of Branding v2
  * Webservice that returns a json file that returns:
  * Two blocks:
    * head block, contains <link> to css
    * masthead block, contains masthead contents


* TL;DR
  * Create a design system
      * Standard language to define common patterns helps even if you're only
        making one brand
    * Sass is great at abstracting these ideas
    * Colors has html classes is a neat idea but you almost certainly don't
      need to go that far (typography however is totally suited to this)

* Link Dump
  * Guardian type and color systems?

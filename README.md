LilyLibrary
============

LilyLibrary is a collaborative space for the creation of new Lilypond tools,
including snippets, templates and extensions.

The main motivation for this project is to offer solutions to a number of
constraints that are present in the long-standing
[Lilypond Snippet Repository](http://lsr.dsi.unimi.it/), in particular:

 * Support for up-to-date Lilypond versions (LSR is still limited to version 2.14.2);

 * Support for multi-file Lilypond extensions and special scripts;

 * Easy collaboration and version control via [Git](http://git-scm.com/).

Besides its role as a repository of contributed tools, LilyLibrary can also serve as
a testing ground for developing and refining new functionality that may be suitable
for Lilypond proper, just as the Boost libraries serve as a testing ground for potential
new functionality in the C++ standard library.

A possible future extension of LilyLibrary is the development of a nice web frontend
for browsing the repository, which could enable integration with official Lilypond
documentation in a similar manner to the LSR.


Using this repository
=====================

The best way to download and use Lilylibrary is to clone the repository to your own
computer using [Git](http://git-scm.com/).  This will enable you to easily keep your
copy of the repository up to date by running the ```git pull``` function.  If you need
help with Git, you can try reading the [Pro Git book](http://git-scm.com/book), or
[contact us directly](README.md#contact) for advice and assistance.

If you don't want to use Git, or you just want to use one or two of the tools provided
in LilyLibrary, you can view the files in your browser by clicking on their names, and
simply copy-and-paste the code into your text editor. You can also
[download](https://github.com/openlilylib/snippets/archive/master.zip)
the whole repository in a ZIP archive.  This is recommended for casual use.

Most snippets are divided into an `.ily` file with function definitions and a `.ly`
file showing a usage example.  To use the functions provided by the snippet, simply
`\include` the `.ily` file into your score.

You can make the root directory of the repository available to LilyPond by using the
`-I` or `--include=` command line option (or, if you use Frescobaldi, add the path in
_LilyPond preferences_).  Then you will be able to `\include` the snippets with a path
relative to the repository root directory: for example,
`\include "debugging-layout/display-grob-anchors/definitions.ily"`
will allow you to use `\printAnchors` function defined in the snippet.


Contributing
============

What's eligible?
----------------

Anything that is useful and isn't totally obvious is welcome in LilyLibrary.
As a rule of thumb, anything over 20 lines of code is probably worth submitting.

**You can also contribute work in progress** and update it later.


How to contribute
-----------------

The easiest way to contribute is using GitLab's web interface.

 1. Create an account on [GitLab](http://gitlab.com/) and log in to it.
 2. Go to the LilyLibrary [GitLab page](https://gitlab.com/lilypond/lilylibrary).
 3. Click "Fork" to create your own personal clone of the LilyLibrary repository.
 4. To modify a file, click its name and then click _Edit_.
 5. Write what you have changed (form at the bottom) and click _Commit_.
 5. Click _Send pull request_ to submit your changes to LilyLibrary
    ([more info...](meta/contributing.md#pull-requests))

Alternatively, you can clone the repository to your local machine for offline
editing before pushing back to your GitLab account and submitting a pull request.
See [GitLab Workflow](https://gitlab.com/help/workflow) and [contributing with
advanced tools](meta/contributing.md#contributing-using-advanced-tools) for more
information.


Guidelines
----------

_Note: detailed guidelines are in [`meta/contributing.md`]
(meta/contributing.md)(optional reading)._

 * Your snippet must compile (even if it's work-in-progress) and it must contain
   a `\version` statement.

 * Please use a template from [`meta/snippet-templates`](meta/snippet-templates)
   as your starting point.

 * Simple snippets that just demonstratea functions, engravers etc. that can be
   useful on their own should use the "includable" template.

 * If possible, please format your code using Frescobaldi's _Format_ tool.

 * When you make changes in your snippets, please contribute updates back to
   the LilyLibrary repository! :-)


Snippet categories
==================

* [__custom-music-fonts__](custom-music-fonts) -
    alternative fonts for LilyPond, that can be used instead of default Feta.
* [__debugging-layout__](debugging-layout) -
    tools that visualize LilyPond's layout decisions (e.g. directions),
* [__general-tools__](general-tools) -
    stuff for working on and with LilyPond itself.
* [__input-shorthands__](input-shorthands) -
    music functions and other tools that make writing LilyPond code easier,
* [__notation-snippets__](notation-snippets) -
    LilyPond code that produces some particular notation,
* [__simple-examples__](simple-examples) -
    snippets that are just explaining or demonstrating things from the documentation,
* [__specific-solutions__](specific-solutions) -
    hacks that aren't generic, just solve a very specific problem,
* [__stylesheets__](stylesheets) -
    a place for collections of user-designed layout settings ("house styles"),
* [__templates__](templates) -
    examples showing how to structure LilyPond code.

Every category has a `README.md` file inside with more details, but if you're not sure
which category to choose, don't worry!  It's not that important and can be decided when
your submission is being reviewed.


<!---
Later on, we may divide the snippets into 2 (or more)
"quality levels":
- official ones, showing Recommended LilyPond Practice,
- drafts, hacks etc. that were just written by someone
  and may be useful, but may also not be.

The policy would be to allow anyone to add anything to the "hacks",
but adding/changing official ones (or moving a draft to official ones)
would require some confirmation from someone else (not necessarily
a full review, but at least a quick look).

Update: actually, the status field probably already does this.
-->

Contact
=======

Have trouble contributing?  Let us know!
[info@openlilylib.org](mailto:info@openlilylib.org)
[janek.lilypond@gmail.com](mailto:janek.lilypond@gmail.com)

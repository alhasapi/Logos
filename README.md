# Logos
Logos is an upcoming with web-extension which tries to make browser automation easy to regular users.
Our goal is to automate as much as possible in order to minimize human intervention. 
The software is expected to function on standard browsers namely firefox and
chrome or chromium.  Most of these operations are performed on forms (form filling). For the
sake of genericity the code might function as a framework, a collection of composable pieces
of software which gives to its users the ability of craft new behaviours programmatically on
the same language of that the software have been produced.

An earlier implementation of these ideas have been produced for specific web pages which requires
at least, to rewrite everytime the code in order to fit new mutations of the pages (ids changes,
some names too etc..). An other limitation of that old version was that, the core software was
splitted into two parts written both in different languages(python & javscript). The former was
parse and preprocess data expected to be submitted to be page to be used while the latter was
working directely on the page.

Furthemore, the javscript part relies on a thirth party application, a code injector.
Its role is to inject the required javascript code which performs the programmed specifcations
one the page. The first design decision will be to merge conceptually these two parts into one
implementation in javascript. The challenge will be to reach a good enough genericity in order
to avoid the code to be rewritten every time there are changes on the pages.

We also expect the software to have a GUI, for configuration, for defining a priori, ways to map data
to the page, or overseeing the progression of tasks, and the loading of data from the filesystem. The
main component of the software is the dom-analyser, which function is to collect relevant items on a
page. One simple operation on a page would be a cold reading of existing data and an eventual exportation
of the data in multiple formats. The remaining set of operation is form-filling, various HTML tags are
targeted here: selects, checkboxes, inputs and text-like tags (paragraphs, bold, italic, code etc...).

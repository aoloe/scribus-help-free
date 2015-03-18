# The Scribus free help files

A set of Scribus help files that are under a free license and can be included in Linux distributions.

The main goals of this project are:

- produce a full help of Scribus
- that is easy to translate
- that is more concise than the current documentation
- that is free (cc-by-sa)

## Concept

Content: 

- focusing on what the user are looking for rather than on documenting every detail.
- we should try to stick to providing help on how to use Scribus and, where it's possible, avoid to disgress and start teaching the user the good habits in DTP (those should be in a separate manual...).
- we should probably start with a basic structure and content and then create a "1.4" branch and keep the master for the development version.

Form:

- one directory per help page.
- each directory contains all the files used to display the page in the different languages.
- text formatting uses markdown.
- english is the default language (no language code) but the work can start in any language.
- translations are post fixed with a 5 letters language code (`this-page.de_DE.md`)
- images also can have a language code.
- we will provide a script that convert the markdown file and produces the file structure requested for the help files.
- each directory should have a `README.md` file with notes on the page.
- if Qt supports it, we should use animaged GIFs to improve the explainations (and keep them short). Cf. the Inkscape manual.

The result will be available as epub, website, and Scribus help files.


## A warning

Please, don't copy content from the official Scribus Help files! The licenses are not compatible!  
On the other side, you might get inspiration from the Scribus Flossmanual: <http://en.flossmanuals.net/scribus-2/>

## FAQ

- Why this is not in the Scribus Wiki?
  - We would like to have a redactional team and at the same time being open to all contributions: this is easier to achieve with the "fork / branch / pull request" model than a Wiki.
  - We would like to produce a multilingual and structured work following some guidelines... not really the main focus of a Wiki...

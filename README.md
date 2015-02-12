# scribus-help-free

Set of Scribus help files that are under a free license and can be included in Linux distribution.

The main goals of this project are:

- produce a full help of Scribus
- that is easy to translate
- that is more concise than the current documentation
- that is free (cc-by-sa)

Ideas:

- one directory per help page
- each directory contains all the files used to display the page in the different languages
- work with markdown files
- english is the default language
- translations are post fixed with a 5 letters language code (`this-page.de_DE.md`)
- images also can have a language code.
- provide a script that convert the markdown file and produces the file structure requested for the help files.
- each directory can have a `README.md` file with notes on the page.

Warning: please, don't copy content from the official Scribus Help files! The licenses are not compatible!  
On the other side, you might get inspiration from the Scribus Flossmanual: <http://en.flossmanuals.net/scribus-2/>

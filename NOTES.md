# Notes

## html output

show a keyboard key with kbd
~~~
kbd {
    background-color: #f7f7f7;
    border: 1px solid #ccc;
    border-radius: 3px;
    box-shadow: 0 1px 0 rgba(0, 0, 0, 0.2), 0 0 0 2px #fff inset;
    color: #333;
    display: inline-block;
    font-family: Arial,Helvetica,sans-serif;
    font-size: 11px;
    line-height: 1.4;
    margin: 0 0.1em;
    padding: 0.1em 0.6em;
    text-shadow: 0 1px 0 #fff;
    white-space: nowrap;
}
<kdb>ctrl</kbd>
~~~

## content to be added

- footnotes
- marks
- table of contents
- non dtp work:
  - interactive PDFs
  - epub
  - mail merging
- render frames
- units: ""just for your information: generally speaking i would not suggest you to work with cm. mm are -- generally speaking -- a better unit. i would also avoid pt.  
  if you have to define some units in pt, i would suggest you to type them as is in the box and they will be automatically converted by scribus into the current unit. this works with most if not all measurement boxes.
- add a section: "common errors, failures and bugs"
  - Spell checking does not work: Check your preferences under Spelling (Hyphenation and Spelling) and see if it points to your /usr/share/myspell/your_language (en_US in my case) and check in fact that it is there.
- page background color:
  - La couleur de fond indique la couleur du papier utilisé : exemple jaune, tu imprimes sur du papier jaune. Mais tu n'imprimeras pas la couleur jaune, donc elle ne sera pas reprise dans la sortie. Pour le noir, c'est pareil. Pour imprimé un fond coloré tu mets une forme noire sous ton document et sur chacune des pages.
Avec les calques et les modèles, c'est rapide.  
Ne pas oublier de paramétrer les bords perdus pour éviter les mauvaises surprises à la sortie. (brunod sur linuxgraphic.org/forum)
- master pages: you can create a master page based on the current page (?). a master page is part of a scribus document. when you create a new document, you may import a masterpage from another document. (the third icon in the 'edit master pages' window…) (utnik, scribus/forum)
- standard/repetitive content: r fenton asks on the mailing list: "In the book I am writing, almost all of the pages will look exactly the same - an image frame in the upper right corner (for Right pages, the opposite for Left pages) with text flowing around it."  
  ale's answer:  
  the easiest way to do this, is to create two master pages (L, R) wit the guides that define the places where you want your frames to be.  
  then you have to ways:
  - after having selected the text / image frame tool, with shift-click you can insert a frame that fills, the space up to the surrounding guides (or page margins). that's quite fast.
  - or you can put sample frames, with different styles and positions (and dummy text) in the scrapbook and double click on the matching item to get it inserted at the position it originally was. you can also put groups in the scrapbook.
  i would avoid the automatic frame creation, except if you plan to have many pages (more than 30) that all look the same and have the text flowing from one page to the next.  
  the script automation is fine if you have really lot of pages... or you like scripting your work (like i do :-)
- gregp said: "In DTP, the most important person to satisfy is yourself, as far as the results are concerned. After that, you're mostly looking for efficient workflow."
- setup the user interface:
  - choose the UI language
  - choose the measurement unit (inch or mm)
  - always maximise the scribus window (except if you have a very large monitor)
  - show the Properties Palette and put it on the right side of your document (in 1.5 it can be docked) and learn the F2 key to show and hide it. Refrain from moving it from keeping moving it around.
  - hide all the toolbars but the tools one and dock it to the left side.
  - setup the hyphenation
  - disable showing the startup dialog (mostly you're faster by typing ctr-o and ctr-n to open or create a new document)
  - enable snapping 
  - set ctrl-shift-p for producing a pdf and ctrl-alt-p for switching the preview mode
  - set the Preflight verifier to check for the most common PDF version for you. if in doubt choose 1.4 (really?).
-  should be i add a book on working with scribus, as an example with a list of software that can be used with it or places where you can find ressources (like images and co)?
- what if...
  - i need the same content on many pages
    - use master pages for the fixed content
    - the scrapbook for editable contents
    - use multiple duplicate
  - i cannot edit the item
    - you cannot edit items that are from a masterpage
    - the item could be locked
    - you're not on the right layer
  - i cannot click on the item
    - if the item is behind another item, use the ctrl-key to click on the items below
  - i cannot upload my pdf to a printshop
    - check that all fonts are embedded
    - check that you chosed the correct PDF version in the preflight verifier
    - check that you're producing the PDF version the print shop is requesting from you
    - only use transparencies (PNGs with transparent background, gradients) if you're sure that the print shop supports them and process them correctly (if you don't have any warning when using PDF 1.3 in the preflight verifier, you don't have transparencies in your document)
    - for pdf/x documents read https://en.wikipedia.org/wiki/PDF/X (generally, read the matching article on wikipedia... and we should provide a list of links)
    - a nice link in german: https://wiki.piratenpartei.de/Druckerzeugnis
  - scribus slows down
    - if you have huge images, try to lower the display resolution (prefs or settings)
    - use two directories with `images/` directories: `images-high` with full-res images and `images` with low-res ones with the same name. when preparing a pdf, close the document, rename the two directories and reopen the document.
- have a look to http://www.cgemy.com/galerie/docs/AideMemoireScribus.pdf 

## building an index

before each title we can put an html comment with index commands in it:

    <!-- index: text frame; loading text; word; ODT; DOC -->
    # Loading text

We can then collect all the indexes and replace the comment with a `<a name=""></a>` inside of the title.

## Table of contents

non, scribus n'a pas façon de créer une table des matière basée sur les styles.

il y a façon de créer une table des matière automatique, mais vous ne voulez pas savoir comment ça marche.
c'est une perte de temps et on est plus rapide à la main.

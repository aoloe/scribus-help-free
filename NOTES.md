# html output

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

# content to be added

- footnotes
- marks
- non dtp work:
  - interactive PDFs
  - epub
  - mail merging
- render frames
 
# building an index

before each title we can put an html comment with index commands in it:

    <!-- index: text frame; loading text; word; ODT; DOC -->
    # Loading text

We can then collect all the indexes and replace the comment with a `<a name=""></a>` inside of the title.

# LaTeX Cheatsheet

** Note ** : These are my most used latex commands so it may lack some of the
more "*common*" ones if I dont use them.

### Document initialization and document options

##### Start a document

```
    \begin{document}

        ...Content...

    \end{document}
```

##### Document Classes

```
    \documentclass[option,option..]{class}
```

The clases available for a default Latex document are :

* book
* report
* article
* letter
* slides

Documentclass options :

* {number}pt (10pt, 11pt ...) : Font size
* Paper size
    * letterpaper
    * a4paper
* landscape
* draft

##### Most used packages

```
    \usepackage[options...]{package}
```

* inputenc : Sets the document encoding `\usepackage[utf8]{inputenc}`
* babel : Sets the document languague `\usepackage[spanish]{babel}`
* graphicx : Allows the user to insert images and graphs
* hyperref : Allows the user to add inner and external links on the document
* anysize : Changes the margins `\marginsize{l}{r}{t}{b}`

##### Titles and general information

** Note ** : These go before the `\begin{document}` tag.

* `author{text}`
* `title{text}`
* `date{text}`

Once these are set the tag `\maketitle` can be used within the document body.

* `\tableofcontents` : Adds a table of contents that reads the document and updates
if necesary.

##### Document structure

The following tags add structure to the document and are readed by the
`\tableofcontents` tag.

* \part{title}`
* \chapter{title}`
* \section{title}`
* \subsection{title}`
* \subsubsection{title}`
* \paragraph{title}`
* \subparagraph{title}`

If used any of the previous tags with the `*` modifier those will not appear in
the table of contents `\section*{title}`


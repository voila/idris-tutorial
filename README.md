# The Idris Tutorial

This a copy of the main `Idris` tutorial taken from [idris-dev].

## idrislang.sty

`idrislang.sty` is used to type set `idris` code within the tutorials.
To keep things `DRY` this style file has been *hard* linked with the original kept in `idris-dev`.
Normally, this file should live in the your local texmf tree, but if we want auto-generation of PDFs then the style file needs to be distributed alongside...

## Building

The tutorial is written in `LaTeX` and the build tool `latexmk` will be used to manage the compilation process.
`latexmk` comes with the default texlive installation.
A nominal `Makefile` is provided that abstracts over the use of `latexmk`.
`Emacs` with `AucTeX-mode` is used during writing.
The `auto` generated by `AucTeX` should be taken care of with the `.gitignore`.
Ditto goes with those pesky `.DS_Store` files generated by Mac OS X.
However, do not be surprised to see several `AucTeX` related code in `LaTeX` comments at the bottom of several files.

Useful bash aliases for working with LaTeXmk instead of a Makefile are:

    alias latexBuild='latexmk -gg -pdf -pvc -bibtex'
    alias latexQBuild='latexmk -gg -pdf -bibtex'
    alias latexClean='latexmk -c'
    alias latexClobber='latexmk -C'


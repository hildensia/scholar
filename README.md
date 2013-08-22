This is a fork of www.icir.org/christian/scholar.html with some added functionality.

scholar
=======

Fetchs google scholar queries and outputs info or citation data


How to download a paper?
========================

Simply use the power of the shell:

wget $(python2 scholar.py "\<SEARCHTERMS\>" -c 1 | grep "URL" | sed "s/ *URL //")

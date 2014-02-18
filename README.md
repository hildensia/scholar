This is a fork of www.icir.org/christian/scholar.html with some added functionality.

# scholar

Fetchs google scholar queries and outputs info or citation data

## I get nothing but ```403 Forbidden```

The default of scholar is to fake a google id. Unfortunately that yields a ```403 Forbidden``` after a while. You can adjust the google id to your actual id by the following steps:

 * export the cookies.txt from your browser (needs an extension, e.g. https://addons.mozilla.org/de/firefox/addon/export-cookies/)
 * find the google-id cookie, its name is GSP=ID=
 * put your google id in line 305 instead of the fake one

## How to download a paper?

Simply use the power of the shell:

wget $(python2 scholar.py "\<SEARCHTERMS\>" -c 1 | grep "^ *URL" | sed "s/ *URL //")

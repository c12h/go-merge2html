# go-merge2html
This is a small command-line tool to generate all-in-one HTML files from .html files that use local .css and .js files.

Usage: `go-merge2html DEST-DIR  FILE.html ...`

For each input HTML file _F_, go-merge2html writes _DEST-DIR_/_F_, which is the same
except that any `<link rel=stylesheet href=STYLE.css>` element naming a local file is replaced by a `<style>`
element containing the text from that file, and
similarily any `<script src=SCRIPT.js>` is changed to a `<script>` element containing that Javascript.

Note that the file extensions must by `.css` and `.js` respectively, modulo case.

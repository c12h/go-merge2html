# go-merge2html
This is a small command-line tool to generate all-in-one HTML files from .html files that use local .css and .js files.

Usage: `go-merge2html  -dest-directory _DEST-DIR_  _FILE.html_ ...`
 where the `-dest-directory` (1) is required and (2) can be abbreviated as far as `-d`.

For each input HTML file _F_, go-merge2html writes _DEST-DIR_/_F_, which is the same
except that any `<link rel=stylesheet href=_STYLE_.css>` element naming a local file is replaced by a `<style>`
element containing the text from `_STYLE_.css`, and
similarily any `<script src=_SCRIPT_.js>` is changed to a `<script>` element containing a copy of `_SCRIPT_.js`.

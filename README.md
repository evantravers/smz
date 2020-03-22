# Simple Markdown Zettelkasten

Vim is an editor on top of the shell. If I write a shell script that can allow
me to search and manipulate my files, then vim integration _should_ be easy.

I was starting to write this in fish, but I'm going to move it to `sh` for
compatibility.

I may prototype in ruby/python, because that's what I'm used to.

## Generating IDs

Borrowing from ["Add Identity"](https://zettelkasten.de/posts/add-identity/),
we need a way to generate a unique ID based on the current date.

If you want copy this, you can use this string in an Alfred snippet:
`{date:YMdhms}`. The strftime format is: `%Y%m%d%H%M%S`.

We are simply using the built-in: `date +"%Y%m%d%H%M%S"`.

## Search

- [X] searching for tags `zkts`
- [X] finding content via full text search `zks`
- [X] finding a file by search of filename `zkf`

`fd` is perfect for this, although `find` is everywhere and adequate.

- [X] Files that link to this file
    - [ ] find files with no links (inbox?)

## Other

- [ ] note transformation: metadata, file name
- [ ] configuration:
    - [ ] notes folder(s)
    - [ ] tag style?

## Requirements

- fd
- rg
- multimarkdown

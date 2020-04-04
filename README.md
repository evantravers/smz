# Simple Markdown Zettelkasten: Shell Command

This is based on assumptions about the [format of a Simple Markdown
Zettelkasten](http://evantravers.com/articles/2020/03/13/simple-markdown-zettelkasten/),
which is itself based on [@ctietze's
work](https://zettelkasten.de/posts/baseline-zettelkasten-software-reviews/)

Vim is an editor on top of the shell. Following the unix philosophy as best as
I can, if I write a shell script that can allow me to search and
manipulate my files, then vim integration _should_ be easy.

## Configuration

To use `zk`, you are going to need to export `SMZPATH` somewhere in your shell
to tell it where to look.

## Subcommands

### Generating IDs

`id                          Generate a Zettelkasten timestamp`

Borrowing from ["Add Identity"](https://zettelkasten.de/posts/add-identity/),
we need a way to generate a unique ID based on the current date.

We are simply using the built-in: `date +"%Y%m%d%H%M%S"`.

### Search

`s|search [--tags] PATTERN   Find notes with content matching PATTERN"`

### Find

`f|find PATTERN              Find notes with name matching PATTERN`

### Backlinks

`b|backlinks TARGET          Find backlinks referencing TARGET`

## Requirements

- fd
- rg

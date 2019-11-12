# fzf-notes

This script was originally written by Casey Brant, and explained in his blog post [Simple Notes Taking with `fzf` and `vim`](https://medium.com/adorableio/simple-note-taking-with-fzf-and-vim-2a647a39cfa).

I've modified it to better suit my note taking style. It's designed for quick editing of a single notes directory. The file selector runs on a loop, wrapping `vim` opening the files. This allows you to jump in to quickly edit a file and then select a new one.

![demo](img/demo.png)

## Dependencies

- [`yq`](https://github.com/mikefarah/yq/)
    * `$ brew install yq`
- [`gnu-getopt`](https://formulae.brew.sh/formula/gnu-getopt)
    * `$ brew install gnu-getopt`

## Installation

```bash
$ git clone git@github.com:alichtman/fzf-notes.sh.git
$ cd notes.sh
$ chmod +x notes && mv notes /usr/local/bin/
$ cat "export NOTES='ABSOLUTE_FILE_PATH_TO_NOTES_ROOT_DIRECTORY'" >> ~/.zshrc
$ source ~/.zshrc
```

## Usage

Simply run `$ notes` from any directory. You may pass initial search terms like this: `$ notes searchterm1 searchterm2`.

You can create new files by selecting `CREATE_NEW_FILE` at the menu, but this is sometimes buggy.

## Configuration



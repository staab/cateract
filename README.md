This is a script for viewing files interactively. Inspired by [fzf](https://github.com/junegunn/fzf), which is an interactive cli file-picker.

[![asciicast](https://asciinema.org/a/413162.svg)](https://asciinema.org/a/413162)

# Usage

```
usage: cateract [-h] filename

An interactive cli file viewer

positional arguments:
  filename    The name of the file to view

optional arguments:
  -h, --help  show this help message and exit
```

Once in the interactive prompt, cateract pipes the contents of the file to an executable of your choice. Further redirection is not supported, as all arguments are shell-quoted. This allows something like `jq .|length` to work as expected without having to quote the argument manually.

# Installation

Make sure `python3` is a valid command on your system, then install:

```
mkdir -p ~/.local/bin
curl https://raw.githubusercontent.com/staab/cateract/master/cateract > ~/.local/bin/cateract
chmod +x ~/.local/bin/cateract
```

Then, make sure ~/.local/bin is in your path.

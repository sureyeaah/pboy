# PAPERBOY

![import screen](https://raw.githubusercontent.com/2mol/pboy/master/doc/import.png)

PaperBoy is a small .pdf management utility.

I was frustrated that most PDFs have pretty useless file names.

This tool helps to rename those files without too much fuss. It will rename/move files to a specified folder, and it even gives some suggestions for the filename by looking at the file metadata and the content.

PaperBoy aims to keep its file management dumb (no keeping files in a database or hidden library folder), so you can uninstall it at any time and your files will remain perfectly accessible.

# Usage

- Open a new file import dialog with <kbd>Space</kbd> or <kbd>Enter</kbd>.
- Switch between the library and the inbox with <kbd>Tab</kbd>.
- Open a file from the library with <kbd>Enter</kbd> or <kbd>Space</kbd>.
- Quit the application with <kbd>Esc</kbd> or <kbd>Ctrl + c</kbd>.

# Install

For now you need stack (cabal probably works too):

```
git clone github.com/2mol/pboy
cd pboy
stack install
```

This will give you an executable named `pboy` in your local bin folder.

# Config

PaperBoy creates a `.pboy.toml` in your home directory. Use this to change your library and incoming folders, as well as to specify whether you want to move the imported files or just copy them.

# Current Limitations

Consider this to be beta quality right now. Nothing in this tool will break your computer, but there is not a lot of exception handling for missing folders or missing utility programs.

Two command line tools are required for the suggestions: `pdftotext` and `pdfinfo`. Both come with the poppler package, which is available via homebrew on Mac or your distro's package manager on Linux.

For large files, `pdftotext` can take quite a long time to parse the document, which is stupid because we're only using the first couple of lines for file name suggestions.

# Contribute

Feel free to open issues, fix the Readme or send pull requests against the spec file https://github.com/2mol/pboy/blob/master/SPEC.md. You're generally very welcome to share any opinions, documentation improvements, fixes, refactoring suggestions etc.

See the abovementioned document to get an idea of what some of the next priotities are.

# Thanks

[`brick` is lovely](https://github.com/jtdaugherty/brick/).

The name for this tool is inspired by [this atrocity](https://en.wikipedia.org/wiki/Paperboy_(video_game)), which I had for the NES and never quite mastered.

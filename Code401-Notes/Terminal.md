# Practicing the Command Line

- [Bash Command Line Tutorials](<https://ryanstutorials.net/linuxtutorial/>)

## The Command Line

A GUI-less text-based interface to the computer system.
On a macOS, the command line can be accessed via the terminal, iTerm.
`echo $SHELL` will return the current shell being used... BASH (Bourne Again Shell, is most common)

## Basic Navigation

`pwd` will return the working directory that you are currently in.
`ls` lists the files and folders within the directory. Options can be added to this command to make it behave differently.

### Paths

The terminal uses 2 types: absolute and relative.

1. An ***Absolute Path*** specifies a location in relation to the **root** directory.
2. A ***Relative Path*** specifies a location in relation to where you currently are in the directory.

Understanding Paths

1. A tilde, `~`, is the shortcut for home directory, for example, `~/Documents`
2. A dot, `.`, references your current directory, for example, `./doc.txt`
3. A dotdot,`..`, references a parent directory, for example `../ ../`

You can change directories by using the `cd` command, for example, `cd ..`

## More About Files

- Linux does not use file extensions
- Linux is case sensitive
- Spaces in file names is o.k. but needs to be wrapped in single quotes
- The use of an escape charachter, the `\`, can be used to remove the special meaning of a particular charachter, such as, a space or apostrophe.
- File names that start with a dot, `.`, are hidden files and can be found in the listing using the `-a` option, for example, `ls -a`

## Manual Pages

Manual pages are accessed using the `man` command followed by the command to look up, for instance, `man ls`
To search the manual for a specific term, use `man -k <search term>`
When running commands, an option being called in longhand is preceeded by two dashes `--`
When running commands, an option being called in shorthand is preceeded by one dash `-`

## Manipulating Files

`mkdir [options]<Directory>` makes a directory
`rmdir [options]<Directory>` removes an empty file/directory
`touch [options]<filename>` creates a blank file
`cp [options]<source><destination>` copies the file from the source directory to the destination directory
`mv [options]<source><destination>` moves the file from the source directory to the destination directory. This command is also used to rename a file/directory.
`rm [options]<file>` will remove a file
`rm -r <file>` will remove all files and directories whether empty or not

# linux-notes

## Getting help

There is a hoarde of documentaion to be found on just about every part of a linux system.

First, manual pages should be available for anything on a system. If you develop software for linux, remember to make a manual. They are divided into sections based on what type of category of they fit. The manuals can be accessed as such:
- ```man man``` this is the manual for man, it is a good starting point for beginners because it explains how the sections work
- ```man <thing>``` where <thing> is the thing you want information on
- ``` man <section> <thing>``` when you know what section to search
- ```apropos <subject>``` where <subject> is a what you want information on but you do not know what man page to seek
- ``` man -k <subject>``` same as apropos
- ```man -a <thing>``` cycles through man pages that match <thing>. After quitting from one man page, a menu is presented (if more exist) where you can view the next manual, skip the next one, or quit the man viewer.

### Info viewer
Any software that is provided by GNU will probably also have a more comprehensive manual. You can access this by running ```info <command>```. The topics are arranged in a directory so if you want to browse to see what is available, ```info``` will get you to the top of the directory. Pressing ```d``` in any info topic will jump to the directory as well. If you ask info for a command that does not have an info topic, it will serve the man page instead.


## Bash and readline:
For help on bash, see ```man bash``` or ```info bash```.

By default, the bash shell is in emacs-mode exposing some emacs key bindings for line editing. These bindings can be extended by creating and modifying a user's readline init file. Alternatively, this behavior can be switched to enable vi style key bindings if preferred. For more info, see ```info bash``` section 8. Using emacs lingo, ```C-x``` is holding down the Ctrl key and pressing x, and ```M-x``` is holding down the Meta* key and pressing x. The Meta key is usually labelled ```Alt```, but can also be used by pressing and releasing ```Escape```. Sometimes ```Alt``` may not functioni correctly due to the terminal emulator. Yank means paste. Kill means cut.

Cancel:
- ```C-g``` abort search

Move command bindings:
- ```C-a``` move cursor to beginning of line
- ```C-e``` move cursor to end of the line
- ```C-f``` move cursor forward one character
- ```M-f``` move cursor forward one word*
- ```C-b``` move cursor backwards one character
- ```M-b``` move cursor backwards one word*

Kill and yank command bindings:
- ```C-d``` kill character at cursor point
- ```M-d``` delete to the end of the word from the cursor point
- ```backspace``` kill the previos character, is actually called ```delete``` in emacs terminology
- ```M-del``` deletes backwards from the cursor to the beginning of the word
- ```C-k``` kill (delete) all text from the point (cursor) to the end of the line
- ```C-w``` kill from cursor to previous whitespace
- ```C-y``` yank the previosly killed text to cursor point
- ```M-y``` rotate the kill ring and yank the new top, only if previous command was ```C-y``` or ```M-y```

History commands:
- ```C-r``` reverse search, enter a search pattern, you can use the command as-is or move the cursor to make changes
- ```C-p``` previous command
- ```C-n``` next command
- ```M-<``` move to first command in history
- ```M->``` move to last command in history

Undo:
- ```C-_``` or ```C-x C-u``` undoes the last edit, especially kill commands (e.g. delete word with ```M-d```) this supposedly can be repeated until there is a blank line left. my results have been mixed.
- ```C-u``` clears the line

More:
- ```C-l``` clear the terminal screen, same as typing clear

Modifier:
- You can use ```M-<numerical argument>``` to alter the above commands. For example, to delete 3 characters from the cursor, ```M-3 C-d```. This can be more than one digit or even a negative number can be passed as an argument by doing ```M-- <number> <command>```.


To edit a command in editor: ```^xe```

_How is this editor identified?_

```C-\``` sends SIGKILL when ```C-c``` fails to end a program. 

## Systemd

### Services
Edit a service file ```systemctl edit <service name>```

### Timers
To get a list of active timers: `systemctl list-timers`


## Shell

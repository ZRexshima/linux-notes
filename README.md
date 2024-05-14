# linux-notes

## getting help

There is a hoarde of documentaion to be found on just about every part of a linux system.

First, manual pages should be available for anything on a system. If you develop software for linux, remember to make a manual. They are divided into sections based on what type of category of they fit. The manuals can be accessed as such:
- ```man man``` this is the manual for man, it is a good starting point for beginners because it explains how the sections work
- ```man <thing>``` where <thing> is the thing you want information on
- ``` man <section> <thing>``` when you know what section to search
- ```apropos <subject>``` where <subject> is a what you want information on but you do not know what man page to seek
- ``` man -k <subject>``` same as apropos
- ```man -a <thing>``` cycles through man pages that match <thing>. After quitting from one man page, a menu is presented (if more exist) where you can view the next manual, skip the next one, or quit the man viewer.

### info viewer
Any software that is provided by GNU will probably also have a more comprehensive manual. You can access this by running ```info <command>```. The topics are arranged in a directory so if you want to browse to see what is available, ```info``` will get you to the top of the directory. Pressing ```d``` in any info topic will jump to the directory as well.


### bash and readline:
for help see ```man bash``` or ```info bash```
By default, the bash shell is in emacs-mode exposing some emacs bkey bindings for line editing.
- ```C-a``` move cursor to beginning of line
- ```C-e``` move cursor to end of the line
- ```C-k``` kill (delete) all text from the point (cursor) to the end of the line
- ```C-f``` move cursor forward one character
- ```M-f``` move cursor forward one word*
- ```C-b``` move cursor backwards one character
- ```M-b``` move cursor backwards one word*
- 

To edit a command in editor: ```^xe```
How is this editor identified?




### timers
To get a list of active timers: `systemctl list-timers`


## shell

# ksm-window

provides handy window management functions

## Why

I frequently find myself in a situation where I have half a dozen
Emacs windows in a frame, and I want to focus on just one of those
windows for a few moments, and then later return my window state to
its present configuration.  Emacs already has facilities for
accomplishing such tasks, but I wanted a quick toggle function like
tmux' "C-b z" pane toggling feature.

I put this file somewhere Emacs will find it, then added the below to
my ~/.emacs/init.el file.

```Lisp
   (require 'ksm-window)
   (global-set-key (kbd "C-x w") #'ksm/window-zoom-out) ;; restore frame layout from stack
   (global-set-key (kbd "C-x z") #'ksm/window-zoom-in)  ;; save frame layout, then zoom in to buffer
```

I also frequently find myself working with half a dozen buffers in as
many windows when interrupted to help someone else. I want to save my
entire frame layout, associated with a key word, then go help the
person who asked for it, and afterwards, quickly restore my frame
layout.

To do this, I add the following two more lines to my
~/.emacs.d/init.el file:

```Lisp
   (global-set-key (kbd "C-x j") #'ksm/window-config-restore) ;; prompt for NAME and restore config
   (global-set-key (kbd "C-x p") #'ksm/window-config-save)    ;; prompt for NAME and save config
```

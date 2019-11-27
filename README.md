# ksm-window

provides handy window management functions

## Setup

```Lisp
(require 'ksm-window)
(global-set-key (kbd "C-x j") #'ksm/window-config-restore) ; Prompt user and restore window configuration identified by NAME
(global-set-key (kbd "C-x p") #'ksm/window-config-save) ; Prompt user and save window configuration identified by NAME
(global-set-key (kbd "C-x w") #'ksm/window-zoom-out) ; Pop a window configuration off the stack and restore it
(global-set-key (kbd "C-x z") #'ksm/window-zoom-in) ; Expand current window to entire frame, pushing the window configuration on the stack beforehand
```

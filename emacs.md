# How to disable the emacs init help message
`(defun display-startup-echo-area-message ()` <br>
`  (message nil))`
  
# Revert file changes
`(revert-buffer :ignore-auto :noconfirm)`

# Use the GUI(GTK) dialog to open files
```
(defun open-file-gui ()
  (interactive)
  (let ((use-dialog-box t)
         (use-file-dialog t)
         (last-nonmenu-event nil))
    (menu-find-file-existing)))

(defun new-file-gui ()
  (interactive)
  (let (
        (use-dialog-box t)
         (use-file-dialog t)
         (last-nonmenu-event nil))
    (cl-flet ((next-read-file-uses-dialog-p () t))
      (call-interactively 'find-file))))
```

# Set the autocompletion dialog to appear instantly
`(setq company-idle-delay 0.0)`

# csharp-ls not showing hower-over docs
Simply execute lsp agin

# Disable top/tool/scroll bars in emacs
(menu-bar-mode -1)
(scroll-bar-mode -1)
(tool-bar-mode -1) 

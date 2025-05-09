# Highlighted less and cat
Highlighted cat(alias): `alias ccat='highlight -O ansi --force'`
Highlited less(in .sh file): `highlight -O ansi --force $1 | less`

# Not working TTY on an nvidia gpu
Simply add `nvidia_drm.modeset=1 nvidia_drm.fbdev=0` to your kernel arguments, in case of grub /etc/default/grub

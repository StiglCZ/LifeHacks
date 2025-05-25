# Highlighted less and cat
Highlighted cat(alias): `alias ccat='highlight -O ansi --force'`
Highlited less(in .sh file): `highlight -O ansi --force $1 | less`

# Not working TTY on an nvidia gpu
Simply add `nvidia_drm.modeset=1 nvidia_drm.fbdev=0` to your kernel arguments, in case of grub /etc/default/grub

# Fix doing focus next in i3wm on multiple monitors
Add: `focus_wrapping workspace`, and it will always limit it to the 1 monitor

# Controlling i3wm from bash
Simply prefix the i3 command with i3-msg, like so: `i3-msg workspace 3` and execute
 
# Controlling any playing media locally
`playerctl next`
`playerctl prev`
works on vlc, firefox, mpv, etc.

# Getting CPU temps
Inside: `/sys/class/thermal/*`
Is in milli celsius(Celsius * 1000)

# Getting CPU frequencies
Simply execute: `watch -n.3 "grep \"^[c]pu MHz\" /proc/cpuinfo"` and watch

# Execute as sudo but remain environment/theme
If you want to for example retain you user profile, often including the theme for your programs, simply use `sudo -E`

# No mouse on linux, controlling your mouse via keyboard
Simply execute: `setxkbmap -option keypad:pointerkeys` and then press Shift + Numlock, and control the mouse with your numkeys. Everything except scrolling works fine.


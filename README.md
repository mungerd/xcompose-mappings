xcompose-mappings
=================

XCompose mappings for unicode input, especially useful for unicode LaTeX input with XeTeX or LuaTeX.


## How to use

Make sure XCompose is activated by adding these lines to your `~/.profile` file.

    export GTK_IM_MODULE=xim
    export XMODIFIERS=@im=none
    export QT_IM_MODULE=xim


Then, put these lines in your `~/.XCompose` file:

    include "/usr/share/X11/locale/en_US.UTF-8/Compose"
    include "<prefix>/xcompose-mappings/arrows"
    include "<prefix>/xcompose-mappings/doublestruck"
    include "<prefix>/xcompose-mappings/fraktur"
    include "<prefix>/xcompose-mappings/greek"
    include "<prefix>/xcompose-mappings/math"
    include "<prefix>/xcompose-mappings/mathbold"
    include "<prefix>/xcompose-mappings/script"
    include "<prefix>/xcompose-mappings/spaces"

where `<prefix>` is the path to which you have cloned this repository.


To use `PrintScreen` as your compose key, run:

    setxkbmap -option 'compose:prsc'

To see all supported compose options, type:

    grep "compose:" /usr/share/X11/xkb/rules/base.lst

To keep using the `Right Alt` key as third-level shift but use `Shift + Right
Alt` as the compose key, run:

    setxkbmap -option lv3:ralt_switch_multikey

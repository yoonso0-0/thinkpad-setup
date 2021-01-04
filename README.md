# thinkpad-setup


### Toggle `ctrl` and `alt` key

Ref : https://askubuntu.com/questions/93624/how-do-i-swap-left-ctrl-with-left-alt-on-my-keyboard

```
~$ gedit ~/.Xmodmap
```
That will create the file and open it in gedit. Add the following lines to the file:

```
clear control
clear mod1
keycode 37 = Alt_L Meta_L
keycode 64 = Control_L
add control = Control_L Control_R
add mod1 = Alt_L Meta_L
```

Save the file and quit gedit. Next time you login the new keymappings will be active. To have the settings take immediate effect run the following command:

```
~$ xmodmap ~/.Xmodmap
```

# Arch Linux - adding colour to your terminal

These are the steps I take to add a bit of colour to the Arch Linux terminal

## Pacman.conf
By default the colour option in pacman's conf file is commented out. Also, adding "ILoveCandy" enables the pacman animation when downloading packaages.

```
sudo nano /etc/pacman.conf
```
Find the "# Misc options" section and comment out Colour and add in ILoveCandy
```
# Misc options
Color
ILoveCandy
```
Save and exit.

## Bashrc
I wanted a command prompt similar to Debian's one. Edit your .bashrc file located in you home directory.
```
nano .bashrc
```
Replace your PS1 line with this
```
PS1='\[\e[01;32m\]\u@\h\[\e[00m\]:\[\e[01;34m\]\w\[\e[00m\]\$ '
```
Save and exit your terminal. When you go back in you should see a coloured prompt.

## Nanorc
Final step is to add some colour to your Nano editor. By default it looks very white in Arch. Edit your nanorc file
```
sudo nano /etc/nanorc
```
Scroll down to the "Syntax coloring" section and uncomment the line with include "# /usr/share/nano/*.nanorc"
```
include /usr/share/nano/*.nanorc
```
Save and exit, then go back into your nanorc file again. Now you have colour.

This should add a bit of color to your terminal, similar to other distros :)

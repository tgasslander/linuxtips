# linuxtips
Just an information bank with stuff I don't want to forget and don't want to google... again

## Xrandr - get your displays in order
### List your connected screens
```
xrandr --listmonitors
```
Example output:
```
Monitors: 2
 0: +DP-4 3840/950x2160/540+1920+0  DP-4
 1: +eDP-1-1 1920/344x1080/194+0+0  eDP-1-1
```
### Config 
Set the laptop screen (eDP-1-1) to the left of the external one (DP-4)
```
xrandr --output eDP-1-1 --auto --left-of DP-4
```

## Vim mode in the terminal
The terminal is normally in emacs mode.
To get some proper vim bindings do:
```
set -o vim
```
Stuff like `CTRL-A` to go to the beginning of the line is now `0`. Your H-J-K-L keys work to navigate your bash (or other) shell history.

> Note: Luckily, for Mac users, this works in the mac terminal (at least iTerm) as well


## SD Card
First create `/mnt/sd` 

To list your devices:
```
sudo fdisk -l
```

Provided that your SD card is at /dev/sdc1:
´´´
sudo mount -t vfat /dev/sdc1 /mnt/sd
```

To list your devices:
```
sudo fdisk -l
```

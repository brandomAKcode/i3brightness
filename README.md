# i3brightness

### Block to Control Screen Brightness for i3blocks

This block is shared because it is very useful if you use i3blocks and want to control your screen brightness.
I hope it can be helpful to you.

I am testing this on Lubuntu but it should work without problems on any Linux distro.

> **Requirements:**
>
> - Add your user to the video group to be able to change the brightness // This is for Ubuntu

> **Dependencies:**
>
> - font-awesome
> - i3blocks
> - brightnessctl

<hr/>

### Preview

![Preview](https://imgur.com/uppcG4Q.png)

<hr/>

### Install Dependecias Debian/Ubuntu

font-awesome:

```
sudo apt install fonts-font-awesome
```

i3blocks:

```
sudo apt install i3blocks
```

brightnessctl:

```
sudo apt install brightnessctl
```

<hr/>

### Install block

Clone repository

```
git clone https://github.com/brandomAKcode/i3brightness.git
cd i3brightness
```

Copy the script into the scripts folder

```
cp i3brightness  i3brightness_down  i3brightness_up ~/.config/i3blocks/scripts
```

Add execution permissions to the scripts

```
chmod +x ~/.config/i3blocks/scripts/*
```

Add the blocks to the i3blocks configuration file `~/.config/i3blocks/config`

```
[brightness]
command=~/.config/i3blocks/scripts/i3brightness
label=
interval=1

[brightness_up]
command=~/.config/i3blocks/scripts/i3brightness_up
interval=once

[brightness_down]
command=~/.config/i3blocks/scripts/i3brightness_down
interval=once
```

<hr/>

### Additional configuration

You can change the brightness increment and decrement intervals by modifying the `INCREASE_BY` and `DECREASE_BY` variables in the `i3brightness_down` and `i3brightness_up` files.

<hr/>

### Inspired by

Anachron https://github.com/Anachron

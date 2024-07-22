# i3 Focused window

Displays title of focused window in i3Wm

![Demo](i3-focusedwindow.png)

# Requirements

Dependencies: `xdotool`

# Command line arguments  

```
> i3-focusedwindow -h
Usage: i3-focusedwindow <displayOption ...>

Other Options:
  -h, --help                    Print usage information.

Display Options:
  -c, --classname               Get classname of current window
  -d, --dimensions              Get window dimensions of current window
  -p, --position                Get window positions of current window
  -t, --titlename               Get titlename of current window
```

# Installation

The recommended i3blocks config is this:
```INI
[i3-focused-window]
command=$SCRIPT_DIR/custom/i3-focused-window -class
interval=1
```
or this:
```INI
[i3-focused-window]
command=$SCRIPT_DIR/i3-focused-window -class -title
interval=once
signal=10
```
with this, or similar, i3 config:
```
bindsym --release Pause       exec pkill -SIGRTMIN+10 i3blocks
```

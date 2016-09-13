My personal i3 window manager config files
------------------------------------------

The contents of the repo is supposed to be cloned into the `~/.i3`
directory.


```
git clone git@github.com:gszasz/doti3.git ~/.i3
```

Following links should be created afterwards:

```
ln -sf ~/.i3/scripts/battery-notify ~/bin/battery-notify
ln -sf ~/.i3/scripts/cconv ~/bin/cconv
ln -sf ~/.i3/scripts/docked-mode-toggle ~/bin/docked-mode-toggle
ln -sf ~/.i3/scripts/i3-get-window-criteria ~/bin/i3-get-window-criteria
ln -sf ~/.i3/scripts/presentation-mode-toggle ~/bin/presentation-mode-toggle
```

The following entry should be added into user's crontab, by `crontab -e`:

```
#
# My personal crontab
#
PATH=/bin:/usr/bin:/home/gszasz/.local/bin:/home/gszasz/bin
DISPLAY=:0

*/5 * * * *   battery-notify
```

The following entry should be added to the /etc/lightdm/lightdm.conf:

```
[SeatDefaults]
...
display-setup-script=/home/gszasz/.i3/scripts/set-screen-layout
...
```

Scripts
-------
* `battery-notify` - Send alert message when battery is low.
* `cconv` - An ultimate currency convertor for bash.
* `docked-mode-toggle` - Switch i3 desktop between docked and undocked mode.
* `i3-get-window-criteria` - Get criteria for use with i3 config commands.
* `presentation-mode-toggle` - Switch i3 desktop to presentation mode.
* `set-screen-layout` - Initial screen settings for LightDM.


Credits
-------

I took a lot of inspiration from Lukas Zapletal. See [1] for more details.

[1] http://lukas.zapletalovi.com/2012/08/new-in-fedora-17-i3-42-tiling-wm.html

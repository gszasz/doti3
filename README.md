My personal i3 window manager config files
------------------------------------------

The contents of repo should be cloned into the `~/.i3` directory and
following links should be created:

```
ln -sf ~/.i3/.i3status.conf ~/.i3status.conf
ln -sf ~/.i3/dunstrc ~/.config/dunst/dunstrc
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

Scripts
-------
* `battery-notify` - Send alert message when battery is low.
* `cconv` - An ultimate currency convertor for bash.
* `docked-mode-toggle` - Switch i3 desktop between docked and undocked mode.
* `i3-get-window-criteria` - Get criteria for use with i3 config commands.
* `presentation-mode-toggle` - Switch i3 desktop to presentation mode.


Credits
-------

I took a lot of inspiration from Lukas Zapletal. See [1] for more details.

[1] http://lukas.zapletalovi.com/2012/08/new-in-fedora-17-i3-42-tiling-wm.html

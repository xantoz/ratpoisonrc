============
ratpoisonrc
============
My ratpoison config + multi-desktop/multi-screen script rpms

Requirements
-------------
The following utilities packages are used by rpms:

  * awk
  * busybox (for busybox ash. Can be used for sed, awk, tr and grep as well; but not as well tested)
  * dmenu
  * perl (TODO: try to get rid of this dependency)
  * realpath
  * sed
  * tr
  * grep

rpms requires /bin/ash to be a symlink to busybox with support for the ash shell
built in. ash was chosen over bash for rpms because it allows some degree of
bashisms (in particular 'set -o pipefail'), while being faster than bash
overall.

The following utilities are used by ratpoisonrc:

  * amixer
  * wmname (used to trick some programs behaving badly under non-reparenting WM:s)
  * transset (used to make xterms transparent + convenient keybind)
  * xterm (TODO: make configurable)
  * xrandr (optional, used by the screen rotation commands)
  * compton (optional) (TODO: make configurable)
  * xsel
  * mpv + youtube-dl (C-t y t)
  * physlock
  * sed
  * grep (requires support for 'grep -E', extended regexp)

Install
--------
Clone to $HOME/.config/ratpoison::

  git clone https://github.com/xantoz/ratpoisonrc $HOME/.config/ratpoison
  
Source the config file from $HOME/.ratpoisonrc::
   
  echo "source $HOME/.config/ratpoison/ratpoisonrc" > .ratpoisonrc

To add some optional feature::

  echo "source $HOME/.config/ratpoison/volumerc" >> .ratpoisonrc

emacs-for-scala
===============

My Emacs setup for Scala development, including a fully-configured Ensime.

![What does it look like?]
(./emacs2.png)

This latest version uses MELPA to download packages instead of installing them directly, and excludes a bunch of packages I've experimented with, but that didn't find their way into my day-to-day workflow.

Intended for use with Emacs for OSX version 24.4 (but likely adapted for other combinations easily enough)

To install additional packages not included by default on startup:

Use M-x package-list-packages
Select the package you want and select "install"

Or edit the .emacs.d/init.el file to taste.

The first time you run load Emacs, it will download the internet. No, it will only feel that way - it will download all package you don't already have installed from MELPA and install them: this only happens the first time.

The .emacs.d contained in this repo has a specific set of keybindings set up for Emacs. Mostly these are the defaults from whatever included modules have been used, but in a few cases they've been customized to play well together.

Please see <a href="http://michaelpnash.github.io/categories.html#emacs-ref" target="_new">here</a> for a series of articles describing the Emacs config I've published here.

By default, the "emacs" launch script here is set up to launch Emacs in GUI mode, using the Emacs for OSX, and not to use client-server mode. If you want to use character-mode, add the param "-nw" to the startup script. This is useful if you want to use Emacs on a remote system, or to use it with Tmux or Screen.
  
For faster startup of Emacs, you can do two things: Compile the elisp, or use Emacs in client-server mode.

For client-server mode, put the scripts 'emacsserver' and 'emacsclient' found in this repo in your path (before any other emacs), and then run "emacs ." - if the server is not running, it will start it, then subsequent launches of emacs will be very quick.

The scripts are intended for OSX, but again could easily be adapted.

Other apps
----------
If your an Emacs user on OSX, you might also want to check out
     - the Emacsome add-on for Chrome
     - the Amethyst window manager
     - Spectacles (a simpler window manager)
     - Alfred

With a bit of work, you can work mostly rodent-free. On OSX the keys map as follows:

| Abbreviation | OSX Key | Notes   |
|--------------|---------|---------|
| M            | Option  | Meta    |
| S            | Command | Super   |
| C            | Control | Control |


# Movement Keys

![Movement](Movement.png)

# Files, Windows, Scrolling Keys

![Scrolling](Scrolling.png)

# Ensime

![Ensime](Ensime.png)

# Spectacle

![Spectacle](Spectacle.png)


-------

Emacs.d Unplugged
-----------------
There is a file emacs.d.zip that contains a snapshot of a .emacs.d directory with all of the above installed
and configured. In envronments where it is not possible for Emacs to contact melpa and download all the 
dependencies directly, you can unzip this file and be up and running immediately - no further downloads should be needed.


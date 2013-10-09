# Getting Started with Slate

## Overview

If you *have* heard of [Slate](https://github.com/jigish/slate)
before, but found it inaccessible because it describes itself as:

> a bit daunting to get configured

Or, if you *have not* heard of [Slate](https://github.com/jigish/slate)
before, but you are using MacOS **and**:

* You find it slightly irritating whenever you manually adjust the
  height and width of windows using a mouse

* You find yourself with a two display setup and you wish you could
  press a button and have an application jump between displays

* You find yourself pressing COMMAND + CONTROL to switch between
  applications, but sometimes you let go before you reach the one you
  want and have to start over again, or perhaps you "go past" the one
  you want and have to loop through again.

**Then you should read on!**

**The goal of this project is to get you up and running with Slate in 10
or 15 minutes.**

[Slate](https://github.com/jigish/slate) can help you manage your
windows, and it *is* really powerful and it can be *extensively*
configured.

However, you can get going with a basic configuration in no time and
it can start contributing to your daily productivity immediately.

This project provides a basic configuration, describes the motivation
behind it, and shows you how to get everything up and running.

In time, you'll know whether you want to go forward with Slate, and if
you do, this can serve as a starting point where your slate
configuration is checked into source control and easily managed.

## Benefits

[Slate](https://github.com/jigish/slate) is capable of many things,
but the *configuration in this project* will focus on three simple
ideas:

### Manage Window Size And Placement

You will be able to use a key press to manage windows.

With regard to window size and placement, you will be able to:

* Maximize the current window
* Make the current window take up exactly half (1/2) of the screen.
  You will be able to split vertically or horizontally.
* Make the current window take up exactly one quarter (1/4) of the
  screen. You will be able to make it jump to any corner: upper left,
  upper right, bottom left, or bottom right.

### Manage Windows Between Displays

If you have multiple monitors, you will be able to use a key press to
make the current window appear on any monitor.

### Manage The Currently Active Window

You will be able to jump between windows with a key press in a fashion
similar to (but faster and less error prone ) than using the
COMMAND-TAB mechanism.

### How Will This Work?

#### Size and Placement

The core of window sizing and placing is based on key-bindings laid
out in the form of a grid, similar to
[a numeric keypad](http://en.wikipedia.org/wiki/Numeric_keypad), and
then utilizing the grid metaphor to make movement more familiar and
think about movement in terms of the "corners" and the "sides" of the
numeric keypad.

Presuming you've got a QWERTY North American keyboard layout, if you
look down you'll see the following keys *sort of* make a 3 x 3 grid:

<table>
  <tr>
    <td>
      u
    </td>
    <td>
      i
    </td>
    <td>
      o
    </td>
  </tr>
    <tr>
    <td>
      j
    </td>
    <td>
      k
    </td>
    <td>
      l
    </td>
  </tr>
    <tr>
    <td>
      m
    </td>
    <td>
      ,
    </td>
    <td>
      .
    </td>
  </tr>
</table>

The associated Slate configuration will make it so that if you hold
CONTROL and COMMAND and then press the keys on the corners of this
table, then you will cause the current window to take up one quarter
of the screen and go to the associated corner, defined as follows:

* ```COMMAND + CONTROL + u``` = upper left corner
* ```COMMAND + CONTROL + o``` = upper right corner
* ```COMMAND + CONTROL + m``` = bottom left corner
* ```COMMAND + CONTROL + u``` = bottom right corner

Further, the configuration makes it so that if you hold CONTROL and
COMMAND and then press the keys on the top, bottom, left, and right,
then you will cause the current window to take up one half of the
screen and it will split vertically or horizontally, defined as
follows:

* ```COMMAND + CONTROL + i``` = top half of screen
* ```COMMAND + CONTROL + l``` = right half of screen
* ```COMMAND + CONTROL + ,``` = bottom half of screen
* ```COMMAND + CONTROL + j``` = bottom left of screen

And finally, if you press ```COMMAND + CONTROL + k``` you will make
the current window take up the entire screen (it will be maximized).

#### Moving Between Displays

If you've got two displays, press ```COMMAND + CONTROL + 2``` to cause
the current window to appear on the second display. Immediately after,
press ```COMMAND + CONTROL + 1``` to cause the same window to jump
back to the first display.

#### Switching Applications

Open at least two applications. Then, press ```COMMAND + CONTROL + ;```

When you press that key-binding, application icons will appear and a
letter will be associated with each icon. These letters are configured
to always be on the home row of the QWERTY keyboard.

If you press the associated letter, you change applications accordingly.

### How do I get started?

Visit the Slate homepage and follow the installation instructions.

Once you have installed slate, clone this repository to somewhere on
your file system.

Once cloned, make the `.slate` file in your home directory point to
the `.slate` file from the directory what was created when you cloned.

For example, if you cloned this project into:
`~/projects/getting-started-with-slate`, then type:

```
cd
ln -s ~/projects/getting-started-with-slate/.slate .slate
```

This will cause a symbolic link to be created in your home directory
that points to the `.slate` file that comes with this project (and
provides these key bindings).

If you don't have git, or don't want to clone the repository, just
navigate to the .slate file on github, and then save it to your
computer and place it in your home directory so that it is saved as
`~/.slate`.

Finally, once you've installed the configuration file, find the Slate
icon at the top of your screen and select 'Relaunch and Load Config'

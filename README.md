# Beginning with Slate

## Overview

If you *have* heard of [Slate](https://github.com/jigish/slate)
before, but found it inaccessible because it describes itself as:

> a bit daunting to get configured

Or, if you *have not* heard of [Slate](https://github.com/jigish/slate)
before, but you are using MacOS **and**:

* You find it slightly irritating whenever you manually adjust the
  height and width of windows using a mouse, **or**

* You find yourself with a two display setup and you wish you could
  press a button and have an application jump between displays, **or**

* You find yourself pressing COMMAND + CONTROL to switch between
  applications, but sometimes you let go before you reach the one you
  want and have to start over again, or perhaps you "go past" the one
  you want and have to loop through again.

Then you should read on!

The goal of this project is to get you up and running with Slate in 10
or 15 minutes.

[Slate](https://github.com/jigish/slate) can help you manage your
windows, and it *is* really powerful and it can be *extensively*
configured.

However, you can get up and running with a basic configuration in no
time and it can start contributing to your daily productivity
immediately.

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

* ```COMMAND + CTRL + u``` = upper left
* ```COMMAND + CTRL + o``` = upper right
* ```COMMAND + CTRL + m``` = bottom left
* ```COMMAND + CTRL + u``` = bottom right

Further, the configuration makes it so that if you hold CONTROL and
COMMAND and then press the keys on the top, bottom, left, and right,
then you will cause the current window to take up one half of the
screen and it will split vertically or horizontally, defined as
follows:

* ```COMMAND + CTRL + i``` = top half
* ```COMMAND + CTRL + l``` = right half
* ```COMMAND + CTRL + ,``` = bottom half
* ```COMMAND + CTRL + j``` = bottom left

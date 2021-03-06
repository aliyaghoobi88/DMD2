DMD2 is an Arduino library designed as an updated replacement for the [original DMD library](http://github.com/freetronics/DMD). Both libraries are designed for use with the [Freetronics Dot Matrix Display](http://www.freetronics.com/collections/display/dmd).

**This library is currently in BETA release meaning the documentation is incomplete, and the implementation may contain bugs. If you want the stable version, please use the [original DMD library](http://github.com/freetronics/DMD) for now not DMD2.**

If you find any bugs, please use the Issues feature in github to report them or [post on the Freetronics Dot Matrix Display forum](http://forum.freetronics.com/viewforum.php?f=26).

# Changes from DMD library

The DMD2 library includes the following new features:

* Supports Arduino Due (IDE 1.5.6 or newer), as well as AVR-based Arduinos.
* Adds new "SoftDMD" support, which allows the standard DMDCon board connections to be used on all standard Arduino compatible models - including Arduino Mega/EtherMega, Arduino Due/EtherDue or Arduino Leonardo.
* Integrated timer management for simpler sketches.
* Improved performance, a single DMD panel uses approximately 5-6% CPU overhead to update (including when using the SoftDMD mode rather than hardware SPI.)
* New drawString() methods accept flash strings, or the Arduino String type, directly. See the "AllDrawingOperations" example.
* New DMD_TextBox class supports automatic scrolling, and automatic `print()` interface for writing out numbers, variables, etc. See "Countdown" and "ScrollingAlphabet" examples.
* New dmd.setBrightness() call allows changing DMD brightness (no more blindingly bright displays!)
* New DMDFrame base class allows direct swapping of the DMD framebuffer, supporting double buffering operations and similar (see "GameOfLife" example.)

# Not Yet Implemented

* Test patterns

# Getting Started

[Install the Arduino library using the steps described here](http://www.freetronics.com/pages/how-to-install-arduino-libraries). You will find some example sketches under File -> Examples -> DMD2.

More documentation will be produced before the library reaches final release rather than Beta status. Many of the DMD2 concepts are borrowed from FTOLED library so the [FTOLED wiki](https://github.com/freetronics/FTOLED/wiki/) may be of use.

Feel free to ask [questions on the forum](http://forum.freetronics.com/viewforum.php?f=26) if things don't work.

# About the Makefiles

You'll notice the examples directory contains some files named `Makefile`. You can ignore these if you are using the Arduino IDE.

However, if you want to use other development tools with the DMD library, the Makefiles work with with the [arduino-mk](http://www.mjoldfield.com/atelier/2009/02/arduino-cli.html) package, version 1.3.1. They may need updating to work with newer versions.

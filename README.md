# HaKey

![HaKey logo](artwork/logo.svg)

Software-level advanced keyboard customization tool.

---

**WARNING!** This project is in very early development stage!
             Mostly documenting stuff…

**HaKey** is **Ha**skell + **Key**board.
The round key cap on the logo is an allusion to a hockey puck,
just because _“HaKey”_ and _“hockey”_ seem to sound similar.

This program (or a set of programs) is a continuation of
[my another project][xlib-keys-hack].

## Goals & Motivation

The general goal is to fix some issues of [xlib-keys-hack] project and to add
new features. [xlib-keys-hack] is very tied to my own requirements and in some
parts not flexible enough so I want this tool to satisfy almost everyone else’s
needs.

The goals are (to make it to be…):

- Relatively easy to use for almost any advanced user
- Very flexible and configurable
- Robust and stable

The motivation is to satisfy my own needs and requirements in a customizable
generic way so this would be useful not only for me (as [xlib-keys-hack] project
seems to be) but for everyone else.

## TODOs

These features this tool is supposed to provide for everyone:

- [ ] Input
  - [ ] GNU/Linux & FreeBSD [evdev] devices
    - [ ] Automated disabling input devices for [X Window System][X11]
          (those which attached to [evdev] devices we’re reading raw
          events from)
    - [ ] Automated enabling back those input [X11] devices which have
          been occupied by **HaKey** after its termination
- [ ] Output
  - [ ] [X11] [XTEST]
  - [ ] [Wayland] libinput? (I don’t know how to deal with [Wayland] yet)
- [ ] Input layer configurable layout
  - [ ] Customizable mapping between raw [evdev] key numbers to virtual
        source keys (like `16` is a `Q` key)
  - [ ] Independent input layer mappings for different keyboards/[evdev]
        devices
- [ ] Output configurable layout
  - [ ] Mapping between source keys and [X11] keys (for [XTEST] output)
  - [ ] Mapping between source keys and [Wayland] keys (for [Wayland]
        output)
  - [ ] Independent output mappings for different keyboards/[evdev]
        devices
- [ ] Switchable layers (switchable by modifiers, togglers, whatever, in
      [xlib-keys-hack] you can see two additional layers of so called
      _alternative mode_), any amount of layers you want or just a single main
      one
- [ ] Shifted modifiers (being able to type `!` for instance by pressing a
      single key, the tool would automatically trigger `Shift`+`1`)
- [ ] Basic predefined output layouts
  - [ ] [QWERTY]
  - [ ] [Dvorak]
  - [ ] [Programmer Dvorak]
- [ ] Store state of some modes
  - [ ] Store _Num Lock_ state
  - [ ] Store _Caps Lock_ state
  - [ ] Store _Scroll Lock_ state
  - [ ] Store _[XKB]_ layout state
- [ ] Reset modes to _default state_
  - [ ] Reset _Num Lock_ state
  - [ ] Reset _Caps Lock_ state
  - [ ] Reset _Scroll Lock_ state
  - [ ] Reset _[XKB]_ layout state
- [ ] DBus IPC
  - [ ] Notify other clients about some modes
    - [ ] _Num Lock_ state
    - [ ] _Caps Lock_ state
    - [ ] _Scroll Lock_ state
    - [ ] _[XKB]_ layout state
  - [ ] Reset modes (incoming API)
  - [ ] Switch output layout layer to specific one (incoming API)
  - [ ] Switch some modes to specific state (incoming API)
    - [ ] _Num Lock_
    - [ ] _Caps Lock_
    - [ ] _Scroll Lock_
    - [ ] _[XKB]_ layout
- [ ] Send and receive events over network
  - [ ] Support encryption to prevent key-logger attacks
  - [ ] Warn user about unencrypted connection
  - [ ] Hot connect/reconnect interface
- [ ] Safe hot plug/unplug of devices
- [ ] Automatically (re)connect to just plugged in device

**WARNING!** This list is incomplete yet,
             there will be more features described here!

[evdev]: https://en.wikipedia.org/wiki/Evdev
[X11]: https://en.wikipedia.org/wiki/X_Window_System
[XTEST]: https://www.x.org/releases/X11R7.7/doc/libXtst/xtestlib.html
[XKB]: https://en.wikipedia.org/wiki/X_keyboard_extension
[Wayland]: https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)
[QWERTY]: https://en.wikipedia.org/wiki/QWERTY
[Dvorak]: https://en.wikipedia.org/wiki/Dvorak_keyboard_layout
[Programmer Dvorak]: https://en.wikipedia.org/wiki/Dvorak_keyboard_layout#Programmer_Dvorak

## Author

Viacheslav Lotsmanov

### Creator of the logo

Viacheslav Lotsmanov

## License

### License for the code

[GNU AGPLv3](LICENSE)

GNU Affero General Public License  
Version 3, 19 November 2007

#### Why this one

Using **AGPLv3** instead of just **GPLv3** because this tool may have web
interface for configuring keyboard layout in the future.

### License for the logo

[CC BY-SA 4.0]

Creative Commons — Attribution-ShareAlike 4.0 International

[CC BY-SA 4.0]: https://creativecommons.org/licenses/by-sa/4.0/
[xlib-keys-hack]: https://github.com/unclechu/xlib-keys-hack

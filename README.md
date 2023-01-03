# menu-qalc
A calculator for Wofi/dmenu(2).
Adapted for Wayland and Wofi.

[Screencast](https://gfycat.com/SociableDopeyHerald)

## Installation

    git clone [repository]
    cd ./menu-qalc
    chmod +x menu-qalc
    mv menu-qalc ~/.local/bin/

## Dependencies
- [libqalculate](https://archlinux.org/packages/extra/x86_64/libqalculate/)
- [wl-clipboard](https://github.com/bugaevc/wl-clipboard/)
- [Wofi](https://hg.sr.ht/~scoopta/wofi/) or
  dmenu[(2)](https://aur.archlinux.org/packages/dmenu2/)

## Usage
`menu-qalc` uses `qalc` as the backend and will accept any operations `qalc` is able to do:

    = 4+4
    = (4+2)/(4+3)
    = 4^2
    = sqrt(4)
    = c(2)
    = '500 + 25%'
    = '1000 EUR to USD'

The answer can be copied to the clipboard and used for further calculations
inside (or outside) Wofi/dmenu.

If launched outside of Wofi/dmenu the expression may need quotation marks.

## Custom Usage
To launch directly into the calculator, use the following command (useful if
bound to "super + equal" in [sway](https://swaywm.org/) or the like):

    = -- [wofi/dmenu parameters]

For example:

    = -- --location 2 --width 100

### Force usage of `dmenu`
By default, if `wofi` is installed, it will be used. You can force `menu-qalc`
to use `dmenu` or any other `dmenu`-like application:

    = --dmenu=dmenu

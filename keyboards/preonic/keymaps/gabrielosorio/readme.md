# A customized version of the default Preonic layout - largely based on the Planck's

For the full docs, go to [docs.qmk.fm](https://docs.qmk.fm/).

## Setup
1. `$ brew install qmk/qmk/qmk`
1. `$ qmk setup`
1. `$ qmk config user.keyboard=preonic/rev3`
1. `$ qmk config user.keymap=gabrielosorio`

## Compiling

Use the full (explicit) command if you haven't set the defaults, or have more than one keyboard/keymap.

```
$ qmk compile [-kb preonic/rev3 -km gabrielosorio]
```

## Flashing

1. `$ qmk flash [-kb preonic/rev3 -km gabrielosorio]`
1. Put your keyboard into bootloader/DFU/reset mode: `[LWR] + [RSE] + q`

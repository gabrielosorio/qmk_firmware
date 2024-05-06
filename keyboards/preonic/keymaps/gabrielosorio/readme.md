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

## Troubleshooting

### Submodules

Error:

```
Command '['git', 'submodule', 'update', '--init', '--recursive']' returned non-zero exit status 128.
```

When running `qmk setup`


Solution:

1. Check: `git submodule status`
1. If you're seeing: `fatal: no submodule mapping found in .gitmodules for path 'lib/ugfx'`
1. `rm -rd lib/ugfx`
1. `git rm --cached lib/ugfx`
1. `make git-submodule`

---

Error:

```
./lib/chibios/os/rt/include/chchecks.h:48:2: error: #error "obsolete or unknown configuration file"
```

When running `qmk compile`

Solution:

1. `git rm --cached lib/chibios`
1. `make git-submodule`


## Old Changes

For the original changes to the fork, see the branch `pre_sync_backup`.

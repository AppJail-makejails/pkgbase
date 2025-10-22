# PkgBase

PkgBase is the FreeBSD base operating system (OS), packaged for use with `pkg(8)`.

wiki.freebsd.org/PkgBase

<img src="https://upload.wikimedia.org/wikipedia/en/thumb/d/df/Freebsd_logo.svg/2560px-Freebsd_logo.svg.png" alt="freebsd logo" width="80%" height="auto">

## How to use this Makejail

```sh
appjail makejail \
    -j pkgbase \
    -f gh+AppJail-makejails/pkgbase \
    -o virtualnet=":<random> default" \
    -o nat
```

### Arguments

* `pkgbase_ajspec` (default: `gh+AppJail-makejails/pkgbase`): Entry point where the `appjail-ajspec(5)` file is located.
* `pkgbase_tag` (default: `15-minimal`): see [#tags](#tags).

## Tags

| Tag                | Arch    | Version | Type    | `pkgbase_osversion` | `pkgbase_release`      |
| ------------------ | --------| ------- | ------- | ------------------- | ---------------------- |
| `15-minimal` | `amd64` |    -    | `thick` |     `15`      | `15-minimal` [1] |
| `15-full`    | `amd64` |    -    | `thick` |     `15`      | `15-full`    [2] |
| `16-minimal` | `amd64` |    -    | `thick` |     `16`      | `16-minimal` [3] |
| `16-full`    | `amd64` |    -    | `thick` |     `16`      | `16-full`    [4] |

1. Created by `appjail fetch pkgbase -r 15-minimal -v 15 FreeBSD-set-minimal-jail`
2. Created by `appjail fetch pkgbase -r 15-full -v 15 FreeBSD-set-base FreeBSD-kernel-generic`
3. Created by `appjail fetch pkgbase -r 16-minimal -v 16 FreeBSD-set-minimal-jail`
4. Created by `appjail fetch pkgbase -r 16-full -v 16 FreeBSD-set-base FreeBSD-kernel-generic`

## Notes

1. Early versions of this Makejail use the OCI image, but now it's just a copy of the base directory created by the `appjail-fetch(1)` `pkgbase` command.

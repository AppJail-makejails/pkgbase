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
* `pkgbase_tag` (default: `14-minimal`): see [#tags](#tags).

## Tags

| Tag                | Arch    | Version            | Type   | `pkgbase_full` | `pkgbase_from`                               |
| ------------------ | --------| ------------------ | ------ | -------------- | -------------------------------------------- |
| `14-minimal` | `amd64` | `14-PKGBASE` | `thin` |      `0`       | `quay.io/dougrabson/freebsd14-minimal` |
| `14-full`    | `amd64` | `14-PKGBASE` | `thin` |      `1`       | `quay.io/dougrabson/freebsd14-full`    |

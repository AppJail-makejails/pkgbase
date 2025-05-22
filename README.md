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
* `pkgbase_tag` (default: `14.2-minimal`): see [#tags](#tags).

## Tags

| Tag                | Arch    | Version            | Type    | `pkgbase_full` | `pkgbase_from`                               |
| ------------------ | --------| ------------------ | ------- | -------------- | -------------------------------------------- |
| `14.2-minimal` | `amd64` | `14.2-RELEASE` | `thick` |      `0`       | `docker.io/freebsd/freebsd-runtime:14.2` |
| `14.2-full`    | `amd64` | `14.2-RELEASE` | `thick` |      `1`       | `docker.io/freebsd/freebsd-runtime:14.2` |
| `14.snap-minimal` | `amd64` | `14.snap-STABLE`  | `thick` |      `0`       | `docker.io/freebsd/freebsd-runtime:14.snap` |
| `14.snap-full`    | `amd64` | `14.snap-STABLE`  | `thick` |      `1`       | `docker.io/freebsd/freebsd-runtime:14.snap` |
| `15.snap-minimal` | `amd64` | `15.snap-CURRENT` | `thick` |      `0`       | `docker.io/freebsd/freebsd-runtime:15.snap` |
| `15.snap-full`    | `amd64` | `15.snap-CURRENT` | `thick` |      `1`       | `docker.io/freebsd/freebsd-runtime:15.snap` |

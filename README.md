## i3-gaps

This repository is a snapshot of [i3-gaps](https://github.com/Airblader/i3) `4.19` release with the following changes:

* Provide a unique Debian package identity (`i3-gaps-wm`) over the upstream project, [i3-wm](https://github.com/i3/i3).
* Breaking the Xsession files into a distinct package (`i3-gaps-session`), so that they can be selectively installed.  Installing the package `i3-gaps` will install everything.  Installing `i3-gaps-wm` will install the window manager but not the Xsession files.

Please see the [i3-gaps](https://github.com/Airblader/i3) and [i3-wm](https://github.com/i3/i3) projects for all other details.

### How to Build

To build this package locally, ensure that the Debian packaging tools and `gbp` are installed.  Then invoke `gbp buildpackage` to generate Debian packages.  Example:

```bash
$ git clone git@github.com:regolith-linux/i3-gaps.git && cd i3-gaps
$ gbp buildpackage --git-debian-branch=main
$ ls -haltr /tmp/debian-pkg-builds/
```

### Known Issues

* Manpage generation is not working.
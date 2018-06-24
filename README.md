Keeping yocto-poky buildable with current host tools
====================================================

This is a clone of http://git.yoctoproject.org/git/poky, with two branches:
   * daisy-backports
   * krogoth-backports

These two branches get fixes to keep them buildable with current host OS distributions, tested with openSUSE Leap 15 and openSUSE Tumbleweed.

They are intended to be used together with https://github.com/seife/meta-neutrino-mp meta layer and one of these:
   * https://github.com/seife/meta-tripledragon (daisy-backports)
   * https://github.com/seife/meta-coolstream
   * https://github.com/seife/meta-stlinux

I need daisy for the TripleDragon, because the only available kernel 2.6.12 can not use anything newer because newer glibc does not support old kernels anymore.
Krogoth for the others, because again, old kernels (2.6.32 / 2.6.34) are no longer easily supported by newer releases.

WARNING
=======
These branches are merely kept buildable. No feature, security or bugfix backports are done (unless I happen to be affected by a bug and need to fix it). Use at your own risk.

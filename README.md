# PBP-Things

## What's this about?

Some odds and ends related to the Pinebook Pro, collected in one place to avoid just having them posted somewhere around the web.

PKGBUILDS are mostly taken from the upstream Arch / alarm / Manjaro repos or the AUR and modified to work with the PBP.

**BEWARE:** Most of this is probably not "clean" or "well done" but more about getting things working for me,
so be careful. It's not my fault if your machine breaks or your house catches on fire.

### Managed elsewhere, but might be useful

[Librewolf, a more privacy focused Firefox-(not-really-a-)fork](https://gitlab.com/librewolf-community/browser/arch), also in the AUR (-bin and regular flavor.)

[Caidao, a very slightly modified ungoogled-chromium](https://gitlab.com/ohfp/caidao). I just like to keep an unmodified chromium available next to an ungoogled one.

## bitwarden

Based on [aur/bitwarden](https://aur.archlinux.org/packages/bitwarden).

## ferdi-git

Based on [aur/ferdi-git](https://aur.archlinux.org/packages/ferdi-git), until the [merge request over there](https://gitlab.com/dpeukert/pkgbuilds/-/merge_requests/2) gets merged someday.

## luks

This just gives a hint at what to modify to get LUKS working with uboot on ManjaroARM on the PBP;
mostly it's about getting the boot.txt to actually load the initramfs (default config just doesn't even attempt to load it,
it seems.) and including all the modules required to init the eDP.

## nordnm-git

This just mirrors/tracks the [AUR package](https://aur.archlinux.org/packages/nordnm-git).

## rtl88x2bu-dkms-git

From [the AUR](https://aur.archlinux.org/packages/rtl88x2bu-dkms-git), just with a fix related to an arch/aarch64-related path.

## signal-desktop

Signal requires PhantomJS to be built. Building PhantomJS on arm/aarch64 is hell, so a prebuilt package is provided,
taken from [http://tardis.tiny-vps.com](http://tardis.tiny-vps.com/aarm/packages/p/phantomjs), which is an alarm package archive.


Needed a somewhat ugly workaround for sqlcipher to be able to apply the openssl-linking patch; basically on arm/aarch64,
most things get rebuilt / pulled in afresh so the patch gets overwritten again, when patching via PKGBUILD or with patch-package.


Based on [upstream community/signal-desktop](https://www.archlinux.org/packages/community/x86_64/signal-desktop/).

## tar-multi

This is just tar with multi-threaded backends used per default. Not an aarch64-specific-thing, just useful imho.

The dirrem.patch is just an ugly hack used to avoid build/test failures when building in a dockerized CI pipeline.


Based on [upstream core/tar](https://www.archlinux.org/packages/core/x86_64/tar/).

## wire-desktop

Taken straight from [upstream community/wire-desktop](https://www.archlinux.org/packages/community/any/wire-desktop/) – actually just works/builds without modification.

## zram-swap

Made for https://forum.pine64.org/showthread.php?tid=8812.

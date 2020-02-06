Some odds and ends related to the Pinebook Pro, collected in one place to avoid just having them posted somewhere around the web.

PKGBUILDS are mostly taken from the upstream Arch / alarm / Manjaro repos or the AUR and modified to work with the PBP.

**BEWARE:** Most of this is probably not "clean" or "well done" but more about getting things working for me,
so be careful. It's not my fault if your machine breaks or your house catches on fire.

Signal requires phantomjs to be built. Building phantomjs on arm/aarch64 is hell, so a prebuilt package is provided,
taken from [http://tardis.tiny-vps.com](http://tardis.tiny-vps.com/aarm/packages/p/phantomjs), which is an alarm package archive.

Managed elsewhere:

[Librewolf, a more privacy focused Firefox-(not-really-a-)fork](https://gitlab.com/librewolf-community/browser/arch), also in the AUR.

[Inox, a very slightly modified ungoogled-chromium](https://gitlab.com/librewolf-community/browser/arch)

*luks* just gives a hint at what to modify to get LUKS working with uboot on ManjaroARM on the PBP;
mostly it's about getting the boot.txt to actually load the initramfs (default config just doesn't even attempt to load it,
it seems.) and including all the modules required to init the eDP.

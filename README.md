# OpenWrt NSS

This started out as a private repo for building a variant of the work by [Qosmio](https://github.com/qosmio/openwrt-ipq) refining NSS usability on various Qualcomm platforms.
However, more recently, the focus has turned to the work being done by [JuliusBairaktaris](https://github.com/JuliusBairaktaris/openwrt-nss-edma) in the same area in the absence of Qosmio.

I personally only have an interest in two targets on the ipq807x platform, and have added a few custom packages as well. If you happen to be building for the Linksys MX4200 v1 and v2, then all you need to do is adjust the R2 output stuff as it'll fail without the correct changes! 😅

Feel free to fork the repo (or just outright copy it, I don't care!) if the work in here is of use to you ❤️\
As `Dropbear` is omitted in favour of `OpenSSH` and password authentication is also disabled by the included `sshd_config`, you'll need to either enable password authentication in the config or include your own SSH public key in `custom/files/root/.ssh/authorized_keys` in the repo - that way the changes are included at build time! 🙌

---
*yes I know the commits are messy, I hate public repos because they show how incompetent I am! but they also give unlimited free minutes for GH Actions* 🫣😅 *don't judge me for the commit history on this repo please!*
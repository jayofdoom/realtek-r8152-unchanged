# realtek-r8152-unchanged

## What is this?

Realtek kindly provides a GPL-2.0 licensed driver for their USB Multi-gig
product line. However, it's recently been hidden behind capcha making it
difficult to get the original sources.

## Where can I get this from the source?

This is a direct import of the tarballs as provided by realtek; the latest
URL as of this writing for the source is: 
https://www.realtek.com/Download/List?cate_id=585 -- be warned, it has moved
frequently, so you may have to navigate from the main page. This particular
driver is usually identified by "Realtek USB FE / GBE / 2.5G / 5G Ethernet".

## What cards does this support?

As retrieved from the above website in June 2025:

| Name | USB version | Chipsets |
| ---- | ----------- | -------- |
|  10G Gigabit Ethernet | USB 3.0 | *RTL8159* |
|   5G Gigabit Ethernet | USB 3.0 | *RTL8157* |
| 2.5G Gigabit Ethernet | USB 3.0 | *RTL8156*, *RTL8156B* |
| 10/100/1000M Gigabit Ethernet | USB 3.0 | *RTL8153*, *RTL8153B*, *RTL8153C*, *RTL8153D*, *RTL8153E* |
| 10/100/1000M Gigabit Ethernet | USB 2.0 | *RTL8154*, *RTL8154B* |
| 10/100M Fast Ethernet | USB 2.0 | *RTL8152B* |


## What releases are where?

| tag | sha256sum | filename |
| --- | --------- | -------- |
| v2.16.3 | 664b76b2ac5652779f6865ac7b2917b2ab1f22d1e57decc8e2eeb928e8a68509 | r8152-2.16.3.tar.bz2 |
| v2.17.1 | 8628ae87d98a8a2e52f6cb3bb28931aa4b12beeeb5614c30698c9d14fed5bb6f | r8152-2.17.1.tar.bz2 |
| v2.18.1 | 142b12ce8a4795790e16ac5dce097448d78692aad235af37ddfd1e343c39b0bc | r8152-2.18.1.tar.bz2 |
| v2.19.2 | 104a3abbd3d16287b5a83b532a4f08a81bbd62b8804df7b11d6b9e750e7cae14 | r8152-2.19.2.tar.bz2 |
| v2.20.1 | f092ebf88850b9bf61065889623d0670fa5a0bf1bdcd80e26949560cbf51c94d | r8152-2.20.1.tar.bz2 |

## Who are you and why are you doing this?

I'm the gentoo maintainer for this package, and I wanted a clean source that
I could patch separately, in the ebuild. If you want to use this on a modern
kernel, you can fetch those patches directly from the gentoo repository:
https://gitweb.gentoo.org/repo/gentoo.git/tree/net-misc/r8152 -- look in the
files directory for the patches, and the versioned-ebuild for the order.


## Why do the version numbers have gaps?

I don't know. I check for updates periodically, and often the versions are
higher. As far as I can tell, there's no log of all releases made so I just
archive what I need to package in Gentoo.

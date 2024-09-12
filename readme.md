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

As retrieved from the above website in Sept 2024:

| Name | USB version | Chipsets |
| ---- | ----------- | -------- |
| 5G Gigabit Ethernet | USB 3.0 | *RTL8157* |
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


## Who are you and why are you doing this?

I'm the gentoo maintainer for this package, and I wanted a clean source that
I could patch separately, in the ebuild. If you want to use this on a modern
kernel, you can fetch those patches directly from the gentoo repository:
https://gitweb.gentoo.org/repo/gentoo.git/tree/net-misc/r8152 -- look in the
files directory for the patches, and the versioned-ebuild for the order.

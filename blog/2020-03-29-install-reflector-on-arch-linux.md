---
slug: install-reflector-on-arch-linux
tags: [reflector, pacman, mirrors, python, arch, linux, tutorial, guide]
authors: sebastian
---

# Install Reflector on Arch Linux

![server-rack](/img/server-rack.webp)

Reflector is a small Python3 script that sort through the Arch Linux mirrors based on parameters of your choice and updates your mirrorlist.

<!--truncate-->

***More info:*** [Reflector - ArchWiki](https://wiki.archlinux.org/index.php/Reflector) | [Project website - xyne](https://xyne.archlinux.ca/projects/reflector/)

## Installation

```shell showLineNumbers
pacman -S reflector
```

## Usage

`reflector --help` will show you the available commands and their options.

The following command will update your mirrorlist with the 50 fastest mirrors that have support for both HTTPS and IPV6.

```shell showLineNumbers
reflector --verbose --completion-percent 100 --ipv6 --protocol https --score 50 --sort rate --save /etc/pacman.d/mirrorlist
```

## Service

Reflector can run automatically in the background at chosen intervalls. The default timer will run reflector once a week.

If you want the options from the example earlier make the following changes.

```showLineNumbers title="/etc/xdg/reflector/reflector.conf"
--save /etc/pacman.d/mirrorlist
--completion-percent 100
--protocol https
--ipv6
--score 50
--sort rate
```

```shell showLineNumbers
systemctl enable reflector.timer
systemctl start reflector.timer
systemctl start reflector.service
```

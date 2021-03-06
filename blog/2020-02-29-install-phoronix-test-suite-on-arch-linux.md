---
slug: install-phoronix-test-suite-on-arch-linux
tags: [phoronix test suite, pts, benchmark, arch, linux, tutorial, guide]
authors: sebastian
---

# Install Phoronix Test Suite on Arch Linux

![pts](/img/pts.webp)

This guide will walk through the steps for installing the [Phoronix Test Suite](https://www.phoronix-test-suite.com/) on Arch Linux. The software will be installed from the [Arch User Repository (AUR)](https://aur.archlinux.org/) with the help of the [AUR Helper](https://wiki.archlinux.org/index.php/AUR_helpers)*yay*. If you don't have an AUR Helper you should definately install one. I have a guide for two of them: [Install yay on Arch Linux](/install-yay-on-arch-linux) & [Install paru on Arch Linux](/install-paru-on-arch-linux).

<!--truncate-->

[Phoronix Test Suite - Documentation](https://www.phoronix-test-suite.com/documentation/phoronix-test-suite.html)

## Installation

```shell showLineNumbers
paru -S phoronix-test-suite
```

## Usage

| Function     | Command                            |
| ------------ | ---------------------------------- |
| List tests   | phoronix-test-suite list-tests     |
| Install test | phoronix-test-suite install `test` |
| Run test     | phoronix-test-suite run `test`     |

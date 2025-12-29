Fork
====

This is a fork of the [alpine-nanopi-neo-rt](https://github.com/jbrazio/alpine-nanopi-neo-rt) repo. The original readme is below the double separation line.

Changes:
- Added compatibility for building an image from Windows.

Quick start:
1. `git clone` this repo.
2. run `docker compose run nanopi-neo /bin/bash` in the folder containing the `docker-compose.yaml` file.
3. when the download and preparation is complete and the bash prompt appears, type `make all` to create the SD card image.
4. the resulting image will be located at `out_image/sdcard-alpine-sunxi-nanopi_neo-256M.img`.

Burn the resulting image to an SD card using an ISO-imager program such as `usbimager` or `win32diskimager` or similar.
Insert the SD card into the NanoPi Neo and power it on. Use the `Debug UART` (UART0 TTL) port to interact with the newly built operating system.

_NB_: The system comes with a single `root` user with no password, and SSH login as root is disabled.

See `src/Makefile` for more complex cases or to build the image in separate steps.

---
---

Alpine Linux real-time kernel build root for NanoPi NEO
=======================================================

This repository contains the build root for building an unofficial port
of [Alpine Linux][1] for the [FriendlyARM NanoPi NEO][2] board patched with the
[CONFIG_PREEMPT_RT][3] real-time Linux patch.

- U-Boot v2024.04
- Kernel v5.4.84 (rt47)
- Alpine v3.19

Use the provided docker files to build the sdcard image.

[1]: https://alpinelinux.org/
[2]: https://linux-sunxi.org/FriendlyARM_NanoPi_NEO
[3]: https://rt.wiki.kernel.org/index.php/Main_Page

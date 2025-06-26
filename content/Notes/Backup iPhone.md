---
date: 2025-06-26
title: Back-up iPhone using rsync
tags:
  - iphone
  - linux
---

Plugin your iPhone via USB cable, then run the following commands:


```bash

# install required packages
sudo apt install libimobiledevice6 libimobiledevice-utils ifuse

# pair device
# note: maybe interaction like entering the access code on the phone is required
# rerun this command after entering the PIN until you get a success message
idevicepair pair

# enable multiple connections
usbmuxd -f -v

# create mount point
sudo mkdir /media/iphone

# mount your device as userspace filesystem (FUSE)
ifuse /media/iphone

# open files in favorite file explorer (Desktop OS only)
xdg-open /media/iphone

# unmount phone after file transfer
fusermount -u /media/iphone
# alternate method: ifuse -u /media/iphone

```


There is also a command-line tool to download photos from iCloud.  See https://github.com/icloud-photos-downloader/icloud_photos_downloader
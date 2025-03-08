---
title: How to properly install Windows
date: 2025-03-08T18:44:52Z
lastmod: 2025-03-08T18:44:52Z
author: Timot
avatar: /timot.jpg
# authorlink: https://author.site
cover: /hirensboot_000.webp
# images:
#   - /img/cover.jpg
categories:
  - Windows
  - Operating Systems
  - Tutorials
tags:
  - tag1
  - tag2
# nolastmod: true
draft: false
---

You've probably installed Windows the wrong way your entire life. Let me show you the right way to do it. This method is faster and works the same as the usual method.

<!--more-->
![Hiren's Boot](/hirensboot_000.webp)

Before we begin with this i'll assume you already know how to make a multibootable USB using ventoy and you've already have the Windows 10/11 iso ready. To begin with this method go to the [Hiren's Boot Website](https://www.hirensbootcd.org/), go to the downloads page and download the HBCD_PE_x64.iso and put it in your multiboot usb drive (if you use an autounattend.xml file copy it too).

![Partition Tools](/hirens_boot_partition_tools_000.webp)

Boot into Hiren's Boot and the first thing you wanna do is partition your ssd if you haven't yet. In this case i'm in a virtual machine so i don't have a main nor a boot partition so as you can see i made them with Aomei Partition Assistent (you don't need a boot partition as big as mine, 500MB is more than enough) Make sure your main partition is an NTFS partition and your boot partition is FAT32.

![Partition Types](/hirens_boot_partition_tools_aomei_partition_types_000.webp)
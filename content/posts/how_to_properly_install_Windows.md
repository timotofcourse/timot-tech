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
  - windows
  - instalation
  - operating
  - system
  - windows11
  - windows10
  - hirensboot
  - winpe
  - live
# nolastmod: true
draft: false
---

You've probably installed Windows the wrong way your entire life. Let me show you the right way to do it. This method is faster and works the same as the usual method.

<!--more-->

All the process for this article was made in a virtual machine to make it easier to take screenshots but i tested and it doesn't work in the virtual machine without the proper drivers declared in WinNTSetup.

![Hiren's Boot](/hirensboot_000.webp)

Before we begin with this i'll assume you already know how to make a multibootable USB using ventoy and you've already have the Windows 10/11 iso ready. To begin with this method go to the [Hiren's Boot Website](https://www.hirensbootcd.org/), go to the downloads page and download the HBCD_PE_x64.iso and put it in your multiboot usb drive (if you use an autounattend.xml file copy it too).

![Partition Tools](/hirens_boot_partition_tools_000.webp)

Boot into Hiren's Boot and the first thing you wanna do is partition your ssd if you haven't yet. In this case i'm in a virtual machine so i don't have a main nor a boot partition so as you can see i made them with Aomei Partition Assistent (you don't need a boot partition as big as mine, 500MB is more than enough) Make sure your main partition is an NTFS partition and your boot partition is FAT32.

![Partition Types](/hirens_boot_partition_tools_aomei_partition_types_000.webp)

Now after your partitioned your SSD let's procede with the installation (you can close the partition tool you used). Open WinNTSetup.
![Where's WinNTSetup Located](/hirens_boot_system_tools.png)
![WinNTSetup](/hirens_boot_system_tools_winntsetup_000.webp)

Now select your Windows iso/wim/esd file as i did here
![Select Wim](/hirens_boot_system_tools_winntsetup_001.webp)

Now it's time to select your boot partition (make sure you select the right one, click on the arrow, not on the browse button) also if you need to format that partition you can click on the 'F' next to it.
![Select Boot Partition](/hirens_boot_system_tools_winntsetup_002.webp)

Now select your main partition(make sure you select the right one, click on the arrow, not on the browse button) also if you need to format that partition you can click on the 'F' next to it.
![Select Main Partition](/hirens_boot_system_tools_winntsetup_003.webp)

Now select the Windows edition you want to install, if your pc have a key in the UEFI firmware for a specific edition, select that edition (Ignore the DEV word)
![Select Windows Edition](/hirens_boot_system_tools_winntsetup_004.webp)

Now if you want an autounattended.xml file and or a driver folder to add add them here
![Add Drivers and Unattended xml](/hirens_boot_system_tools_winntsetup_005.webp)

Click on the 'Setup' button and check if all the things are like this then confirm
![Click Setup and check options](/hirens_boot_system_tools_winntsetup_006.webp)
![Installing](/hirens_boot_system_tools_winntsetup_007.webp)

When it asks you to reboot, reboot and you should be in the oobe or directly on your desktop depending on your autounattended.xml if you used one
![Reboot](/hirens_boot_system_tools_winntsetup_008.webp)

This method was way faster in my main machine, i have an nvme ssd and this method installed Windows in about 2 minutes compared to the 10 to 15 minutes of a regular instalation, i use an autounattended file for both methods anyway when i install Windows but this method is the fastest one. If you don't like Hiren's Boot, you can use DLC Boot, or Serguei Strelec or any other winpe graphical environment that has partition tools and WinNTSetup.
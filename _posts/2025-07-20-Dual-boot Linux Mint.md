---
layout: post
title: How To Dual-Boot Linux Mint And Windows Or macOS 
date: 2025-07-20 01:00:00 -0400
categories: guide linux
pin: false
tags: linux windows macOS
image: 
  path: /assets/img/posts/Linux-Dual-Boot.jpg
  lqip: data:image/jpeg;base64,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dzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPiA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RFdnQ9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZUV2ZW50IyIgeG1sbnM6ZGM9Imh0dHA6Ly9wdXJsLm9yZy9kYy9lbGVtZW50cy8xLjEvIiB4bWxuczpleGlmPSJodHRwOi8vbnMuYWRvYmUuY29tL2V4aWYvMS4wLyIgeG1sbnM6R0lNUD0iaHR0cDovL3d3dy5naW1wLm9yZy94bXAvIiB4bWxuczppcHRjRXh0PSJodHRwOi8vaXB0Yy5vcmcvc3RkL0lwdGM0eG1wRXh0LzIwMDgtMDItMjkvIiB4bWxuczpwaG90b3Nob3A9Imh0dHA6Ly9ucy5hZG9iZS5jb20vcGhvdG9zaG9wLzEuMC8iIHhtbG5zOnhtcD0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wLyIgeG1wTU06RG9jdW1lbnRJRD0iZ2ltcDpkb2NpZDpnaW1wOjgwZjJjYjYyLWM2NWYtNGIyYS1iZjU1LTM0ZmYzODhiNTY3YiIgeG1wTU06SW5zdGFuY2VJRD0ieG1wLmlpZDoxMmZiNjkxMC02ZWJiLTRiYmEtOTRkMC05NmNkMzYxYzM3NWUiIHhtcE1NOk9yaWdpbmFsRG9jdW1lbnRJRD0ieG1wLmRpZDpmNzAwMWZlYy0xYjRmLTQyZTctOGMxZS02NjAxZmNhNmZlNTYiIGRjOkZvcm1hdD0iaW1hZ2UvanBlZyIgZXhpZjpEYXRlVGltZU9yaWdpbmFsPSIyMDI1LTA3LTIwVDA1OjQ1OjQ2KzAwOjAwIiBHSU1QOkFQST0iMi4wIiBHSU1QOlBsYXRmb3JtPSJXaW5kb3dzIiBHSU1QOlRpbWVTdGFtcD0iMTc1Mjk5MDk0MzMzNjUzOCIgR0lNUDpWZXJzaW9uPSIyLjEwLjI4IiBpcHRjRXh0OkRpZ2l0YWxTb3VyY2VGaWxlVHlwZT0iaHR0cDovL2N2LmlwdGMub3JnL25ld3Njb2Rlcy9kaWdpdGFsc291cmNldHlwZS90cmFpbmVkQWxnb3JpdGhtaWNNZWRpYSIgaXB0Y0V4dDpEaWdpdGFsU291cmNlVHlwZT0iaHR0cDovL2N2LmlwdGMub3JnL25ld3Njb2Rlcy9kaWdpdGFsc291cmNldHlwZS90cmFpbmVkQWxnb3JpdGhtaWNNZWRpYSIgcGhvdG9zaG9wOkNyZWRpdD0iTWFkZSB3aXRoIEdvb2dsZSBBSSIgcGhvdG9zaG9wOkRhdGVDcmVhdGVkPSIyMDI1LTA3LTIwVDA1OjQ1OjQ2KzAwOjAwIiB4bXA6Q3JlYXRvclRvb2w9IkdJTVAgMi4xMCI+IDx4bXBNTTpIaXN0b3J5PiA8cmRmOlNlcT4gPHJkZjpsaSBzdEV2dDphY3Rpb249InNhdmVkIiBzdEV2dDpjaGFuZ2VkPSIvIiBzdEV2dDppbnN0YW5jZUlEPSJ4bXAuaWlkOjM3NDI5OTM4LWI0MzgtNDhhMC1hY2I5LWQzZjM1OTY4ZWQ5NyIgc3RFdnQ6c29mdHdhcmVBZ2VudD0iR2ltcCAyLjEwIChXaW5kb3dzKSIgc3RFdnQ6d2hlbj0iMjAyNS0wNy0yMFQwMTo1MTozNyIvPiA8cmRmOmxpIHN0RXZ0OmFjdGlvbj0ic2F2ZWQiIHN0RXZ0OmNoYW5nZWQ9Ii8iIHN0RXZ0Omluc3RhbmNlSUQ9InhtcC5paWQ6NzRlNjI1Y2UtMjhlMC00NDQxLWFmYTctZTQ1ODllNjcyNTViIiBzdEV2dDpzb2Z0d2FyZUFnZW50PSJHaW1wIDIuMTAgKFdpbmRvd3MpIiBzdEV2dDp3aGVuPSIyMDI1LTA3LTIwVDAxOjU1OjQzIi8+IDwvcmRmOlNlcT4gPC94bXBNTTpIaXN0b3J5PiA8L3JkZjpEZXNjcmlwdGlvbj4gPC9yZGY6UkRGPiA8L3g6eG1wbWV0YT4gICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAg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
---

# A Beginner's Guide to Dual-Booting Linux Mint

This guide will walk you through installing Linux Mint alongside your current operating system. This setup, known as "dual booting," lets you choose which OS to use when you start your computer.

### Who is this guide for?
This guide is designed for beginners with little to no Linux experience. It provides step-by-step instructions for users with a standard **Intel or AMD (x86_64) computer** running one of the following operating systems:
* **Windows** (10, 11)
* **macOS** on an Intel-based Mac (only tested with Catalina)

The goal of this tutorial is to install Linux Mint *next to* your existing operating system. It does **not** cover replacing your current OS, advanced partitioning, or installing on **ARM-based computers** (like Apple Silicon Macs or certain Windows devices).

This guide is based on the comprehensive official [Linux Mint Installation Guide](https://linuxmint-installation-guide.readthedocs.io/en/latest/), which is an excellent resource for more advanced topics and troubleshooting.

*Disclaimer & Author's Note*:
This guide was created with AI assistance and reviewed by the author, but is provided 'as-is' without warranty. You follow these instructions entirely at your own risk. The author is not responsible for any issues, including data loss, which is always a possibility when modifying your system.

### What You'll Need

- A spare USB flash drive (at least 4 GB or larger).
- At least 100 GB of free space on your computer's internal storage drive.
- A reliable internet connection.
- An external hard drive or cloud storage for backing up your files.

**IMPORTANT**: You must back up your important files before proceeding. While these steps are generally safe, there is always a risk of data loss when modifying your computer's storage.

---

## Step 1: Download the Linux Mint ISO

First, you'll need the installer file, which comes in the form of an **ISO image**.

1.  **Visit the [Linux Mint website](https://linuxmint.com/)** to download the latest version.
2.  **Choose your edition**. Linux Mint comes in a few "flavors." For newcomers to Linux Desktop, the **Cinnamon** edition is a popular choice. It’s modern, full-featured, and widely supported.[^1]
3.  **Download the 64-bit version**. Most computers made in the last decade are 64-bit, so this is almost certainly the right one for you.

---

## Step 2: Create a Bootable USB Drive

You will need a USB stick that's at least 4GB. You can't just copy the ISO file to a USB drive; you need a special tool to make it bootable.

1.  **Download and install [Etcher](https://www.balena.io/etcher/)**. It’s a free, easy-to-use tool that works on both Windows and macOS.[^2]
2.  Open Etcher and follow these three simple steps:
    * Click **"Flash from file"** and select the Linux Mint ISO file you downloaded.
    * Click **"Select target"** and choose your USB drive.
    * Click **"Flash!"** to create the bootable drive.

---

## Step 3: Make Space for Linux Mint (Partitioning)

Now, you need to make some free space on your main storage drive for Linux Mint. This is done by shrinking your current operating system's partition. A good starting point is **100 GB**, which should provide plenty of room for the system and your files. If you plan to use Linux Mint as your main OS, you may want to give it more space.

* **On Windows**:
    * *Note: For the best results, it's recommended to disable the "Fast Startup" feature in your Windows Power Options before partitioning.*
    1.  Press the Windows key and type `diskmgmt.msc` to open the **Disk Management** utility.
    2.  Right-click on your main Windows partition (usually the C: drive) and select **"Shrink Volume..."**.
    3.  Enter the amount of space to free up.
    4.  Click **"Shrink"**. You will now see a black bar of "Unallocated" space.

* **On an Intel-based Mac**:
    1.  Open **"Disk Utility"** (you can find it in Applications > Utilities).
    2.  Select your main hard drive on the left (usually named Macintosh HD).
    3.  Click the **"Partition"** button.
    4.  Click the **plus (+)** button to add a new partition.
    5.  Resize the new partition to be at least **100 GB**. Name it something like "LINUXMINT" and set the format to **ExFAT** for now—the Linux installer will reformat it correctly later.
    6.  Click **"Apply"**.

    
    **Special Note for Newer Intel Macs (2018-2020)**: 
    If your Intel Mac is from 2018 or newer, it has an Apple T2 Security Chip which blocks booting from a USB by default. Before you begin the installation process, you must change this setting. For official instructions, restart your Mac in Recovery Mode and follow [Apple's guide to using the Startup Security Utility](https://support.apple.com/en-us/102522). 
    
    In the recovery utility, apply these two settings:
    - Secure Boot: Set to "No Security".
    - Allowed Boot Media: Set to "Allow booting from external or removable media".
    
    After saving these changes, you can restart your Mac and hold the Option (Alt) key to open the boot menu and proceed with the installation.

---

## Step 4: Boot from Your USB Drive

It's time to restart your computer and boot from the USB drive you created.

1.  Plug the bootable USB drive into your computer.
2.  Restart the computer. As it starts up, you'll need to press a special key to open the **Boot Menu**.[^3]
    * *Note: If your PC does not boot from the USB, you may need to restart, enter your computer's BIOS/UEFI settings, and temporarily disable "Secure Boot".*[^4]
    * **For most PCs**, this key is `F1`, `F2`, `F10`, `F11`, `F12`, `Delete`, or `Escape`.
    * **For Macs**, hold down the **Option (or Alt)** key right after you hear the startup chime.
3.  From the boot menu, select your USB drive to boot from it.
4.  A menu will appear. Select the option to **"Start Linux Mint"** and press Enter.

Your computer will now load into a "live session" of Linux Mint. This is a fully functional temporary version running from the USB stick. It's a great way to try it out, but remember that it runs slower than a full installation, and no changes you make here are permanent.

---

## Step 5: Install Linux Mint

Once you're at the Linux Mint desktop, you can begin the permanent installation.

1.  Double-click the **"Install Linux Mint"** icon on the desktop.
2.  Follow the on-screen prompts to select your language and keyboard layout.
3.  Connect to your Wi-Fi network when prompted. This allows the installer to download updates. Tick the box to **install multimedia codecs** for full video and web compatibility.
4.  You'll reach the **"Installation type"** screen. Pay close attention here.
    * The installer should detect your other operating system and offer to **"Install Linux Mint alongside..."** it. If you see this option, select it. It's the easiest choice and will automatically handle the partitions and set up a boot menu.
    * If you don't see that option, choose **"Something else"**. Find the "free space" you created earlier, select it, and click the **plus (+)** button to create a new partition. Set it up as follows:
        * **Size**: Use all the available space.
        * **Use as**: `Ext4 journaling file system`.
        * **Mount point**: `/`.
        * Click **OK**, then **Install Now**.
5.  Continue through the final steps: select your timezone, and create your user account with a name and a strong password. For extra security, you can tick the box to **"Encrypt my home folder"**.
6.  The installation will now proceed. When it's finished, click **"Restart Now"**. The system will prompt you to remove the USB drive before rebooting.

**Note for Mac Users:** After the installation is complete, you can set Linux Mint as your default startup disk. To do this, hold down the Option key during startup to show the boot manager. Then, while holding the Control key, click the arrow under the Linux Mint volume. Your Mac will now remember this choice and boot into Linux Mint by default.

---

## Step 6: Welcome to Dual Booting!

Congratulations on your new Linux Mint installation! After logging in for the first time, it's a good idea to check for any additional hardware drivers.

From the main menu, open the **Driver Manager**. This tool will scan your system and recommend if any proprietary drivers are available for your hardware. Installing these is an important step to ensure components like your graphics card or Wi-Fi adapter perform optimally.[^5]

Enjoy your new dual-boot setup!

---
## Troubleshooting and Where to Find Help

If you run into trouble, a great place to find help is from the official Linux Mint community.

* **The [Linux Mint Forums](https://forums.linuxmint.com/):** This is a great place for finding answers and asking questions. There's a high probability someone has already solved the same problem you're facing.
* **Official Documentation:** The [Linux Mint Installation Guide](https://linuxmint-installation-guide.readthedocs.io/en/latest/) includes helpful troubleshooting tips.

---

[^1]: *Linux Mint Installation Guide*, Page 4
[^2]: *Linux Mint Installation Guide*, Page 12
[^3]: *Linux Mint Installation Guide*, Page 15
[^4]: *Linux Mint Installation Guide*, Page 33
[^5]: *Linux Mint Installation Guide*, Page 25

## Links

- [Connect with me on LinkedIn](https://www.linkedin.com/in/matthewblack/)
- [My Resume](https://drive.google.com/file/d/14V3R6QMxwq7bQzE4mC7xrCRjsQI8HOYg/view?usp=sharing)
- [Collaborate on GitHub](https://github.com/mblackonline)
- [CD Tech Chattanooga](https://www.linkedin.com/company/cd-tech-chattanooga/)
- [Community Tech Network (CTN)](https://communitytechnetwork.org/)
- [Chattanooga Technology Council (ChaTech)](https://www.chatech.org/)
- [Western Governors University (WGU)](https://www.wgu.edu/online-it-degrees/cloud-computing-bachelors-program.html)

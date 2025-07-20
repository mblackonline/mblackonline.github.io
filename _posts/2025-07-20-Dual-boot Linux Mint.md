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

# A First-Time User's Guide to Dual-Booting Linux Mint

This guide walks you through installing Linux Mint alongside your current operating system. This "dual-boot" setup lets you choose which OS to use when you start your computer.

### Who is this guide for?

This guide is for new users using a standard **Intel or AMD (x86_64) computer** running one of these operating systems:
* **Windows** (10, 11, or other recent versions)
* **macOS** on an Intel-based Mac

This guide is based on the official [Linux Mint Installation Guide](https://linuxmint-installation-guide.readthedocs.io/en/latest/), which is an excellent resource for more advanced topics.

*Disclaimer & Author's Note*: 
This guide was developed with AI assistance and reviewed by the author. It is provided for informational purposes on an "as-is" basis, without warranty. By following these instructions, you acknowledge that you do so at your own risk. The author is not liable for any issues that may occur.

### What You'll Need

* A USB flash drive (4 GB or larger).
* At least 100 GB of free space on your computer's internal drive.
* A reliable internet connection.
* An external drive or cloud storage for backing up your files.

**IMPORTANT**: Back up your important files before you begin. While these steps are generally safe, there is always a risk of data loss when partitioning a drive.

***

## Step 1: Download the Linux Mint ISO

First, you'll need the installer file, called an **ISO image**.

1.  **Visit the [Linux Mint website](https://linuxmint.com/)** to download the latest version.
2.  **Choose your edition**. For first-time users, the **Cinnamon** edition is a popular choice. It’s modern, full-featured, and widely supported.[^1]
3.  **Download the 64-bit version**. Most computers made in the last decade are 64-bit, so this is almost certainly the right choice.

***

## Step 2: Create a Bootable USB Drive

You'll need a USB stick that's at least 4GB. You can't just copy the ISO file; you need a special tool to make the drive bootable.

1.  **Download and install [Etcher](https://www.balena.io/etcher/)**. It’s a free, easy tool for both Windows and macOS.[^2]
2.  Open Etcher and follow these three steps:
    * Click **"Flash from file"** and select your downloaded Linux Mint ISO.
    * Click **"Select target"** and choose your USB drive.
    * Click **"Flash!"** to create the bootable drive.

***

## Step 3: Make Space for Linux Mint (Partitioning)

Next, you need to free up space on your main drive for Linux Mint. Shrink your current OS partition to create this space. A good starting point is **100 GB**.

* **On Windows**:
    * *Note: It's best to first disable the "Fast Startup" feature in your Windows Power Options.*
    1.  Press the Windows key and type `diskmgmt.msc` to open **Disk Management**.
    2.  Right-click your main Windows partition (usually C:) and select **"Shrink Volume..."**.
    3.  Enter the amount of space to free up and click **"Shrink"**. You will now see a black bar of "Unallocated" space.

* **On an Intel-based Mac**:
    1.  Open **Disk Utility** (in Applications > Utilities).
    2.  Select your main hard drive (usually Macintosh HD).
    3.  Click the **"Partition"** button, then the **plus (+)** button.
    4.  Resize the new partition to at least **100 GB**. Name it "LINUXMINT" and set the format to **ExFAT** for now; the installer will reformat it later.
    5.  Click **"Apply"**.

    **Special Note for Newer Intel Macs (2018-2020):** If your Intel Mac is from 2018 or newer, it has an Apple T2 Security Chip which blocks booting from a USB by default. Before you begin the installation process, you must change this setting. For official instructions, restart your Mac in Recovery Mode and follow [Apple’s guide to using the Startup Security Utility](https://support.apple.com/en-us/102522).

    - In the recovery utility, apply these two settings:
      - Secure Boot: Set to “No Security”.
      - Allowed Boot Media: Set to “Allow booting from external or removable media”.
      
      After saving these changes, you can restart your Mac and hold the Option (Alt) key to open the boot menu and proceed with the installation.

***

## Step 4: Boot from Your USB Drive

Now it's time to restart and boot from the USB drive.

1.  Plug the bootable USB drive into your computer and restart it.
2.  As it starts, press the special key to open the **Boot Menu**.[^3]
    * *Note: If your PC doesn't boot from the USB, you may need to enter your computer's BIOS/UEFI settings and temporarily disable "Secure Boot".*[^4]
    * **For most PCs**, this key is `F1`, `F2`, `F10`, `F11`, `F12`, `Delete`, or `Escape`.
    * **For Macs**, hold the **Option (or Alt)** key right after the startup chime.
3.  From the boot menu, select your USB drive.
4.  When the Linux Mint menu appears, select **"Start Linux Mint"** and press Enter.

Your computer will now load a "live session" of Linux Mint from the USB stick. This is a temporary version to try it out. It runs slower than a full installation, and no changes are saved.

***

## Step 5: Install Linux Mint

From the live desktop, you can begin the permanent installation.

1.  Double-click the **"Install Linux Mint"** icon.
2.  Follow the prompts to select your language and keyboard layout.
3.  Connect to your Wi-Fi network. This allows the installer to download updates. Tick the box to **install multimedia codecs** for full media compatibility.
4.  At the **"Installation type"** screen, pay close attention.
    * The installer should offer to **"Install Linux Mint alongside..."** your current OS. If you see this, select it. It's the easiest choice and automatically handles everything.
    * If you don't see that option, choose **"Something else"**. Find the "free space" you created, select it, and click the **plus (+)** button. Use these settings:
        * **Size**: Use all available space.
        * **Use as**: `Ext4 journaling file system`.
        * **Mount point**: `/`.
        * Click **OK**, then **Install Now**.
5.  Continue through the final steps: select your timezone and create your user account with a name and a strong password. You can tick **"Encrypt my home folder"** for extra security.
6.  When the installation finishes, click **"Restart Now"** and remove the USB drive when prompted.

***

## Step 6: Welcome to Dual Booting!

After logging in for the first time, check for additional hardware drivers.

- From the main menu, open the **Driver Manager**. This tool will scan your system and recommend any proprietary drivers for your hardware. Installing these is an important step to ensure components like your graphics card or Wi-Fi adapter perform correctly.[^5]

Enjoy your new dual-boot setup!

***

## Troubleshooting and Where to Find Help

If you run into trouble, the best place for help is the official Linux Mint community.

* **The [Linux Mint Forums](https://forums.linuxmint.com/):** A great place to find answers and ask questions.
* **Official Documentation:** The [Linux Mint Installation Guide](https://linuxmint-installation-guide.readthedocs.io/en/latest/) has helpful troubleshooting tips.

***

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

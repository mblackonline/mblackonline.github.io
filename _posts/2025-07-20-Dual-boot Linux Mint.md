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

This guide walks you through installing Linux Mint alongside your current operating system, creating a "dual-boot" setup that lets you choose which OS to use at startup.

### Who is this guide for?

New users with **Intel or AMD (x86_64) computers** running:
* **Windows** (10, 11, or recent versions)
* **macOS** on Intel-based Mac

This guide is based on the official [Linux Mint Installation Guide](https://linuxmint-installation-guide.readthedocs.io/en/latest/).

**Note for Mac Users**: This guide was tested on a 2012 MacBook Pro. If you have a different Mac model, please research whether these instructions apply to your specific computer before proceeding.

*Disclaimer*: This guide was developed with AI assistance. It's provided "as-is" without warranty. By following these instructions, you acknowledge you do so at your own risk. The author is not liable for any issues.

### What You'll Need

* USB flash drive (4 GB or larger)
* At least 100 GB free space on your internal drive
* Reliable internet connection
* External drive or cloud storage for backing up files

**IMPORTANT**: Back up important files before beginning. While generally safe, there's always risk of data loss when partitioning drives.

---

## Step 1: Download the Linux Mint ISO

1. **Visit [Linux Mint website](https://linuxmint.com/)** to download the latest version
2. **Choose your edition**:
   - **Cinnamon**: Recommended for modern computers - polished, feature-rich desktop[^1]
   - **XFCE**: For older/less powerful computers - lightweight and fast
3. **Download the 64-bit version** (correct for most computers made in the last decade)

---

## Step 2: Create a Bootable USB Drive

You need a special tool to make the USB drive bootable.

1. **Download and install [Etcher](https://www.balena.io/etcher/)** (free for Windows and macOS)[^2]
2. **Open Etcher** and follow three steps:
   * Click **"Flash from file"** and select your Linux Mint ISO
   * Click **"Select target"** and choose your USB drive
   * Click **"Flash!"** to create the bootable drive

---

## Step 3: Make Space for Linux Mint

Shrink your current OS partition to create space for Linux Mint. Allocate at least **100 GB**, or more if you plan to use Linux as your primary OS.

**On Windows**:
*Note: First disable "Fast Startup" in Windows Power Options.*
1. Press Windows key, type `diskmgmt.msc` to open **Disk Management**
2. Right-click your main Windows partition (usually C:) and select **"Shrink Volume..."**
3. Enter space amount and click **"Shrink"** - you'll see black "Unallocated" space

**On Intel-based Mac**:
1. Open **Disk Utility** (Applications > Utilities)
2. Select your main drive (usually Macintosh HD)
3. Click **"Partition"** button, then **plus (+)** button
4. Resize new partition to at least **100 GB**, name it "LINUXMINT", format as **exFAT**
5. Click **"Apply"**

---

## Step 4: Boot from USB Drive

1. **Plug in USB drive** and restart computer
2. **Press boot menu key** as it starts[^3]:
   * **PCs**: Usually `F1`, `F2`, `F10`, `F11`, `F12`, `Delete`, or `Escape` (search online to find the correct key for your computer)
   * **Macs**: Hold **Option (Alt)** key after startup chime
3. **Select USB drive** from boot menu
4. **Choose "Start Linux Mint"** from the menu

You'll now see a "live session" - a temporary version running from the USB.

---

## Step 5: Install Linux Mint

### For Windows Users

1. Double-click **"Install Linux Mint"** icon
2. Follow prompts for language, keyboard, Wi-Fi, and tick multimedia codecs box
3. At **"Installation type"**, select **"Install Linux Mint alongside Windows Boot Manager"**
4. Use slider to allocate the free space you created in Step 3 to Linux Mint
5. Click **Install Now**, complete timezone and user account setup
6. Click **"Restart Now"** when finished, remove USB when prompted

### For Mac Users

**Part A: Create Partitions with GParted**
1. Open **GParted** from main menu
2. Select the free space created in Step 3
3. Create three new partitions (right-click free space, select "New"):
   * **EFI Partition**: `1000 MB`, format as `fat32`. After creating, right-click → "Manage Flags" → check `boot` and `esp`
   * **Swap Partition**: Size equal to your RAM, format as `linux-swap`
   * **Root Partition**: Remaining space, format as `ext4`
4. Click green checkmark to apply changes, close GParted

**Part B: Run Installer**
1. Double-click **"Install Linux Mint"** icon
2. Proceed through initial screens
3. At **"Installation type"**, choose **"Something else"**
4. Assign partitions:
   * Select the `ext4` partition (root partition) → "Change..." → set "Use as:" to `Ext4 journaling file system` and "Mount point:" to **`/`**
   * `linux-swap` partition should auto-detect
5. **Crucial**: Set **"Device for boot loader installation"** to the `fat32` EFI partition
6. Click **"Install Now"**, confirm changes, complete setup
7. Restart and remove USB when finished

---

## Step 6: Choosing Your OS at Startup

**On PC**: You'll see **GRUB** menu at startup. Use arrow keys to select Linux Mint or Windows, press Enter.

**On Mac**: No GRUB menu appears. To choose OS: shut down, power on while **holding Option (Alt) key**. Click desired OS. To set default: hold **Control** and click arrow under preferred OS.

### First Login

Open **Driver Manager** from main menu to scan for and install recommended hardware drivers for optimal performance.[^5]

---

## Troubleshooting

If you run into issues, try these solutions:

### Boot Problems

**USB won't boot on Windows PC**:
- Enter BIOS/UEFI settings and temporarily disable **"Secure Boot"**[^4]
- Remember to re-enable Secure Boot after installation

**Boot issues on newer Intel Macs (2018-2020 with T2 chip)**:
1. Boot into Recovery Mode (`Command + R` at startup)
2. Open **Startup Security Utility** from Utilities menu:
   * Set **Secure Boot** to "No Security"
   * Set **Allowed Boot Media** to "Allow booting from external or removable media"
3. **Optional but recommended**: Open **Terminal** from Utilities menu and disable SIP:
4. Restart and boot from USB (hold Option key at startup)
5. **Important**: After installation, re-enable these security features by repeating steps 1-2 and reversing the settings

**Security Warning**: Disabling these security features temporarily reduces your system's protection against malware and unauthorized modifications. Re-enable them promptly after completing the Linux installation to restore full security.

### Getting Help

* **[Linux Mint Forums](https://forums.linuxmint.com/)**: Community Q&A
* **[Linux Mint Installation Guide](https://linuxmint-installation-guide.readthedocs.io/en/latest/)**: Official troubleshooting

---

[^1]: *Linux Mint Installation Guide*, Page 4
[^2]: *Linux Mint Installation Guide*, Page 12
[^3]: *Linux Mint Installation Guide*, Page 15
[^4]: *Linux Mint Installation Guide*, Page 33
[^5]: *Linux Mint Installation Guide*, Page 25


---

## Links

- [Connect with me on LinkedIn](https://www.linkedin.com/in/matthewblack/)
- [My Resume](https://drive.google.com/file/d/14V3R6QMxwq7bQzE4mC7xrCRjsQI8HOYg/view?usp=sharing)
- [Collaborate on GitHub](https://github.com/mblackonline)
- [CD Tech Chattanooga](https://www.linkedin.com/company/cd-tech-chattanooga/)
- [Community Tech Network (CTN)](https://communitytechnetwork.org/)
- [Chattanooga Technology Council (ChaTech)](https://www.chatech.org/)
- [Western Governors University (WGU)](https://www.wgu.edu/online-it-degrees/cloud-computing-bachelors-program.html)

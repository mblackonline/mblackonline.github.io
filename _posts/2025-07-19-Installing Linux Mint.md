---
layout: post
title: How To Install Linux Mint And Replace Your OS
date: 2025-07-19 12:00:00 -0400
categories: guide linux
pin: false
tags: linux windows macOS
image: 
  path: /assets/img/posts/linux_mint_install.jpg
  lqip: data:image/jpeg;base64,/9j/4AAQSkZJRgABAQEAYABgAAD/4QYmRXhpZgAASUkqAAgAAAAHABIBAwABAAAAAQAAABoBBQABAAAAYgAAABsBBQABAAAAagAAACgBAwABAAAAAgAAADEBAgANAAAAcgAAADIBAgAUAAAAgAAAAGmHBAABAAAAlAAAAP4AAABgAAAAAQAAAGAAAAABAAAAR0lNUCAyLjEwLjI4AAAyMDI1OjA3OjE5IDIzOjQxOjMyAAUAA5ACABQAAADWAAAABJACABQAAADqAAAAkZICAAMAAAAwMAAAkpICAAMAAAAwMAAAAaADAAEAAAABAAAAAAAAADIwMjU6MDc6MjAgMDM6MjI6NDMAMjAyNTowNzoyMCAwMzoyMjo0MwAJAP4ABAABAAAAAQAAAAABBAABAAAAAAEAAAEBBAABAAAAgAAAAAIBAwADAAAAcAEAAAMBAwABAAAABgAAAAYBAwABAAAABgAAABUBAwABAAAAAwAAAAECBAABAAAAdgEAAAICBAABAAAAqAQAAAAAAAAIAAgACAD/2P/gABBKRklGAAEBAAABAAEAAP/bAEMACAYGBwYFCAcHBwkJCAoMFA0MCwsMGRITDxQdGh8eHRocHCAkLicgIiwjHBwoNyksMDE0NDQfJzk9ODI8LjM0Mv/bAEMBCQkJDAsMGA0NGDIhHCEyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMv/AABEIAIABAAMBIgACEQEDEQH/xAAfAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgv/xAC1EAACAQMDAgQDBQUEBAAAAX0BAgMABBEFEiExQQYTUWEHInEUMoGRoQgjQrHBFVLR8CQzYnKCCQoWFxgZGiUmJygpKjQ1Njc4OTpDREVGR0hJSlNUVVZXWFlaY2RlZmdoaWpzdHV2d3h5eoOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4eLj5OXm5+jp6vHy8/T19vf4+fr/xAAfAQADAQEBAQEBAQEBAAAAAAAAAQIDBAUGBwgJCgv/xAC1EQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APf6KKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooASiiigRHRRRTAbRRRTAnoooqQEooooGJRRRQA6iiigAooooAKKKKACiiigBKKKKQDaKKKQC0UUUwHUUUUwCiiigAooooAw6KKK2MzjqKKK7jjLVFFFQWd3RRRXnnYY9FFFIZkUUUUAdpRRRQBXoooqRFCiiipEXqKKKYySiiikBmUUUVyCJ6KKK0GaVFFFdQx1FFFMAooooAwqKKK3MzjKKKK7TiLlFFFQaHd0UUV552GHRRRSGY1FFFIDtqKKKAKFFFFAiCiiipEX6KKKBlqiiigDHoooriELRRRQBsUUUV3FElFFFUAUUUUANooooAjooopiGUUUUxFiiiipKK9FFFADaKKKALFFFFAD6KKKAEooooAWiiigBlFFFICCiiiswEooopCLFFFFaDH0UUVQBRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFIBKKKKYBRRRQAtFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAf//Z/+ENiGh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC8APD94cGFja2V0IGJlZ2luPSLvu78iIGlkPSJXNU0wTXBDZWhpSHpyZVN6TlRjemtjOWQiPz4gPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iWE1QIENvcmUgNC40LjAtRXhpdjIiPiA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPiA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RFdnQ9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZUV2ZW50IyIgeG1sbnM6ZGM9Imh0dHA6Ly9wdXJsLm9yZy9kYy9lbGVtZW50cy8xLjEvIiB4bWxuczpleGlmPSJodHRwOi8vbnMuYWRvYmUuY29tL2V4aWYvMS4wLyIgeG1sbnM6R0lNUD0iaHR0cDovL3d3dy5naW1wLm9yZy94bXAvIiB4bWxuczp4bXA9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC8iIHhtcE1NOkRvY3VtZW50SUQ9ImdpbXA6ZG9jaWQ6Z2ltcDo0MTQyNmVlZC01NDA5LTQxMDgtOWMyNi1hZTg3ZWJkNmQwNWMiIHhtcE1NOkluc3RhbmNlSUQ9InhtcC5paWQ6N2M2ZWY4NzYtYmI1Yy00NmFjLTk5MjgtYzM3N2I5ODY1Yzc3IiB4bXBNTTpPcmlnaW5hbERvY3VtZW50SUQ9InhtcC5kaWQ6YWE3YTg0Y2QtOWJhYi00NzdiLWI3OTQtYzJjNzU2NWZmZGNlIiBkYzpGb3JtYXQ9ImltYWdlL2pwZWciIGV4aWY6RGF0ZVRpbWVPcmlnaW5hbD0iMjAyNS0wNy0yMFQwMzoyMjo0MyIgR0lNUDpBUEk9IjIuMCIgR0lNUDpQbGF0Zm9ybT0iV2luZG93cyIgR0lNUDpUaW1lU3RhbXA9IjE3NTI5ODI4OTUyMjA0MjciIEdJTVA6VmVyc2lvbj0iMi4xMC4yOCIgeG1wOkNyZWF0b3JUb29sPSJHSU1QIDIuMTAiPiA8eG1wTU06SGlzdG9yeT4gPHJkZjpTZXE+IDxyZGY6bGkgc3RFdnQ6YWN0aW9uPSJzYXZlZCIgc3RFdnQ6Y2hhbmdlZD0iLyIgc3RFdnQ6aW5zdGFuY2VJRD0ieG1wLmlpZDpmYzdhMDgwYi1mMDA5LTQ0NDktYTUyMy0xODRlOWQ3YTJlN2EiIHN0RXZ0OnNvZnR3YXJlQWdlbnQ9IkdpbXAgMi4xMCAoV2luZG93cykiIHN0RXZ0OndoZW49IjIwMjUtMDctMTlUMjM6MzY6NDMiLz4gPHJkZjpsaSBzdEV2dDphY3Rpb249InNhdmVkIiBzdEV2dDpjaGFuZ2VkPSIvIiBzdEV2dDppbnN0YW5jZUlEPSJ4bXAuaWlkOjVmYzMwNTk0LTFjNTMtNDkyZS1iNWIyLTU0ZjkxN2MxMDViNiIgc3RFdnQ6c29mdHdhcmVBZ2VudD0iR2ltcCAyLjEwIChXaW5kb3dzKSIgc3RFdnQ6d2hlbj0iMjAyNS0wNy0xOVQyMzo0MTozNSIvPiA8L3JkZjpTZXE+IDwveG1wTU06SGlzdG9yeT4gPC9yZGY6RGVzY3JpcHRpb24+IDwvcmRmOlJERj4gPC94OnhtcG1ldGE+ICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgPD94cGFja2V0IGVuZD0idyI/Pv/iArBJQ0NfUFJPRklMRQABAQAAAqBsY21zBDAAAG1udHJSR0IgWFlaIAfpAAcAFAADACUAIWFjc3BNU0ZUAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAD21gABAAAAANMtbGNtcwAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAADWRlc2MAAAEgAAAAQGNwcnQAAAFgAAAANnd0cHQAAAGYAAAAFGNoYWQAAAGsAAAALHJYWVoAAAHYAAAAFGJYWVoAAAHsAAAAFGdYWVoAAAIAAAAAFHJUUkMAAAIUAAAAIGdUUkMAAAIUAAAAIGJUUkMAAAIUAAAAIGNocm0AAAI0AAAAJGRtbmQAAAJYAAAAJGRtZGQAAAJ8AAAAJG1sdWMAAAAAAAAAAQAAAAxlblVTAAAAJAAAABwARwBJAE0AUAAgAGIAdQBpAGwAdAAtAGkAbgAgAHMAUgBHAEJtbHVjAAAAAAAAAAEAAAAMZW5VUwAAABoAAAAcAFAAdQBiAGwAaQBjACAARABvAG0AYQBpAG4AAFhZWiAAAAAAAAD21gABAAAAANMtc2YzMgAAAAAAAQxCAAAF3v//8yUAAAeTAAD9kP//+6H///2iAAAD3AAAwG5YWVogAAAAAAAAb6AAADj1AAADkFhZWiAAAAAAAAAknwAAD4QAALbEWFlaIAAAAAAAAGKXAAC3hwAAGNlwYXJhAAAAAAADAAAAAmZmAADypwAADVkAABPQAAAKW2Nocm0AAAAAAAMAAAAAo9cAAFR8AABMzQAAmZoAACZnAAAPXG1sdWMAAAAAAAAAAQAAAAxlblVTAAAACAAAABwARwBJAE0AUG1sdWMAAAAAAAAAAQAAAAxlblVTAAAACAAAABwAcwBSAEcAQv/bAEMAAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/bAEMBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/CABEIAAgAEAMBEQACEQEDEQH/xAAVAAEBAAAAAAAAAAAAAAAAAAAFCf/EABUBAQEAAAAAAAAAAAAAAAAAAAME/9oADAMBAAIQAxAAAAG6rCtEv//EABgQAAIDAAAAAAAAAAAAAAAAAAISExQl/9oACAEBAAEFAticbTf/xAAeEQACAQQDAQAAAAAAAAAAAAARExIAAiExAyJBYf/aAAgBAwEBPwGxzOVi1G1MJTA7MOCdR83Wflf/xAAiEQABAwMDBQAAAAAAAAAAAAABERITAAMhAhQiBCMyQZH/2gAIAQIBAT8BubeKzFNMmrcSMjVQyJvJEVzsrRPUS20Fs2ecpyNYx22+jny+iv/EACMQAAAEBgEFAAAAAAAAAAAAAAESEyEAAgMEERRSIjFCQ3H/2gAIAQEABj8CrtYDbbFvrvXW1X2lvFfsiTo5RIcKJczqEGZg9ZTYyPJvkf/EABoQAAIDAQEAAAAAAAAAAAAAAAERADFRQSH/2gAIAQEAAT8hYMWCg6DVUwlbf1E6gYHAdxP/2gAMAwEAAgADAAAAEOP/xAAdEQABBAIDAAAAAAAAAAAAAAARASExYQBBUaHB/9oACAEDAQE/EPcRBXh1ciwj0LHIJqe8/8QAGxEBAQADAAMAAAAAAAAAAAAAAREhMUEAYZH/2gAIAQIBAT8Q7Nwj2i+Mkx4QXkM4koq0oLokNP8A/8QAFxABAQEBAAAAAAAAAAAAAAAAAREhMf/aAAgBAQABPxAsnClk1+ZgLXvQGKhENotAmjQimj//2Q==
---

# A Beginner's Guide to Replacing Windows or macOS with Linux Mint

This guide provides a walkthrough for replacing your current operating system with Linux Mint. This process will erase your hard drive and install Linux Mint as the only OS on your computer.

### Who is this guide for?
This guide is for beginners who have decided to fully switch to Linux Mint and want to remove their existing Windows or macOS installation. It covers the process for a standard **Intel or AMD (x86_64) computer**. While this guide is specific to Linux Mint, the process should be similar for other Debian based Linux distrubutions.

This guide does **not** cover installing on **ARM-based computers** (like Apple Silicon Macs) or dual-booting.

This guide is based on the comprehensive official [Linux Mint Installation Guide](https://linuxmint-installation-guide.readthedocs.io/en/latest/), which is an excellent resource for more advanced topics like dual-booting and troubleshooting.

***

### **IMPORTANT WARNING: THIS WILL ERASE ALL YOUR DATA**
Be sure to back up all your important files to an external hard drive or a cloud storage service before you begin. Following these steps will **delete everything** on your computer's internal storage drive, including your documents, photos, applications, and your current operating system (Windows or macOS).

*Disclaimer & Author's Note*
This guide was created with AI assistance and reviewed by the author, but is provided 'as-is' without warranty. You follow these instructions entirely at your own risk. The author is not responsible for any issues, including data loss, which is always a possibility when modifying your system.

***

### What You'll Need

* A spare USB flash drive (at least 4 GB or larger).
* A reliable internet connection.
* An external hard drive or cloud storage to back up your important files.

---

## Step 1: Download the Linux Mint ISO

First, you need the installer file, which is called an **ISO image**.

1.  **Go to the [official Linux Mint website](https://linuxmint.com/)** to get the latest version.
2.  **Choose your edition**. Linux Mint is available in a few different "flavors." The **Cinnamon** edition is highly recommended for newcomers as it's modern, easy to use, and has good community support[^1].
3.  **Download the 64-bit version**. This is the correct choice for nearly all modern computers.

---

## Step 2: Create a Bootable USB Drive

You can't just copy the ISO file to your USB drive. You must use a special tool to make it bootable.

1.  **Download and install [Etcher](https://www.balena.io/etcher/)**. This is a free and simple tool that runs on both Windows and macOS[^2].
2.  Launch Etcher and complete the three steps:
    * Click **"Flash from file"** and choose the Linux Mint ISO you just downloaded.
    * Click **"Select target"** and select your USB flash drive.
    * Click **"Flash!"** to begin the process.

---

## Step 3: Boot from Your USB Drive

Now you will restart your computer using the USB drive you just created.

1.  Make sure the bootable USB drive is plugged into your computer.
2.  Restart your computer. As it powers on, you must press a specific key to open the **Boot Menu**[^3].
    * *Note: If your PC doesn't boot from the USB, you may need to enter your computer's BIOS/UEFI settings and temporarily disable the "Secure Boot" feature.*[^4]
    * **For PCs**, this key could be `F1`, `F2`, `F10`, `F11`, `F12`, `Delete`, or `Escape`.
    * **For Intel-based Macs**, hold down the **Option (or Alt)** key immediately after you hear the startup sound.
3.  In the boot menu, use the arrow keys to select your USB drive and press Enter.
4.  A menu will appear on the screen. Choose the option to **"Start Linux Mint"** and press Enter.

Your computer will now load a "live session" of Linux Mint directly from the USB. This is a temporary, fully-functional desktop. It's a great chance to look around, but remember it runs a bit slower from a USB and no changes you make will be saved.

---

## Step 4: Install Linux Mint

Once you are at the Linux Mint desktop, you can begin the installation.

1.  Double-click the **"Install Linux Mint"** icon on the desktop to launch the installer.
2.  Follow the first few prompts to select your language and keyboard layout.
3.  Connect to your Wi-Fi network. This allows the installer to download updates and other necessary files. Be sure to check the box to **install multimedia codecs**.
4.  Next is the **"Installation type"** screen. This is the most important step.
    * Since you are replacing your old operating system, choose the option to **"Erase disk and install Linux Mint"**.
    * This is the simplest and most direct method. It will automatically format the entire drive and set up the necessary partitions for you.
5.  Click **"Install Now"** and confirm that you want to write the changes to the disk.
6.  Complete the final steps: choose your timezone and create your user account with a name and a strong password. You can also check the box to **"Encrypt my home folder"** for added security.
7.  The installer will now copy all the files to your hard drive. Once it's done, click **"Restart Now"**. You will be asked to remove your USB drive before the computer reboots.

---

## Step 5: Final Checks

Congratulations! You are now running Linux Mint. After you log in for the first time, it's a good idea to check for any additional hardware drivers that could improve performance.

From the main menu, open the **Driver Manager**. This tool will scan your system and let you know if proprietary drivers are available for hardware like your graphics card or Wi-Fi adapter. Install any recommended drivers to ensure your system runs smoothly.

Enjoy your new Linux Mint system!

---

## Troubleshooting and Where to Find Help

If you run into trouble installing Linux Mint, the best place to find help is from the official Linux Mint community.

* **The [Linux Mint Forums](https://forums.linuxmint.com/):** This is a great place for finding answers and asking questions. There's a high probability someone has already solved the same problem you're facing. When asking for help, always be as detailed as possible about your computer's hardware and the exact problem you are encountering.
* **Official Documentation:** The [Linux Mint Installation Guide](https://linuxmint-installation-guide.readthedocs.io/en/latest/) includes helpful troubleshooting tips.

---

[^1]: *Linux Mint Installation Guide*, Page 4
[^2]: *Linux Mint Installation Guide*, Page 12
[^3]: *Linux Mint Installation Guide*, Page 15
[^4]: *Linux Mint Installation Guide*, Page 33

## Links

- [Connect with me on LinkedIn](https://www.linkedin.com/in/matthewblack/)
- [My Resume](https://drive.google.com/file/d/14V3R6QMxwq7bQzE4mC7xrCRjsQI8HOYg/view?usp=sharing)
- [Collaborate on GitHub](https://github.com/mblackonline)
- [CD Tech Chattanooga](https://www.linkedin.com/company/cd-tech-chattanooga/)
- [Community Tech Network (CTN)](https://communitytechnetwork.org/)
- [Chattanooga Technology Council (ChaTech)](https://www.chatech.org/)
- [Western Governors University (WGU)](https://www.wgu.edu/online-it-degrees/cloud-computing-bachelors-program.html)

---
layout: post
title: Unattended-Upgrades with Email Notifications on the Raspberry Pi
date: 2023-10-26 16:54:00 -0400
categories: raspberry-pi unattended-upgrades postfix security
pin: false
tags: raspberry-pi unattended-upgrades postfix security
image: 
  path: /assets/img/posts/unattended-upgrades.jpg
  lqip: data:image/jpeg;base64,/9j/4AAQSkZJRgABAQEAYABgAAD/4QXSRXhpZgAASUkqAAgAAAAHABIBAwABAAAAAQAAABoBBQABAAAAYgAAABsBBQABAAAAagAAACgBAwABAAAAAgAAADEBAgANAAAAcgAAADIBAgAUAAAAgAAAAGmHBAABAAAAlAAAAKYAAABgAAAAAQAAAGAAAAABAAAAR0lNUCAyLjEwLjI4AAAyMDIzOjEwOjI1IDExOjQ2OjE2AAEAAaADAAEAAAABAAAAAAAAAAkA/gAEAAEAAAABAAAAAAEEAAEAAAAAAQAAAQEEAAEAAACAAAAAAgEDAAMAAAAYAQAAAwEDAAEAAAAGAAAABgEDAAEAAAAGAAAAFQEDAAEAAAADAAAAAQIEAAEAAAAeAQAAAgIEAAEAAACrBAAAAAAAAAgACAAIAP/Y/+AAEEpGSUYAAQEAAAEAAQAA/9sAQwAIBgYHBgUIBwcHCQkICgwUDQwLCwwZEhMPFB0aHx4dGhwcICQuJyAiLCMcHCg3KSwwMTQ0NB8nOT04MjwuMzQy/9sAQwEJCQkMCwwYDQ0YMiEcITIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIy/8AAEQgAgAEAAwEiAAIRAQMRAf/EAB8AAAEFAQEBAQEBAAAAAAAAAAABAgMEBQYHCAkKC//EALUQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+v/EAB8BAAMBAQEBAQEBAQEAAAAAAAABAgMEBQYHCAkKC//EALURAAIBAgQEAwQHBQQEAAECdwABAgMRBAUhMQYSQVEHYXETIjKBCBRCkaGxwQkjM1LwFWJy0QoWJDThJfEXGBkaJicoKSo1Njc4OTpDREVGR0hJSlNUVVZXWFlaY2RlZmdoaWpzdHV2d3h5eoKDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uLj5OXm5+jp6vLz9PX29/j5+v/aAAwDAQACEQMRAD8AxaKKK7DsFooooAKKKKACiiigCOiiimAlFFFAwooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigBKKKKAL1FFFQQWKKKKQhaKKKACiiigBKKKKBiUUUUgCiiimMKKKKACiiigAooooAKKKKQhaKKKYC0UUUCEooooASiiigCrRRRVFHTUUUVgYGxRRRUCJKKKKBBRRRQMKKKKQDaKKKBhRRRQAUUUUAFFFFAwooooEFFFFADqKKKBC0UUUxBRRRQBDRRRQMwqKKKso2KKKKkk3aKKKzMySiiigBaKKKACiiigYUUUUgEooooAKKKKAFooooAKKKKYCUUUUALRRRQIWiiigBaKKKAIaKKKYzmqKKK0LLNFFFSBvUUUVBmSUUUUAFFFFAC0UUUgCiiigAooopgFFFFAC0UUUAFFFFIAooopgLRRRQA6iiikAtFFFMCGiiigZy9FFFaFliiiikB0FFFFQZktFFFIAooooAjooopFiUUUUDJaKKKZAtFFFAhKKKKYBRRRSAKKKKYDqKKKAHUUUUgCiiigCvRRRTA5WiiitDQhooopgbdFFFZkktFFFIQlFFFAyOiiigoSiiigZJRRRTIHUUUUCCiiigBKKKKACiiikAtFFFABRRRTAKKKKAIKKKKBnO0UUVqWYNFFFaGhaoooqSR1FFFIAooooASiiigAooooAWiiigAooooAKKKKACiiigAooooEFFFFAwooooAKKKKAGUUUUxFKiiirND/9kA/+ENMWh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC8APD94cGFja2V0IGJlZ2luPSLvu78iIGlkPSJXNU0wTXBDZWhpSHpyZVN6TlRjemtjOWQiPz4gPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iWE1QIENvcmUgNC40LjAtRXhpdjIiPiA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPiA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RFdnQ9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZUV2ZW50IyIgeG1sbnM6ZGM9Imh0dHA6Ly9wdXJsLm9yZy9kYy9lbGVtZW50cy8xLjEvIiB4bWxuczpHSU1QPSJodHRwOi8vd3d3LmdpbXAub3JnL3htcC8iIHhtbG5zOnhtcD0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wLyIgeG1wTU06RG9jdW1lbnRJRD0iZ2ltcDpkb2NpZDpnaW1wOjc3ZTg3ZTRkLTVkNmYtNDdhYy1hMTRmLWFlNmY4NzYyODQyOCIgeG1wTU06SW5zdGFuY2VJRD0ieG1wLmlpZDo1NDQwNDUwMy0yNDVjLTRkOWUtOTY1My03MTUzNzUxYWI4MmYiIHhtcE1NOk9yaWdpbmFsRG9jdW1lbnRJRD0ieG1wLmRpZDo2ZjU2N2YxYy0yZjUyLTQyODAtYTM5Zi04ZGI4Zjc5OTdhZjQiIGRjOkZvcm1hdD0iaW1hZ2UvanBlZyIgR0lNUDpBUEk9IjIuMCIgR0lNUDpQbGF0Zm9ybT0iV2luZG93cyIgR0lNUDpUaW1lU3RhbXA9IjE2OTgyNDg3ODEwMzQzNzUiIEdJTVA6VmVyc2lvbj0iMi4xMC4yOCIgeG1wOkNyZWF0b3JUb29sPSJHSU1QIDIuMTAiPiA8eG1wTU06SGlzdG9yeT4gPHJkZjpTZXE+IDxyZGY6bGkgc3RFdnQ6YWN0aW9uPSJzYXZlZCIgc3RFdnQ6Y2hhbmdlZD0iLyIgc3RFdnQ6aW5zdGFuY2VJRD0ieG1wLmlpZDowMjc2MGY5YS0xZDgyLTQ4MzYtOTAwMi05NDBkZWYyYWRjYWQiIHN0RXZ0OnNvZnR3YXJlQWdlbnQ9IkdpbXAgMi4xMCAoV2luZG93cykiIHN0RXZ0OndoZW49IjIwMjMtMTAtMjVUMTE6NDM6MTQiLz4gPHJkZjpsaSBzdEV2dDphY3Rpb249InNhdmVkIiBzdEV2dDpjaGFuZ2VkPSIvIiBzdEV2dDppbnN0YW5jZUlEPSJ4bXAuaWlkOjk3ZjcxOTNkLTlmN2UtNDFlYi1hOGY2LTc0NDM1ZGRiNmUyNSIgc3RFdnQ6c29mdHdhcmVBZ2VudD0iR2ltcCAyLjEwIChXaW5kb3dzKSIgc3RFdnQ6d2hlbj0iMjAyMy0xMC0yNVQxMTo0NjoyMSIvPiA8L3JkZjpTZXE+IDwveG1wTU06SGlzdG9yeT4gPC9yZGY6RGVzY3JpcHRpb24+IDwvcmRmOlJERj4gPC94OnhtcG1ldGE+ICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgPD94cGFja2V0IGVuZD0idyI/Pv/iArBJQ0NfUFJPRklMRQABAQAAAqBsY21zBDAAAG1udHJSR0IgWFlaIAfnAAoAGQAPACYAOGFjc3BNU0ZUAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAD21gABAAAAANMtbGNtcwAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAADWRlc2MAAAEgAAAAQGNwcnQAAAFgAAAANnd0cHQAAAGYAAAAFGNoYWQAAAGsAAAALHJYWVoAAAHYAAAAFGJYWVoAAAHsAAAAFGdYWVoAAAIAAAAAFHJUUkMAAAIUAAAAIGdUUkMAAAIUAAAAIGJUUkMAAAIUAAAAIGNocm0AAAI0AAAAJGRtbmQAAAJYAAAAJGRtZGQAAAJ8AAAAJG1sdWMAAAAAAAAAAQAAAAxlblVTAAAAJAAAABwARwBJAE0AUAAgAGIAdQBpAGwAdAAtAGkAbgAgAHMAUgBHAEJtbHVjAAAAAAAAAAEAAAAMZW5VUwAAABoAAAAcAFAAdQBiAGwAaQBjACAARABvAG0AYQBpAG4AAFhZWiAAAAAAAAD21gABAAAAANMtc2YzMgAAAAAAAQxCAAAF3v//8yUAAAeTAAD9kP//+6H///2iAAAD3AAAwG5YWVogAAAAAAAAb6AAADj1AAADkFhZWiAAAAAAAAAknwAAD4QAALbEWFlaIAAAAAAAAGKXAAC3hwAAGNlwYXJhAAAAAAADAAAAAmZmAADypwAADVkAABPQAAAKW2Nocm0AAAAAAAMAAAAAo9cAAFR8AABMzQAAmZoAACZnAAAPXG1sdWMAAAAAAAAAAQAAAAxlblVTAAAACAAAABwARwBJAE0AUG1sdWMAAAAAAAAAAQAAAAxlblVTAAAACAAAABwAcwBSAEcAQv/bAEMAAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/bAEMBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/CABEIAAgAEAMBEQACEQEDEQH/xAAVAAEBAAAAAAAAAAAAAAAAAAABB//EABYBAQEBAAAAAAAAAAAAAAAAAAEEBf/aAAwDAQACEAMQAAABv9mmJ//EABgQAAMBAQAAAAAAAAAAAAAAAAIDBgQH/9oACAEBAAEFAkT8AaNU9z4Mv//EAB4RAAEDBAMAAAAAAAAAAAAAAAECESEABAUSFDKx/9oACAEDAQE/AeXkAVtswMAo8ihe5EqT3AcRoa//xAAiEQABAgMJAAAAAAAAAAAAAAABAAIEBSEDERITIkNhceH/2gAIAQIBAT8BdGzMOIGaKnb8TI2Z4mgm1NRfo56X/8QAHhAAAQQCAwEAAAAAAAAAAAAAAQIDBBIRIQATIlH/2gAIAQEABj8CYLsiFdTaCrM06VUWz61vklbciF2JZcLeJhJuEmuPX3n/xAAaEAEAAwADAAAAAAAAAAAAAAABABEhMUFR/9oACAEBAAE/IcjClKNTzaz2UsWStIDK4o7n/9oADAMBAAIAAwAAABAP/8QAGxEBAQACAwEAAAAAAAAAAAAAAREhMQBxgbH/2gAIAQMBAT8QHyoCApYQZIS6nhKtYSCGpunWPq8//8QAGxEBAQACAwEAAAAAAAAAAAAAAREhQQAxgeH/2gAIAQIBAT8QYkAsCQs0uMD84oiJVJIPKd9ze3n/xAAXEAEBAQEAAAAAAAAAAAAAAAABEQAh/9oACAEBAAE/EGyHoIyjGQQcEgGYlL2TjaiEGkI7/9k=
---

# Keeping Your Raspberry Pi Secure with Unattended Upgrades

In my previous post, I talked about [Setting up an SFTP Server on Raspberry Pi for Obsidian Sync.](https://www.matt-black.tech/posts/SyncFTP-Obsidian/) While it's easy to keep your Pi's software up-to-date manually, I thought it would be nice to automate the process to save time and effort. 

To prevent hackers from exploiting old software flaws, it is best to install security patches as soon as they are released. The ‘unattended-upgrades’ package on Debian-based systems (like Raspberry Pi OS) does this automatically for you.

In this post, we'll go over how to install and configure unattended-upgrades to help harden your Raspberry Pi against attacks. We'll also set up the postfix mail transfer agent to send email notifications when updates are performed.

**Caution** - While automatic updates can be convenient, they also come with risks like unwanted changes or new software bugs. You should check your system’s status and updates regularly, for example, by using log files or notification systems. You should also backup your data often, especially in production environments.

---

## An Overview of Unattended Upgrades

The unattended-upgrades package provides automatic package updates for Debian-based systems (e.g. Raspberry Pi OS, Ubuntu, Linux Mint, Zorin OS, etc.). Once enabled and properly configured, it will automatically download and install apt package updates without the need for user interaction.

#### **Some key features of unattended-upgrades:**

- Can focus solely on security updates and ignore non-security packages, or can be configured to install all updates.
- Can automatically reboot the server after installing updates, if needed.
- Email notifications can be provided to give update status and details.
- Blacklisting allows excluding certain packages from auto-updates.

#### ***---***  **Prerequisites/Assumptions in this guide:**
  * You have a Raspberry Pi running Raspberry Pi OS.
  * You already have SSH access to your Pi (or you can access the Pi terminal by some other login method like direct access or VNC).
  * You have a Gmail account to use for email notifications.
  * You have a basic understanding of how to use the Linux terminal.

# Part 1: Installing and Configuring Unattended Upgrades

### 1. Login into the Pi via SSH (or any other means that you find convenient)

```bash
ssh your-Pi-userName@raspberrypi-hostname
```
**Note**: The default user should be `pi`, and the default hostname is typically `raspberrypi`. It would be wise to change these to something else if you haven't already done so. You could also use the Pi's IPv4 address or its [FQDN](https://en.wikipedia.org/wiki/Fully_qualified_domain_name) instead of the hostname if you prefer.

### 2. Update the Apt Package Manager and Upgrade Existing Packages
```bash
sudo apt update && sudo apt upgrade -y && sudo reboot
```
*This will update your existing packages and reboot the Pi. Wait for the Pi to reboot and then log back in using the above SSH commands.*

### 3. Install Unattended Upgrades and Power Management Base

Installing unattended-upgrades and power management is simple - just run the following command in your terminal:

```bash
sudo apt install unattended-upgrades -y && sudo apt install powermgmt-base -y
```

### 4. Enable Unattended Upgrades
Enable unattended-upgrades to run automatically by running the following command: 

```bash
sudo dpkg-reconfigure --priority=low unattended-upgrades
```
At the confirmation prompt, select **Yes** to enable unattended upgrades.

### 5. Configure Unattended Upgrades

The main configuration file for unattended-upgrades is located at /etc/apt/apt.conf.d/50unattended-upgrades. To open the 50unattended-upgrades file in a terminal-based text editor such as nano, run the following command:

```bash
sudo nano /etc/apt/apt.conf.d/50unattended-upgrades
```
  - *If you're unfamiliar with how to use nano, you can find a [quick reference guide here](https://www.nano-editor.org/dist/latest/cheatsheet.html).*

### 6. Select Which Updates To Activate

To enable automatic package downloads and installation of security updates, look for the below line in the 50unattended-upgrades file and make your settings match the following:

```bash
Unattended-Upgrade::Origins-Pattern {
        // Codename based matching:
        // This will follow the migration of a release through different
        // archives (e.g. from testing to stable and later oldstable).
        // Software will be the latest available for the named release,
        // but the Debian release itself will not be automatically upgraded.
        "origin=Debian,codename=${distro_codename}-updates";  // this line enables regular package updates from the Debian archive
//      "origin=Debian,codename=${distro_codename}-proposed-updates";
        "origin=Debian,codename=${distro_codename},label=Debian";  // this line enables non-security updates labeled as 'Debian' from the Debian archive
        "origin=Debian,codename=${distro_codename},label=Debian-Security"; // this line enables security updates from the Debian archive
        "origin=Debian,codename=${distro_codename}-security,label=Debian-Security"; // this line enables security updates from the Debian archive
        "origin=Raspbian,codename=${distro_codename},label=Raspbian"; // this line enables non-security updates labeled as 'Raspbian' from the Raspbian archiv
        "origin=Raspberry Pi Foundation,codename=${distro_codename},label=Raspberry Pi Foundation"; // this line enables non-security updates labeled as 'Raspberry Pi Foundation' from the Raspberry Pi Foundation archive

        // Archive or Suite based matching:
        // Note that this will silently match a different release after
        // migration to the specified archive (e.g. testing becomes the
        // new stable).
//      "o=Debian,a=stable";
//      "o=Debian,a=stable-updates";
//      "o=Debian,a=proposed-updates";
//      "o=Debian Backports,a=${distro_codename}-backports,l=Debian Backports";
};
```
**Note**, you will need to uncomment lines that you want to activate by removing the `//` to the left of the line. To enable Raspberry Pi OS-specific updates, you'll also need to add the origin patterns for Raspbian and Raspberry Pi Foundation to the above list. 

### 7. Enable Auto-Reboot After Updates 

To automatically reboot the server after updates that require it, find the following line in the 50unattended-upgrades file and make your settings match the following:

```bash
Unattended-Upgrade::Automatic-Reboot "true";
```

Be aware that this will reboot your server without warning, so plan maintenance windows accordingly. You can set a specific time for the reboot to occur by uncommenting the following line to activate it and setting the time to your desired value:

```bash
Unattended-Upgrade::Automatic-Reboot-Time "02:00";
```

**NOTE** - if you do not want to enable email notifications, you can stop right here. But if you do want to enable email notifications, keep reading...

---
---
# Part 2. Configuring Email Notifications with Postfix

### 8. Enable Email Notifications

To receive email notifications when updates are performed, add your email address to the following line in the 50unattended-upgrades file:

```bash
Unattended-Upgrade::Mail "your-email-address@example.com";
```

### 9. Create an App Password for Gmail
To use Gmail for our email notifications, we will need to get a Gmail App Password. To do this, follow this guide from Google: [How to generate App Passwords](https://knowledge.workspace.google.com/kb/how-to-generate-an-app-passwords-000009237). 

**Important**- Be sure to copy the password to a safe place once it is generated, as you will not be able to view it again after closing the window.

### 10. Install Postfix for Email Notifications

To enable the email notifications from unattended-upgrades, we'll be using the [postfix](https://wiki.debian.org/Postfix) application. 
- Postfix is a mail transfer agent (MTA) that can be used to send and receive email.
- For our purposes, we will only configure postfix to send email notifications from unattended-upgrades. 
- When installing postfix, you'll be prompted to enter your system mail name, which should be your Pi's domain name. Use the following terminal command to get this before installing postfix and jot it down for later use:

```bash
hostname -f
```

- To install postfix, run the following command in your terminal:

```bash
sudo apt install postfix -y
```
During the postfix configuration select **"Internet Site"**, and specify your Raspberry Pi's domain (from above) as the "mail name."

- *__TIP__ - I found the following guide from Tony Florida to be very helpful for learning how to set this up: (https://tonyteaches.tech/postfix-gmail-smtp-on-ubuntu/)*

### 11. Configure the settings for [Simple Authentication and Security Layer (SASL)](https://en.wikipedia.org/wiki/Simple_Authentication_and_Security_Layer) 
- *SASL provides a method for adding authentication support for Postfix to allow us to send email through our Gmail account.*

**Check to make sure that the /etc/postfix/sasl/ directory exists by running `ls -la /etc/postfix` in your terminal.** You should see the sasl directory in the output. If the directory doesn’t exist, you can create it using the mkdir command as follows:
```bash
sudo mkdir -p /etc/postfix/sasl/
```
- *The -p option tells mkdir to create parent directories as needed.*

- Now create a file named `sasl_passwd` in the /etc/postfix/sasl/ directory by running the following command in your terminal:
```bash
sudo touch /etc/postfix/sasl/sasl_passwd
```
- And add your email address and Google App password to the sasl_passwd file by running the following command in your terminal:
```bash
sudo nano /etc/postfix/sasl/sasl_passwd
[smtp.gmail.com]:587 your-email@gmail.com:your-app-password 
```
**Note** - there should be no spaces between the characters in your Gmail App Password.

### 12. Next, we will use the [postmap](https://man.archlinux.org/man/postmap.1.en) command to create a database file from the sasl_passwd file we just created. 
- To do this, run the following command in your terminal:

```bash
sudo postmap /etc/postfix/sasl/sasl_passwd
```
- If you look in the directory at /etc/postfix/sasl, you should now see a new file named sasl_passwd.db.
- This file is used by Postfix to authenticate with Gmail when sending email. ([See this guide for more details.](https://tecadmin.net/postfix-configure-sasl-authentication-for-remote-smtp/))

### 13. Now we need to change the permissions to make sure that only the root user can read or write to the sasl_passwd and sasl_passwd.db files. To do this, run the following commands in your terminal:

```bash
sudo chown root:root /etc/postfix/sasl/sasl_passwd /etc/postfix/sasl/sasl_passwd.db
sudo chmod 0600 /etc/postfix/sasl/sasl_passwd /etc/postfix/sasl/sasl_passwd.db
```

We're almost done, I promise...hang in there! 😊 

### 14. Now we need to configure the main postfix configuration file:

The main configuration file for postfix is in the following directory: /etc/postfix/main.cf. To open the main.cf file in a terminal-based text editor such as nano, run the following command:

```bash
sudo nano /etc/postfix/main.cf
```

Then find the following `relayhost =` line, and change your settings to match the following:

```bash
relayhost = [smtp.gmail.com]:587
```

### 15. Add the following lines to the bottom of the main.cf file (credit to Tony Florida's guide [here](https://tonyteaches.tech/postfix-gmail-smtp-on-ubuntu/)):

```bash
# Enable SASL authentication
smtp_sasl_auth_enable = yes
smtp_sasl_security_options = noanonymous
smtp_sasl_password_maps = hash:/etc/postfix/sasl/sasl_passwd
smtp_tls_security_level = encrypt
smtp_tls_CAfile = /etc/ssl/certs/ca-certificates.crt
```

### 16. Restart postfix with the following command:

```bash
sudo systemctl restart postfix
```

### 17. Now let's test to make sure that postfix is working properly. To do this, we can use the sendmail command to send a test email. Run the following command in your terminal:

``` bash
sendmail your-email@example.com
## You'll see output that looks like this: 
  ## sendmail: warning: /etc/postfix/main.cf, line 53: overriding earlier entry: smtp_tls_security_level=may
  ## postdrop: warning: /etc/postfix/main.cf, line 53: overriding earlier entry: smtp_tls_security_level=may
To: your-email@example.com
Subject: Testing Postfix
This is a test email to make sure postfix is working properly
```
If you receive the email, then you're good to go! If not, you may need to troubleshoot your postfix configuration.

## Conclusion

Keeping your Linux systems up-to-date with the latest security patches is vital for defense against attacks. Manually applying updates is time-consuming and inefficient. Using the unattended-upgrades package automates the process of installing security updates in the background and makes the process much more efficient. Additionally, configuring email notifications via postfix provides visibility into update activity.

I hope this guide was helpful! If you have any questions or comments, please feel free to reach out to me on [LinkedIn](https://www.linkedin.com/in/matthewblack/) or by [email](mailto:mblackonline.git@gmail.com). 


## Links

- [Connect with me on LinkedIn](https://www.linkedin.com/in/matthewblack/)
- [My Resume](https://media.licdn.com/dms/document/media/D562DAQECYUI9cjzZ2Q/profile-treasury-document-pdf-analyzed/0/1697120496637?e=1698278400&v=beta&t=t-vspXsgS1XuIjc3vFtS9J4TphRyj8B5ZJ1QSS8voTA)
- [Collaborate on GitHub](https://github.com/mblackonline)
- [CD Tech Chattanooga](https://www.linkedin.com/company/cd-tech-chattanooga/)
- [Community Tech Network (CTN)](https://communitytechnetwork.org/)
- [Chattanooga Technology Council (ChaTech)](https://www.chatech.org/)
- [Western Governors University (WGU)](https://www.wgu.edu/online-it-degrees/cloud-computing-bachelors-program.html)
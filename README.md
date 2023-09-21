# Bypass Account Creation when installing Windows 10/11
Instructions for how to install Windows 10/11 without needing to create a Microsoft account. Also works for bypassing school/work account requirement :)

_Simplified version of this tutorial: https://www.makeuseof.com/rufus-bypass-tpm-secure-boot-requirements-windows-11/_

## TL;DR
1. Use [Rufus](https://rufus.ie/) to strip the Windows ISO file from any restrictions
2. Use Rufus to Create a bootable Windows installation drive
3. Install Windows on your desired computer with local account

> <img src="https://github.com/Prid13/Windows-10-11-Bypass-Account-Creation/assets/27897747/34821eb7-3c25-4364-ab34-7fd601969d49" width="400">
_this is the important step that bypasses the restrictions. it's in the program Rufus right before creating the bootable drive_

## Prerequisities
You will need these things:
- **ONE external storage device** (minimum 6-8GB, not used for anything else):
  - ![USB Drive](https://cdn-icons-png.flaticon.com/24/7397/7397713.png) USB Drive
  - ![HDD](https://cdn-icons-png.flaticon.com/24/7397/7397679.png) External Hard-Disk / SSD
- **6-8GB of free storage on your computer**/storage device
  - _this can be bypassed by directly downloading the Windows installation file to the USB drive/HDD/SSD_
 
## Table-of-Contents
1. Install Rufus
2. Download Windows ISO file
3. Configure settings
4. Create bootable external drive (USB/HDD/SSD)
5. Install Windows on new computer

## 1. Install Rufus

Rufus is a tool to create a bootable Windows installation drive, so that you can use a USB, HDD or SSD to install Windows on another computer.

1. **Go to Rufus' website**: https://rufus.ie/
2. Scroll down to "Download" section
3. **Download** your desired version (choose the top link if you're unsure)

<img src="https://github.com/Prid13/Windows-10-11-Bypass-Account-Creation/assets/27897747/e14dc8f1-3a5b-4e3f-b423-2ca9d2d07e13" width="500">

## 2. Set up Rufus

1. **Open Rufus** by opening the file you installed (e.g. `rufus-4.2.exe`)
2. Click **Yes** when the admin prompt shows up
3. **Plug in your external drive** (your USB drive, or HDD / SSD, depending on what you have)
> [!WARNING]  
> **Everything in the external drive will be deleted!** make sure it's _**empty**_ OR not does contain important files.
4. Under **Device**, choose your plugged-in external drive (e.g. `KINGSTON (D:) [8 GB]`)

## 3. Download Windows ISO file

### EASY Way

1. **From within Rufus**, find the **SELECT** button, and **click on its arrow** (right-hand side)
2. **Choose DOWNLOAD**
> <img src="https://github.com/Prid13/Windows-10-11-Bypass-Account-Creation/assets/27897747/ce6f632e-cff2-4aa9-9326-4650d66c9e3f" width="400">
3. Then **click on the DOWNLOAD button** (not the arrow, this time, on the button itself)
   - Wait a few seconds for things to get ready
   - A popup will appear
> <img src="https://github.com/Prid13/Windows-10-11-Bypass-Account-Creation/assets/27897747/279c6f22-bf3a-4a8c-b07a-cc4f790a6ef5" width="300">
4. **Choose the Windows version you want**, and **click Continue**
   - Wait a few seconds, it might be a bit slow (probably fetching info from the internet)
5. Choose **Release**, and **click Continue**
6. Choose **Edition**, and **click Continue**
7. Choose **Language**, and **click Continue**
8. Choose **Architecture** ([check if you target computer is 32-bit or 64-bit]([url](https://support.microsoft.com/en-us/windows/32-bit-and-64-bit-windows-frequently-asked-questions-c6ca9541-8dce-4d48-0415-94a3faa2e13d)https://support.microsoft.com/en-us/windows/32-bit-and-64-bit-windows-frequently-asked-questions-c6ca9541-8dce-4d48-0415-94a3faa2e13d))
> <img src="https://github.com/Prid13/Windows-10-11-Bypass-Account-Creation/assets/27897747/d3bcd77b-651d-445f-ba4e-d3b3027296a0" width="300">
9. Finally, **click Download**, choose where the .iso file will be downloaded, and hit OK to start

<img src="https://github.com/Prid13/Windows-10-11-Bypass-Account-Creation/assets/27897747/8a996645-11fb-4dd9-ba83-795711513a13" width="300">

### Alternate Way

For whatever reason, if you're unable to do it the easy way, or get errors, then:
1. Find your desired Windows ISO file from wherever
   - Some links where you can find ISO files:
     - https://mirror.mika.moe/
     - https://www.uup.ee/
     - https://www.heidoc.net/joomla/technology-science/microsoft/67-microsoft-windows-and-office-iso-download-tool
2. In Rufus, click on SELECT (not DOWNLOAD), choose your ISO file, and hit OK

## 4. Configure Settings

You may leave all the settings to default before creating the bootable drive, but you're also free to configure things as you want here:

<img src="https://github.com/Prid13/Windows-10-11-Bypass-Account-Creation/assets/27897747/7a319a0b-3b6a-45cd-8c48-535dd5d00638" width="300">

## 5. Create bootable drive, and Bypass Windows restrictions

1. Once done, **click on the START button** at bottom in Rufus to start
> <img src="https://github.com/Prid13/Windows-10-11-Bypass-Account-Creation/assets/27897747/4c48315f-667b-4c5b-aaef-d57baff92f80" width="300">
2. **A popup with options will appear**
3. **Check the two top-most options**, and optionally check all the others as well. Hit OK once done.
> <img src="https://github.com/Prid13/Windows-10-11-Bypass-Account-Creation/assets/27897747/34821eb7-3c25-4364-ab34-7fd601969d49" width="500">
4. A final warning will appear telling you that _everything in your external drive **will be wiped**_. Hit OK if you want to proceed.
> <img src="https://github.com/Prid13/Windows-10-11-Bypass-Account-Creation/assets/27897747/583b1de2-a04e-4498-87f9-a3a4185788a2" width="300">
5. Your bootable drive is being made. This may take some time :)

## 6. Install Windows on new computer

Once your bootable drive is made using Rufus, do this:

1. Unplug your external drive (e.g. USB), and **plug it in your target computer/laptop** (where you want to install Windows)
2. On that target computer, **enter BIOS mode** and **re-order boot devices so that your external drive is at top**
   - this will be different depending on your computer/laptop. Look up tutorials on your model and make to figure this step out
   - this step is necessary to make your computer run off of your external drive (e.g. USB) when booting
3. Reboot your computer, so that it enters your external drive, and then **install Windows from there** by following the instructions

If all went well, then you will NOT be asked to provide any Microsoft account during installation, and your local account will already be set up with the name you chose in Rufus :)

This is repo contains efi file for Lenovo Thinkpad X270:

![picture home screen](images/../images/Home-Screen.png)

# Spec

💻 Laptop: 
- <b>Merk</b> : Lenovo Thinkpad x270
- <b>Processor</b> : i5-6300U (Skylake-U)
- <b>igpu</b> : Intel(R) HD Graphics 520
- <b>RAM</b> : 16GB DDR4 2133 Mhz
- <b>Audio</b> : Realtek ALC298 @ Intel Sunrise Point-LP PCH - High Definition Audio Controller
- <b>Trackpad</b> : HID-Compilant Mouse
- <b>Storage</b> : SSD SATA 128 + 128 GB
- <b>Wireless + bluetooth</b> : Intel(R) Dual Band Wireless-AC 8260
- <b>Ethernet</b> : Intel(R) Ethernet Connection I219-LM
- <b>Bootloader</b> : Opencore 0.9.7
- <b>OS Version</b> : MacOS Ventura 13.6.3
- <b>Installer offline</b> : olarilla

# Bios settings

<b>Security</b>
- `Security Chip` **Disabled**
- `Memory Protection -> Execution Prevention` **Enabled**
- `Virtualization -> Intel Virtualization Technology` **Enabled**
- `Virtualization -> Intel VT-d Feature` **Enabled**
- `Anti-Theft -> Computrace -> Current Setting` **Disabled**
- `Secure Boot -> Secure Boot` **Disabled**
- `Intel SGX -> Intel SGX Control` **Disabled**
- `Device Guard` **Disabled**

<b>Startup</b>
- `UEFI/Legacy Boot` **UEFI Only**
- `CSM Support` **No**


# Customization

Custom command for fix lagging when maximize and minimize window:

`defaults write -g NSWindowResizeTime -float 0.001`
 
To restore animation time you must use this command:

`defaults delete -g NSWindowResizeTime`

If the desired time zone is not available, you can manually set the time zone using the following command in your terminal:

1. In your terminal, use the below command to find out the available time zones. Go through the different time zones and find yours:

    `sudo systemsetup -listtimezones | more`

2. Next, set your timezone to the one you want. In this example, I'll be setting the timezone to Asia/Jakarta

    `sudo systemsetup -settimezone Asia/Jakarta`

3. Verify that you have set the timezone correctly

    `sudo systemsetup -gettimezone`

# What's Working?
- [x] Intel HD 520 Graphics (incuding graphics acceleration)
- [x] CPU Power Management
- [x] Battery
- [x] All USB ports
- [x] HDMI port (including HDMI Audio)
- [x] Intel Ethernet port
- [x] Realtek Audio (including headphones jack)
- [x] Internal camera (including Facetime)
- [x] Trackpad (gestures work but not the trackpad click. tap to click works.)
- [x] Shutdown / Reboot 
- [x] Keyboard (incuding all fn Keys)
- [x] Wi-Fi & Bluetooth (including Apple services)
- [x] iMessage, FaceTime, App Store, iTunes Store (with valid smbios)
- [x] Sleep / Wake (lid sleep and lid wake) 

# What's not working ⚠️
- [x] DRM support (iTunes Movies, Apple TV+, Amazon Prime and Netflix, and others) but you can use browser support DRM


Thanks ☕
# AndroidKitKatUTM
Run [Android-x86](https://www.android-x86.org/)’s [KitKat](https://developer.android.com/about/versions/kitkat?hl=zh-tw) OS in [UTM](https://docs.getutm.app/).Works on all Apple devices with [UTM](https://docs.getutm.app/) or [UTM SE](https://apps.apple.com/hk/app/utm-se-retro-pc-emulator/id1564628856)installed.
# Prerequisite 
• Any iOS/iPadOS/MacOS device with [UTM](https://docs.getutm.app/) or [UTM SE](https://apps.apple.com/hk/app/utm-se-retro-pc-emulator/id1564628856) installed.[(Install Guide)](https://getutm.app/install/)

• Need at least 512MB memory for the VM.

• JIT is not strictly required. But you are recommended to use JIT via [Stikdebug](https://stikdebug.xyz/) or [Trollstore](https://github.com/opa334/TrollStore) etc for a faster performance.
# Installation
Step 1: Everything from prerequisite 

Step 2: Go to [UTM](https://docs.getutm.app/) settings->touch input->change to touch mode(try hiding curser)

Step 3: Two paths

Path 1: 

Step 4: Download the *.zip from releases and unzip it into a desired destination in the Files app or UTM folder, you will see a .utm folder there.

Step 5: Enable JIT(Optional)

Step 6: Boot the VM and play!

Path 2:

Step 4: Download the Android-x86 4.4-r1 install iso from a trusted source like [Internet Archive](https://archive.org/details/sjarb_android_4.4r1). Not the x86_64 one.

Step 5: Create a new VM, select Emulation, or virtualization if you are on x86 Mac. Select OS as Windows. Toggle UEFI boot and install Windows 10 or later to off. Tap browse and attach the downloaded iso.

Step 6: Click next, and assign at least 512 MB ram to the VM.Click next again, and assign no less than 8GB storage to the VM on the next screen. Skip shared directory and change the VM’s name and icon if you want.

Step 7: Now boot.

Step 8: After entering the menu, select installing Android-x86 to harddisk and in the next popup choose create/modify partitions.

Step 9: In the partition table, choose New->Logical->Press enter on next screen->Bootable->Write->Type ‘yes’ manually->(wait a sec)Quit 

Step 10: Choose sda5 and choose ext3 next. Choose yes when asking if you want to write sda5 to ext3, and install boot loader GRUB. Install /system directory as read and write.(wait a sec)

Step 11: Choose reboot and then eject the iso.(press the 💿 icon, tap your attached iso and eject it)

Step 12: Hightlight the option “Android-x86 4.4-r1” and boot it, and be welcomed by the setup wizard! Installation successful!
# Extra 
1, Change resolution especially for iPhones

Go to the Terminal Emulator app in the VM and type `su` and grant superuser rights;

type `wm size 720x1280`to change the resolution and make it fit the iPhone screen;

type `wm density 350` to make the text larger

type `reboot` 

2, Broken Launcher app icon movement

Both the Trebuchet Launcher or third party Nova Launcher are facing issues moving the app icons, they may drop back to the original slot before you can even move them to the desired place.

Please continually try to move the icon, because it works sometimes, but it may be really time consuming and ‘finger aching’.

3, No modern web

The VM connects to the internet, but the built in browser is ancient Chromium 30, you obviously cannot browse modern webpages, other side loaded browsers always fail, the reason is unclear. 

You are highly recommended to install the [ISRG Root X1 certificare from Lets Encrypt](https://letsencrypt.org/certificates/) which fix connection issues only.

```diff+ If you want to download files, the most reliable way is to download it on your iPhone and transfer it into the VM with a local file hoster app over wifi. ```

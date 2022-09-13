Those are outputs of helper commands on the indonesian based telegram group. Very helpfull resources are there. Some of those notes here are translated. To be sure, enter the chat there:

https://t.me/R10ID_Update
***
```
Daftar catatan dalam Redmi 10 (2021/2022) || Selene/Selenes Indonesia 🇮🇩:
- backupimei
- boot
- dns
- fix_mount/cust_twrp
- flash_gsi
- flash_rom
- flash_twrp
- global
- install-gsi
- kumpulan_boot.img
- linkgrup
- magisk
- mbank
- mtk_exploit
- oot
- payload_dumper
- recovery
- restore_imei
- root
- screenrecord
- tools
- tool_unbrick_selene
- twrp_pemanen
- ubl
- ublinstan
- unbrick
- vbmeta
```
# backupimei
```
sptool - https://www.youtube.com/watch?v=BDb8t9g6KVs
twrp - backup everything?
```
# boot
`file`
# dns
a dns list?
# fix_mount/cust_twrp
```
How to Fix In TWRP it says "failed to mount /cust" after UNBRICK

Take the cust.img file in the Firmware Folder that was flashing

Move to platform tools folder

Keep opening CMD from platform tools

Type in cmd fastboot flash cust cust.img

Enter wait until it's finished

Type again in cmd Fastboot reboot
```
# flash_gsi
```
GUIDE FLAH GSI ON TWRP

1.fastboot devices

2.fastboot --disable-verity --disable-verification flash vbmeta vbmeta.img

3.fastboot reboot fastboot

4.fastboot getvar is-userspace

5.fastboot erase system

note :
Erasing 'system_a'
Erasing 'system_b'

6.fastboot delete-logical-partition product_ ....

note : ....
if what appears above Erasing 'system_a' means fastboot delete-logical-partition product_a
if what appears above Erasing 'system_b' means fastboot delete-logical-partition product_b

7.fastboot flash system namaromGSI.img

8.fastboot reboot recovery


USE ONLY ON TWRP LATEST BUILD
```
# flash_rom
```
Tutorial Install Cusrom Selene

Requirements :

- BRAIN ( Seriously, you all gonna really need that, otherwise you are zombies )
- Unlocked Bootloader
- PC / Laptop with working adb fastboot, SP Flash Tools
- recovery and fastboot MIUI Stock ROM ( ID, EEA, Global, CN, Taiwan / pick one that work, or your currently ROM Version )
- put your recovery ROM to Microsd / OTG

How To : (If you never update OTA then go STEP 1, else go STEP 2)

- BACKUP YOUR IMEI FIRST ‼️‼️

STEP 1
- boot to fastboot mode
- flash twrp / ofox  "fastboot flash boot namatwrp.img "
- reboot recovery  "fastboot reboot recovery"
- Format Data
- install / flash MIUI Recovery rom, check reflash TWRP / OFOX
- reboot to "BOOTLOADER"
- flash vbmeta " fastboot --disable-verification --disable-verity flash vbmeta vbmeta.img "
- reboot  "fastboot reboot " ( if success booting up to system go to STEP 2, if not success, read again from start )

STEP 2
- no need to setup anything, you can skip all that MIUI Setup wizard, just reboot to fastboot again
- flash twrp / ofox  "fastboot flash boot namatwrp.img "
- reboot recovery  "fastboot reboot recovery"
- Format Data
- install / flash Custom rom with Automatically reflash TWRP after flashing a ROM checked
- reboot ( If you skipped STEP 1 and not booting, back to fastboot or TWRP, then Go to STEP 1 first, if can't boot to either TWRP / Fastboot, Then you need MTK Bypass + SP Flash Tool)
- ( If you DONE STEP 1 but still no luck check SPECIAL CASE )
- DONE

SPECIAL CASE
If your device still reboot back to recovery after all that step, especially some Samsung emmc varian and NFC varian. or another gacha, do this :
- reboot to recovery, flash another Custom ROM boot.img to boot partition, and re flash TWRP/OFOX, reboot
- if still not booting, try flash MIUI boot.img, then re flash TWRP/OFOX, reboot
- if booting succesfully, you need to reboot to recovery again to flash any custom kernel, because your wifi, bluetooth etc is DEAD
```
# flash_twrp
```
Guide boot to system after install TWRP/PBRP
1. copy twrp.img and stock boot.img in internal memory or sdcard
2. in TWRP menu chose install select image
3. select stock boot.img
4. select boot partition
5. don't reboot system
6. in TWRP menu chose install select image
7. select TWRP.img
8. select install recovery ramdisk
9. finish reboot system
```

# global
```
@Redmi10_Community
https://t.me/Redmi_10ID/70398
```
# install-gsi
```
How to Install GSI on Redmi 10 Selene via Fastbootd

Requirements :
-> already installed adb & fastboot (platform-tools) along with the drivers on your computer
-> GSI file that has been extracted, it should be in .img format
-> UBL-enabled devices
-> Guts
-> Coffee :)

Steps:
-> Turn on Android Debug Bridge In Developer settings menu
-> Plug your cellphone into your computer
-> then on your computer open the adb directory, copy the gsi file to the adb directory and in the adb directory right click select "open cmd here"
-> then type "adb reboot fastboot" until it appears on your cellphone screen that says FASTBOOTD
-> then type again "fastboot erase userdata" and "fastboot flash system NamaGSI.img"
-> then after that you can "fastboot reboot"

NB: If the Rom(GSI) is stuck on the mi logo or bootloop, try to disable-verification & verity by "fastboot --disable-verification --disable-verity flash vbmeta vbmeta.img"
The vbmeta file is taken from the stockrom zip.

That is all and thank you
```
# kumpulan_boot.img
```
https://telegra.ph/Kumpulan-Boot-img-Selene-04-11
```
# linkgrup
```
https://www-mihub-my-id.translate.goog/2021/02/daftar-link-group-telegram-xiaomi.html?_x_tr_sl=auto&_x_tr_tl=en&_x_tr_hl=en
```
# magisk
```
only links
Latest Magisk Releases :
Stable - v24.3 (24300) : APK | Note
Beta - v25.0 (25000) : APK | Note
Canary - vcacf8736 (25001) : APK | Note
```
# mbank
```
Fix banking on a rooted cellphone

Material:
• Magisk Delta
• Riru
• Magiskhideprops
• safetynetfix

Steps:
• remove all magisk modules that require zgisk
• rename the magisk delta apk to .zip
• Go to magisk manager > modules > install modules
• select the previously renamed magisk delta apk
• Uninstall magisk manager
• rename the magisk delta apk again to .apk
• install Magisk Delta
• reboot system
• open Magisk Delta
• enter magisk settings
• disable zgisk
• install riru and safetynet fix via magisk
• reboot system
• open Magisk Delta
• enter magisk settings
• enable MagiskHide
• enter Configure MagiskHide
• tick all the apps you want to hide
• Ensure green safetynet
```
# mtk_exploit
```
file
```
# oot
```
Redmi Mediatek Series OOT Indonesia

https://t.me/RMTKG_OOT
```

# payload_dumper
```
blob:https://web.telegram.org/61136d1e-e715-4bef-844d-3b17f4327f64
How To Extract boot.img from ROM zip

- download FastbootEnhanced then extract it somewhere
-  extract payload.bin from rom zip
- watch the gif
```

# recovery
### Grab the latest twrp from that channel
```
#Twrp #Recovery #Selene #UNOFFICIAL
🆕 Twrp | UNOFFICIAL.
👤 By @yazidkucrit
📅 Release : 7/11/21

🆑 Changelog: 
• Initial build 

🐞 Bug :
• Encryption Ded
• format data
• install zip stockrom
• set brightness

👥 Credits :
 @woomymy @myusernameiswhat 

⁉️ Flash Step
• fastboot flash boot twrp.img
• fastboot disable-verity disable-verification flash vbmeta vbmeta.img
• fastboot reboot recovery
• copy stock boot.img to sdcard or internal
• install boot.img
• don't reboot
• select advanced menu
• select install curent twrp
• rebot system

📌 Join : @Redmi_10ID
📌 Follow : @R10ID_Update
```
Propably this
```
TWRP UPDATE
build : 7-3-22

🆑 Changelog: 
  Sorce update
• theme: move TW_THEME_VERSION to variables.h
• theme: clean up TW_THEME_VERSION shell command
• Partition_Property_Get: Get props from additional partitions
• twrpRepacker: avoid code duplication
• language: Update Chinese Simplified translation
• sdcard: only bind mount sdcard after successful preparation of data
• fstab: add support for metadata_encryption flag
• fstab: add quota to handled flags
• datamedia: setup datamedia with key_directory set
• twres: fix folder copy on dirty builds
• sdcard: remove mount check
• soong: create phony package to fix dirty builds (2/2)
• fscrypt_destroy_user_storage: continue when EnsurePolicy returns false 
• A11: 3.6.1 release 

  NOTES
• only for miui 12.5 android 11 and aosp custom rom a11 a12
• not work on miui 13 and don't try to flash on your device 
  
  IKI YO OLEH DI PENCET
  DONAT KOPI PAKET DATA PULSA OVO GOPAY DANA DLL
  ```
  # restore_imei
  ```
  how to restore imei via spflashtool
August 06, 2021
Tutorial restore imei via Spflashtool



1. Open your fastboot scatter rom

2. Look for the following file names: nvcfg,nvdata,nvram,persist,protect1,protect2

3. Then edit each one to

File name write nvcfg.img

Then, download it, make it true



File name write nvdata.img

Then, download it, make it true



File name write nvram.bin

Then, download it, make it true



File name write persist.img

Then, download it, make it true



File name write protect1.img

Then, download it, make it true



File name write protect2.img

Then, download it, make it true



4. After editing, save the scatter then open the spflashtool and enter the scatter

5. Next check the 6 names and then enter the backup file according to its name in spflashtool

6. Flash with Format All + download click download

7. Wait for it to finish



(NOTE; DON'T FORGET TO BYPASS AND FILTER DRIVER WITH USB LIB BEFORE FLASHING)
```
# root
```
How to Root Redmi 10
Request
- mandatory UBL #ubl
- Need a PC/Laptop
- Download Rom recovery / recovery Selene
- Download the #magisk magic app
- Download platform-tools #tools
Step :
1. Take the boot.img and Vtmeta files from the downloaded recovery Rom, then extract them in the default memory
2. Install the magisk application, then open it, select install>Select and Add file> find the boot.img file earlier
3. When you have patched the boot and copy Vtmeta to the PC, save it in the platform-tools folder
4. Open platform-tools
Type the one below

fastboot devices
fastboot flash boot boot.img
fastboot --disable-verification --disable-verity flash vbmeta vbmeta.img
```
# screenrecord
```
apk file
```
# tools
```
links to mi flash etc
https://t.me/Redmi_10ID/70983
https://t.me/Redmi_10ID/70983
https://t.me/Redmi_10ID/70983
```
# tool_unbrick_selene
```
file
```
# ubl
```
https://telegra.ph/How-to-Unlock-bootloader-11-05#Unlock%20Bootloader

Step 1

On your device, please login to your Mi account.

Step 2

Download Mi Unlock app and extract to desktop on PC.

Step 3

Put / reboot your device into bootloader mode. To do that, simply turn off your device, press the Power button and Volume down ( – ) button at the same time.

Step 4

On your computer, open MiFlash Unlock tool you’ve just installed. Click on the Agree button when asked.

Step 5

Login to MiFlash Unlock tool with the same Mi Account.

Step 6

Now connect your phone to computer using its USB cable.

Step 7

Once your phone is connected, the Unlock button will become active. Next, simply click on the Unlock button to start the process. The unlock process will take about 10 – 15 seconds to complete. That’s all. After unlocking your phone’s bootloader, you’ll be able to flash Fastboot ROM or custom ROM. Enjoy.

If stuck at 50% or could not verify your mi account please try again and again
Note - please ensure you got sms from approval permission from xiaomi
And when you got approval sms, you need to wait 5 to 7 days(until please don't try).
```
# ublinstan
```
UBL is haram
Requirements :
• pc/laptop
• windows 10/11 (8/8.1 possible but not tested)
• Internet connection

Material :
• mtkclient-gui
• drivers

Step2 :
1. Download the material above
2. Extract the driver
3. Go to the extracted driver folder
4. Right click android_winusb.inf and select install, then restart your pc
5. After restarting extract mtclient-gui
6. Go to the extracted folder mtkclient-gui
7. Double click on start.bat
8. turn off the cellphone
9. back to the laptop, select Unlock bootloader
10. Type y, then enter
11. press and hold vol up then connect to pc (still hold vol up button)
12. release if the cellphone has been detected in cmd
13. wait for it to finish

Tested devices:
• Redmi Note 9 (myst33d)

Thanks to :
• chaosmaster and All MTK-bypass Team
• Bjoern Kerler
• myst33d
```
# unbrick
```
https://forum.xda-developers.com/t/guide-how-to-bypass-authentication-and-flash-in-edl-with-no-auth-for-free.4229679/#post-84509085

https://youtu.be/yh3lzKRhok0

file spflash tool

https://t.me/redmi_9indonesia/496428
```
# vbmeta
```
file
Flash via fastboot
fastboot --disable-verity --disable-verification flash vbmeta vbmeta.img
```

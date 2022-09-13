# redmi10-liberated
My journey to install a custom rom on redmi 10: https://www.gsmchoice.com/en/catalogue/redmi/10/
## Use on your own risk, I don't take any responsibility for your actions.
Also, your device may have other IC inside, so everything may not work, additional steps could be needed. **Look into `notes-telegram` for a more detailed instructions**

### 1. Request unlocking your phone
![image](https://user-images.githubusercontent.com/53944559/189953810-12d82ab7-4748-4669-94b8-95a2b72d1804.png)

You need mobile data for this step. Some rumors on the internet say that sharing internet using bluetooth from another device that is using mobile data could also work.

### 2. Wait
The hardest step, for some reason you need to wait 7 days before you can unlock after signing up in the first step

### 3. Unlock bootloader
Download this:

https://en.miui.com/unlock/download_en.html

Fortunatelly, windows is needed. Using a VM is a bad idea for this. Enter fastboot ( Click power and volume down button. Arround 40s is needed, after some tryies it will work ). 

Install MiUsbDriver from the directory where mi flash unlock tool is. After it run it and unlock the device.

### 4. Install TWRP
There are no official versions sadly. The mediatek cpu makes it harder. Good that friends from indonesia figured this out. They figured everything out, here is the link:

https://t.me/R10ID_Update

There can you find the latest twrp for this device. In `files` folder is the image that worked for me. Flash it:
```
 fastboot flash boot TWRP_3.6.2_a11-selene.img
```
now:
```
fastboot reboot recovery
```
I hope it worked ;p

Now backup everything. Twice. A USB-C pendrive can do the job. Don't forget that FAT32 filesystem has a limit of 4Gb per file.

Try to reboot. If it doesn't worked ( It shouldn't ). Enter TWRP once more. In `notes-telegram` Its noted that flashing stock boot is needed for unkown reason. I flashed a whole stock rom, from this link:

https://miuirom.org/phones/redmi-10#EEA

Install is just `Install` in TWRP

Also very important, to avoid bricking:

https://www.xda-developers.com/xiaomi-anti-rollback-protection-brick-phone/

#### After every install, wipe etc. in TWRP use the "flash current TWRP" in advanced settings. Its needed

Now, you should have a bare miui system with TWRP

### 5. Custom ROMs

I personally installed Nusantara rom, which works good:

https://nusantararom.org

as for 13.09.2022 those are "serious" ( Official for those roms, there are also unnoficiall ports for others ) ROMs that im aware about for redmi 10:
- https://cherishos.com
- GSI roms, as pixel experience was reported too work too

Instalation is as with MIUI ROM, simply install with TWRP.

### 6. Root
It was reported that magisk doesn't work. For me it works. 

Install the newest magisk app from github, then make another backup of boot partition, provide it to magisk and this:
```
fastboot flash boot magisk_patched-25200_FNiG8.img
fastboot --disable-verification --disable-verity flash vbmeta Vbmeta.img
```

Thats it

Additional notes:
- Idk about stock, but `scrcpy` works only with those arguments: `scrcpy --encoder 'c2.android.avc.encoder' --bit-rate 5M --max-size 800 -S`
- Mobile data works better on custom rom because it isin't locked to LTE, 3G and 2G+ as on MIUI.
- Low level tools to unbrick are available, so it should be save.

### Feel free to share ( On xda for example. For some reason, even a forum isin't created for this device ), improve by creating a github issue, share your experience with this device too

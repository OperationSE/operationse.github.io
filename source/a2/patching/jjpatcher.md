# JJPatcher

JJPatcher is Java-based patcher that leverages an exploit to patch the phone at runtime. It is a bit tedious to set up but works great once installed.
It is also the only way to patch devices that have a CID greater than 53

## Prerequisites
First and foremost, you need **bpatch**, you can find the Git repo for it here: [farid1991/bpatch](https://github.com/farid1991/bpatch), either clone the repository or download it as a ZIP directly from GitHub.

You'll also need FAR Manager with SEFP2.

Finally, you'll need to take one of these `Patcher.jar` that matches your phone's firmware, if it doesn't, flash the corresponding firmware.
- [J10_R7CA061](/_static/jjpatcher_jar/J10_R7CA061/Patcher.jar)
- [J10_R7CA065](/_static/jjpatcher_jar/J10_R7CA065/Patcher.jar)
- [J20_R7CA064](/_static/jjpatcher_jar/J20_R7CA064/Patcher.jar)
- [J108_R7EA011](/_static/jjpatcher_jar/J108_R7EA011/Patcher.jar)
- [U10_R7AA071](/_static/jjpatcher_jar/U10_R7AA071/Patcher.jar)
- [U10_R7BA084](/_static/jjpatcher_jar/U10_R7BA084/Patcher.jar)
- [U100_R7AA076](/_static/jjpatcher_jar/U100_R7AA076/Patcher.jar)
- [W705_R1GA031](/_static/jjpatcher_jar/W705_R1GA031/Patcher.jar)
- [W20_R7DA062](/_static/jjpatcher_jar/W20_R7DA062/Patcher.jar)
- [W995_R1HA035](/_static/jjpatcher_jar/W995_R1HA035/Patcher.jar)

## Installation
1. Copy the corresponding `Patcher.jar` file on your device and install it as an application.
2. Once done, go to your Applications menu and copy it to internal storage. It won't work otherwise.
3. Now, remove your battery and prepare SEFP2 on your computer (Open FAR, press F11, select SEFP2 and press "Continue").
4. Put your battery back in and connect your phone to the computer while holding **C**.
5. Copy `script/customize_upgrade.xml` from the bpatch folder to `/tpa/preset/custom` on your phone.
6. Disconnect from SEFP2, remove your battery, plug it back in and start the phone.
7. Once done, go to the File Manager and you should see a file called `jab3b4ded00cb34b3cc77a6699f87ac10753fa701.b` in the **Others** folder, copy it to your memory card to get it out from the phone to bpatch's folder
8. Once out, run `python bpatch.py jab3b4ded00cb34b3cc77a6699f87ac10753fa701.b` to patch the bytecode.
9. Shut down your phone again, start SEFP2 and plug your phone back while holding **C**
10. Copy the patched `jab3b4ded00cb34b3cc77a6699f87ac10753fa701.b` file to `/tpa/preset/system/ams`
11. Unplug the phone, remove the battery, put it back in and start the phone. JJPatcher should work just fine and will patch your system with any `.vkp` patch that's in `/card/others/patches` (`card` is your memory card) on startup. Otherwise, if you've added more patches while the phone is still on, you can re-run JJPatcher from the Applications folder
# Tools
To flash and break your device, you'll need some tools.

## Driver
To begin, you need to install the USB drivers.

[Gordon's Gate Flasher](files/tools/ggsetup-3.0.0.7.exe)

## XS++
This tool lets you flash your A1-based Sony Ericsson phone.

[XS++ v3.1](files/tools/XS++.exe)

## A2Uploader
A2Uploader is a tool that fills the same purpose as XS++ but it's meant for A2-based phones.

[A2Uploader](files/tools/a2uploader.exe)

## FAR Manager
This is a modular file manager made by [Eugene Roshal](https://fr.wikipedia.org/wiki/Eugene_Roshal). It is quite modular and this specific one comes with plugins to break A1 phones and navigate through the phone's internal filesystem that's otherwise inaccessible. For A2 phones, different tools are included to patch their firmware.

Here are the links for it:
- [Far Manager A1](files/tools/FARManager.7z)
- [Far Manager A2](files/tools/FARManager_A2.7z)

## qamaker
This command line tool is used to create a "quick access" patch for your phone's firmware that has to be flashed while breaking the phone. This patch lets you then access the "break" mode quicker to flash patches.
To use this, simply drag and drop your firmware's main (`.mbn`) file on the executable and it should output a patch (with the `.vkp` format)

[qamaker](files/tools/qamaker.exe)

## SimLockPatchGen
Working in the same manner as qamaker, SimLockPatchGen generates a `.vkp` patch to remove the carrier lock. 

[SimLockPatchGen](files/tools/SIMLockPatchGen.exe)
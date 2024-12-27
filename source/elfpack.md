# Elfpacks

## Introduction
Elfpacks are a way to run custom executables natively (meaning that it's not in a virtual machine like Java applets). This means in this particular instance that they run as the same level of privilege as the kernel, and it also means that performance is magnitudes higher than Java applets.

## Installation
⚠️ **YOU SHOULD BE ABLE TO FLASH PATCHES ON YOUR PHONE BEFOREHAND, REFER TO THE FLASHING AND PATCHING DOCUMENTATION FOR YOUR MODELS**.

Here are the files you need to flash ElfPacks:
- a main ElfPack patch, as a `.vkp` file
- a "Library" ElfPack patch, that contains offsets for all function addresses, as a `.lib.vkp` file
- a binary called `DYN_CONST.bin`

### 1. Flash the patches
You have to flash the main patch and then the library patch.

### 2. Setup the file tree
Now that the patches are flashed, follow this procedure : 
- Create a **"ZBin"** folder in the **"Others"** folder of your phone
- In this **"ZBin"** folder, create **"Config"** and **"DLL"** folders.
- In the **"Config"** folder, copy the `DYN_CONST.bin` file.
- If you have any dynamic library, copy it in the **"DLL"** folder.

Daemons are ELF executables that launch at startup.
Depending on whether your phone has external storage or not *(e.g. W980)*, a **"Daemons"** folder should be created alongside the  **"Config"** and **"DLL"** folders, otherwise, this folder must be on the external storage (with this path `PHONE CARD/Other/ZBin/Daemons`)
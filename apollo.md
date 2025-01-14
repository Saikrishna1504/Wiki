![Installation Guide For Project Elixir](https://i.imgur.com/42LxtAl.png)

### Installation Guide For Project Elixir on Xiaomi Mi 10T (Pro) (apollo/apollopro/apollon)

###  **Note:** 
- The device must have an unlocked bootloader. If you are moving from Android 11/12/13 to Android 14, it is necessary CLEAN FLASH (Format Data).

### Step 1: Download Required Files
1. Download the latest Android platform tools for Windows from the link below:
   - **Platform Tools Link (Windows)**: [platform-tools-latest-windows.zip](https://dl.google.com/android/repository/platform-tools-latest-windows.zip)

2. Download the Recovery from the link below:
   - **Recovery Link [ For Android 14 ]:** [LOS Recovery](https://download.lineageos.org/devices/apollon/builds)
     - Download the latest recovery.img

3. Download the Project Elixir ROM for Mi 10T aka Apollo from a reliable source.
   - **Project Elixir ROM Link**: [DOWNLOAD](https://projectelixiros.com/device/apollo)
   

### Step 2: Install ADB and Boot into Fastboot Mode
1. Make sure you have ADB (Android Debug Bridge) installed on your computer. 
2. Extract the downloaded platform-tools zip file on your computer.
3. Connect your device to your computer using a USB cable.
4. Open a command prompt (Windows) or terminal (macOS and Linux) on your computer.
5. Navigate to the location where you extracted the platform-tools.
6. Enter the following command to check if your device is connected and detected by ADB:
```
adb devices
```
If your device is listed, proceed to the next step. If not, make sure your device is connected properly and that USB debugging is enabled in the developer options.
7. Now, reboot your device into Fastboot Mode using the following command:
```
adb reboot bootloader
```

### Step 3: Flash LOS Recovery using Fastboot
1. Once your device is in Fastboot Mode, use the following command to check if Fastboot still detects your device:
```
fastboot devices
```
If your device is listed, you are ready to flash the LOS Recovery.
2. Download the LOS Recovery ZIP (`.img` file will be in zip) from the link provided in Step 1.
3. Place the downloaded LOS Recovery image (`.img` file) in the same location as the platform-tools folder on your computer.
4. Now, flash the LOS Recovery using the following command:
```
fastboot flash recovery recovery_file_name.img
```
**Replace `recovery_file_name.img` with the actual name of the Recovery image you downloaded if needed.**
5. After flashing the recovery, use the following command to reboot your Recovery:
```
fastboot reboot recovery
```
Your device will reboot with LOS Recovery installed.

### Step 4: Wipe Data
1. In LOS Recovery, use the touch screen or physical buttons to navigate.
2. Select "Factory reset" from the main menu.
3. Tap "Format data/factory reset" and proceed to wipe data.

### Step 5: Flash Project Elixir ROM
1. Reboot to recovery.
2. In the main menu in recovery.
3. Select "Apply update".
4. Select "Apply from ADB".
5. Place the Elixir ROM file (.zip file) in the same location as the platform-tools folder on your computer.
6. Connect your phone to your PC.
7. Now, flash Project Elixir ROM using the following command
```
adb sideload ROM_file_name.zip
```
8. A warning will come up, but tap Yes and ignore.
9. Reboot & Enjoy

### Note:
- If you are coming from A12/A13 to A14 then clean flash is compulsory and format data.
- If you are encrypted do format Data before flashing build to avoid bugs.


 ## How to remove hwid and shadow bans 
 
 
❗ Note that this process will change your hardware id permanently!

***


# Let's start


### Firstly, you have to check your current hwid to compare it with the new ones:

1 - Open HWID Checker.bat

2 - Copy and paste results into notepad and save the file


### Then clean trace files

1 - Run "mw cleaner.bat"


### Change your Disks IDs:

1 - Start "HardDisk_VolumeID_Changer.exe"

2 - Wait for it to be finished

3 - Restart your pc


### Now you have to change your mac addresses:

1 - Start "MAC_Address_Changer.exe"

2 - Select the adapter you use

3 - Click on generate a random mac

4 - Click on update mac address

### And now you have to change hardware ids:

1 - Open the link to Command Prompt and type this command:

Code:
```
cd [path to "HWID spoof" folder]
```

2 - Then type to change UUID (replace X with a random character uppercase or lowercase or with a number)

```
Code:
1.AMIDEWINx64.EXE /SU AUTO 
2.AMIDEWINx64.EXE /BS XXXXXXXX
3.AMIDEWINx64.EXE /CS XXXXXX
4.AMIDEWINx64.EXE /SS XXXXXXXX
```

3 - Type following commands to save your changes

```
Code:
1.net stop winmgmt /y
2.net start winmgmt /y
3.sc stop winmgmt
4.sc start winmgmt
```

### Then modify some registers:

1 - Press win + r and type in "regedit" and press enter

2 - Follow the path: "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Cryptography"

3 - Open this website

4 - Generate a new GUID

5 - Copy and paste the new GUID into the "MachineGuid" key.

6 - Do the same thing with this path: "Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\IDConfigDB\Hardware Profiles\0001"


### And create a new Windows user, give him administrator rights and change pc name (note that if you reinstalled windows you don't need to do this):

1 - Open CMD as administrator and type

```
Code:
1.Net user [username] [password] /add
2.net localgroup administrators [username] /add
```
3 - Open pc settings

2 - Click on system

3 - Click on info

4 - Change pc name

5 - Reboot your pc

### Only if your UUID and/or Baseboard Serial number don't stick after reboot (usually with ASUS mobos):

1 - Format a USB device in FAT32

2 - Put everything inside the "Efi shell" folder inside the USB device

3 - Open id.nsh with notepad and modify what needed

4 - Turn off you pc and open the BIOS (usually with F2 or end at the starting of the pc)

5 - Put the USB device as first to run and your drive where Windows is installed as second

6 - You have to leave plugged in the USB device every time you start the pc




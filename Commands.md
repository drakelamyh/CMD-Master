# COmmand Prompt #

## General navigation ##

To see what files you have at current directory

`dir`

To see which directory you are in

`cd`

To change directory into next level of folder e.g. Desktop

`cd Desktop`

To go up one layer

`cd ..`

To go up two layers

`cd ..\..`

To change directory to specified folder location (regardless of current location)

`cd "C:\Users\XXX\Dropbox\MOOC Elearning\Coursera - Python\Course 1"`

Open File Explorer at current directory

`start .`

To open name of file (need double inverted commas if file name has spaces in it)

`filename.txt`

`"file name.txt"`

To clear command prompt screen

`cls`

To exit from Command Prompt

`exit`







## Wi-Fi ##

Shows all Wi-Fi profiles saved

`netsh wlan show profile`

Show Wi-Fi password of a particular Wi-Fi profile (replace WiFiName with name of Wi-Fi)

`netsh wlan show profile WiFiName key=clear`


## Checksum ##

To check if two files are the same, or if the file matches what is being downloaded, compare the file checksum.

`certUtil -hashfile "C:\Users\Username\Desktop\Example.txt" SHA256`









## Computer Specs ##

List Hard Disks with Device ID, Volume Name and Description

`wmic logicaldisk get deviceid, volumename, description`

Check full specs of RAM

`wmic memorychip list full`


## Repairs ##

Run Check Disk and fix errors (Requires Admin)

`chkdsk c: /f`

Run System File Checker to fix corrupted files (Requires Admin)

`sfc /scannow`





## DISM (Deployment Image Servicing and Management) to repair Window images (Requires Admin) ##

To check whether there is any corruption:

`DISM /Online /Cleanup-Image /CheckHealth`

To scan the Windows image for any corruption:

`DISM /Online /Cleanup-Image /ScanHealth`

To fix Windows image:

`DISM /Online /Cleanup-Image /RestoreHealth /Source:repairSource\install.wim`



# Command Prompt #

## General navigation ##

To see what files you have at current directory

`dir`

To see which directory you are in

`cd`

`chdir`

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

Run the Command Prompt as an Administrator

`powershell start cmd -v runAs`

Creates a Folder

`mkdir "folder name"`

Deletes a Folder

`rmdir`

Delete file

`del "file name.txt"`

Moves a File or Folder to a Specified Folder

`move hello.txt folder_name`

Renames a File with the Syntax

`ren filename.extension new-name.extension`

Shows the Tree of the Current Directory or Specified Drive

`tree`

Provides a Guide to other Commands

`-help`

Stops the Execution of a Command

`CTRL + C`

Command Prompt

`control`





## Wi-Fi ##

Shows all Wi-Fi profiles saved

`netsh wlan show profile`

Show Wi-Fi password of a particular Wi-Fi profile (replace WiFiName with name of Wi-Fi)

`netsh wlan show profile WiFiName key=clear`

Shows All Wi-Fi Passwords

`for /f "skip=9 tokens=1,2 delims=:" %i in ('netsh wlan show profiles') do @echo %j | findstr -i -v echo | netsh wlan show profiles %j key=clear`

Shows Information about PC IP Addresses and Connections

`ipconfig`

Release current IP address

`ipconfig /release`

Get new IP address (after releasing current IP address)

`ipconfig /renew`

Refresh DNS cache

`ipconfig /flushdns`

Logs on to a Website from the Command Line

`start www.google.com`

List of currently open ports and related IP addresses, what state the port is in; listening, established, or closed.
`netstat -an`

Test connectivity whether packets are making it to a specific networked device

`ping www.google.com`









## Comparisons ##

To check if two files are the same, or if the file matches what is being downloaded, compare the file checksum.

`certUtil -hashfile "C:\Users\Username\Desktop\Example.txt" SHA256`

File Compare to to identify differences in text between two files

Typing `/b` compares only binary output, `/c` disregards the case of text in the comparison, and `/l` only compares ASCII text.

`fc "C:\Program Files (x86)\example1.doc" "C:\Program Files (x86)\example2.doc"`








## Cipher ##

Checks encryption state of current directory and files it contains

`cipher`

wipe free space on the drive (does not overwrite undeleted data)

`cipher /w:d`

Encrypt a file

`cipher /e:<filename>`

Decrypt selected file

`cipher /d:<filename>`








## Computer Specs ##

Shows Your PC's details

`systeminfo`

Show other PC's details on local network

`systeminfo /s [host_name] /u [domain]\[user_name] /p [user_password]`

List Hard Disks with Device ID, Volume Name and Description

`wmic logicaldisk get deviceid, volumename, description`

Check full specs of RAM

`wmic memorychip list full`

Lists All Installed Drivers

`driverquery`

Lists Programs and the Extensions They are Associated With

`assoc`

Shows the Version of the OS

`ver`

Shows Open Programs (including hidden tasks on Task Manager)

`tasklist`

Terminates a Running Task

`taskkill /IM "task.exe" /F`

Shows the Serial Number and Label Info of the Current Drive

`vol`

Shuts down, Restarts, Hibernates, Sleeps the Computer

`shutdown`

Shutdown computer

`shutdown /s`

Restart computer

`shutdown /r`

Restart computer and launches the Advanced Start Options menu (where you can access Safe Mode and Windows recovery utilities)

`shutdown /r /o`











## Repairs ##

Run Check Disk and fix errors (Requires Admin)

`chkdsk c: /f`

Run System File Checker to fix corrupted files (Requires Admin)

`sfc /scannow`

Controls Configurable Power Settings

For example, you can use `powercfg /energy` to generate a battery health report. Can find the HTML report in `C:\Windows\system32\energy-report.html`

`powercfg`








## DISM (Deployment Image Servicing and Management) to repair Window images (Requires Admin) ##

To check whether there is any corruption:

`DISM /Online /Cleanup-Image /CheckHealth`

To scan the Windows image for any corruption:

`DISM /Online /Cleanup-Image /ScanHealth`

To fix Windows image:

`DISM /Online /Cleanup-Image /RestoreHealth /Source:repairSource\install.wim`





## Format (requires Admin) ##

Quick-format the D drive with the exFAT file system, with an allocation unit size of 2048 bytes, and rename the volume to "label" (without the quotes).

`format D: /Q /FS:exFAT /A:2048 /V:label`





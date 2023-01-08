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







## Wi-Fi ##

Shows all Wi-Fi profiles saved

`netsh wlan show profile`

Show Wi-Fi password of a particular Wi-Fi profile (replace WiFiName with name of Wi-Fi)

`netsh wlan show profile WiFiName key=clear`

Shows All Wi-Fi Passwords

`for /f "skip=9 tokens=1,2 delims=:" %i in ('netsh wlan show profiles') do @echo %j | findstr -i -v echo | netsh wlan show profiles %j key=clear`

Shows Information about PC IP Addresses and Connections
This command also has extensions such as `ipconfig /release`, `ipconfig /renew`, and `ipconfig /flushdns` which you can use to troubleshoot issues with internet connections.

`ipconfig`

Logs on to a Website from the Command Line

`start www.google.com`







## Checksum ##

To check if two files are the same, or if the file matches what is being downloaded, compare the file checksum.

`certUtil -hashfile "C:\Users\Username\Desktop\Example.txt" SHA256`









## Computer Specs ##

Shows Your PC's Details

`systeminfo`

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

Shows Open Programs

`tasklist`

Terminates a Running Task

`taskkill /IM "task.exe" /F`

Shows the Serial Number and Label Info of the Current Drive

`vol`

Shuts down, Restarts, Hibernates, Sleeps the Computer

`shutdown`

Restart computer

`shutdown /r`









## Repairs ##

Run Check Disk and fix errors (Requires Admin)

`chkdsk c: /f`

Run System File Checker to fix corrupted files (Requires Admin)

`sfc /scannow`

Controls Configurable Power Settings

`powercfg`

For example, you can use `powercfg /energy` to generate a battery health report. Can find the HTML report in `C:\Windows\system32\energy-report.html`



## DISM (Deployment Image Servicing and Management) to repair Window images (Requires Admin) ##

To check whether there is any corruption:

`DISM /Online /Cleanup-Image /CheckHealth`

To scan the Windows image for any corruption:

`DISM /Online /Cleanup-Image /ScanHealth`

To fix Windows image:

`DISM /Online /Cleanup-Image /RestoreHealth /Source:repairSource\install.wim`



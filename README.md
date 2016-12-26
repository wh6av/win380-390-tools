MD380Tools Version
How to update firmware and upload contacts.csv on Windows PC Machine
Performed by Yoram Rotbach 4Z5YR, documented by Zvika Segal 4Z1ZV
Foreword
MD380 Tools is a firmware version for TYT MD380/390 radios that enable several new features.
Key features are ability to monitor any traffic on a time slot, get on the fly contact information and some other nice to have features.
This challenging project is being performed by Travis Goodspeed KK4VCZ and can be found on his web site: https://github.com/travisgoodspeed/md380tools
The most updated firmware can be found here at the bottom of the page: https://github.com/roelandjansen/md380tools/releases and can be uploaded to the radio using the Windows Firmware Loader of TYT for MD380/390. The contact.csv can be loaded only by UNIX and “UNIX like” operating system.
Many thanks to Yoram Rotbach 4Z5YR who prepared a package of Debian Linux Virtual Machine that can run on a normal PC with Windows OS. The virtual player software is copyright of VMware http://www.vmware.com/products/player/playerpro-evaluation.html
The menu system has been created and copyright by Gescio Oteco Alpuro WH6AV. This can be downloaded directly from https://github.com/wh6av/md380-radio (Remark: For the purpose of this compilation, some unnecessary menu items have been removed)
This platform enables flashing the latest firmware as well as loading and updating the contacts.csv file on the radio.
WARNING – CONTINUE AT YOUR OWN RISK!!
Firmware update, either official or unofficial such as MD380Tools requires knowledge which is somewhat beyond basic skills. The virtual machine may not run on platforms where the CPU and/or BIOS are not capable of supporting virtualization (also known as VT-x) and may even cause the PC to hang up.
In addition, loading the wrong firmware version to the radio (Old/New Vocoders, MD380/390 with or without GPS may cause weird behavior of the radio or even potentially brick it beyond repair.
The creators of the solution and/or this document accept no liability to any such damage
Step by step instruction how to run the Virtual Debian Linux machine:
 Download and install VMware player from here: https://www.dropbox.com/s/6v47gh188apbax1/VMware-player-12.5.2-4638234.exe?dl=0
 Download the MD380tools.zip from here: https://www.dropbox.com/s/agve8z306c7kabq/md380tools.zip?dl=0
 Unzip and copy the whole directory MD380tools
folder to your hard drive or on a flash drive.
 Launch VMware Player
 First time chose – “Open a virtual machine”
 Navigate to MD380tools folder and chose file
md380tools.vmx
 Press the play button or double click md380tools
 DOS like window will pop up. Ignore all messages
and let the virtual machine run until you get the log
in screen
18-December-2016
 Point the mouse to the DOS like window and click the left button to get it into focus
You will get a debian login: message  enter: root
Password  enter: md380tools
First time operation you will be required to enter your name and call sign.
Then you will get the following menu:
For first time activation and to make sure the software is up to date, do the following:
1. Press 1 to update source files
2. Press 2 to update applications
3. Press 3 to install prerequisite MD380TOOLS programs
4. And finally press 4 to install the MD380TOOLS
Now you are ready to start flashing the radio
To install or update MD380Tools Firmware:
 Connect the radio to a USB port on the PC. Turn on the radio (volume knob) while pressing both PTT and upper button. Red/Green LED will start flashing.
 Choose menu 5 for MD-380/390 non GPS module
 Choose menu 6 for MD-380/390 GPS modules
The program will automatically download the latest firmware version from network and will perform the installation/update to the radio. Note: On the top right side of the screen there are device icons (if not shown press “<<” to open. At list one USB icon should be displayed (the radio USB). If it is grayed out, double click it with right mouse and choose “connect (disconnect from host)”.
18-December-2016
DO NOT TOUCH THE RADIO UNTIL YOU GET THE MASSAGE that the process is completed and it is safe to disconnect and re-boot the radio.
To shut down the Linux player system cleanly enter the following:
 Choose menu – 99
 Enter into the command line: shutdown –h now
 Close window and choose power down
To install or update contacts.csv
 Follow above process until you get the menu screen.
 Choose menu “7”.
The program will download the contacts.csv list from network, erase the current contacts DB from the radio and will upload the new file.
The radio screen will show: PC Program, USB mode. This may take few minutes until completed.
The radio will re-start and you are done.
How to enable some of the new features
 Enable Contact CSV mode: MenuUtilitiesMD380ToolsUserCSVEnable
 Enable last heard message instead of date: MenuUtilitiesMD380ToolsDate FormatAlt. Status
 Enable monitoring all time slot traffic: MenuUtilitiesMD380ToolsPromiscuousenable
 Enable Developer screens: MenuUtilitiesMD380ToolsDevOnly!!  enable
o Use “8”,”9”,”#” as hot keys, “7” – Normal screen
 Microphone bar graph: MenuUtilitiesMD380Tools Mic bar graph
Troubleshooting
 If during first activation of the VMware software and the md380tools virtual machine you are asked if this machine has been moved or copied, choose copied
 If flashing doesn't seem to do anything, exit cleanly (menu 99, Shutdown,…) start again and choose menu items 3 and then 4. Once done try again to flash your radio or update your users file
 Always make sure your radio is in the correct state for firmware flashing or for users database update
 Always make sure that Linux is connected to the radio and not your Windows (look at the icons on the top right of the Linux window)

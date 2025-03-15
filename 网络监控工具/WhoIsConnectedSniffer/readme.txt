


WhoIsConnectedSniffer v1.30
Copyright (c) 2013 - 2025 Nir Sofer
Web site: https://www.nirsoft.net



Description
===========

WhoIsConnectedSniffer is a network discovery tool that listens to network
packets on your network adapter using a capture driver (WinpCap or MS
network monitor) and accumulates a list of computer and devices currently
connected to your network. WhoIsConnectedSniffer uses various protocols
to detect the computers connected to your network, including ARP, UDP,
DHCP, mDNS, and BROWSER.
For every detected computer or device, the following information is
displayed: (Some of the fields might be empty if the information cannot
be found inside the packets) IP Address, MAC Address, name of the
device/computer, description, Operating System, Network Adapter Company,
IPv6 Address.

After collecting the connected computers/devices information, you can
easily export the list to tab-delimited/comma-delimited/xml/html file.



WhoIsConnectedSniffer vs Other NirSoft Tools
============================================

As you may know, NirSoft already provides other tools (Wireless Network
Watcher, NetBScanner) that scan the network and show the computers that
are currently connected. As opposed to the other tools,
WhoIsConnectedSniffer doesn't perform any scanning and it doesn't send
any packet to the other computers. WhoIsConnectedSniffer only listens to
the packets sent by other computers and devices, analyzes them and then
displays the result on the main window.
WhoIsConnectedSniffer also provides some information that the other tools
cannot get, like operating system, description text of the computer, IPv6
address.



System Requirements And Limitations
===================================


* Any version of Windows, starting from Windows 2000, and up to Windows
  11. Both 32-bit and 64-bit systems are supported. When using Microsoft
  Network Monitor driver on 64-bit system, you must use the 64-bit
  version of WhoIsConnectedSniffer.
* You have to install one of the following capture drivers:
  o Npcap capture driver (based on the discontinued WinPcap library)
  o Network Monitor driver

* WhoIsConnectedSniffer cannot detect a device or computer if it
  doesn't send any packet that is received by the computer running this
  tool.
* WhoIsConnectedSniffer cannot detect computers from other subnets.



Versions History
================


* Version 1.30:
  o Updated to detect Android and Windows operating systems from DHCP
    requests.
  o Added 'Black Background' option (Under the View menu). When it's
    turned on, the main table is displayed in black background and white
    text, instead of default system colors.
  o Updated the internal MAC addresses file.

* Version 1.28:
  o Fixed bug: WhoIsConnectedSniffer displayed random external IP
    address for the router, instead of the actual IP address.

* Version 1.27:
  o Added 'Beep On New Item' option (Under the Options menu).
  o Updated the internal MAC addresses file.

* Version 1.26:
  o Updated the internal MAC addresses file.

* Version 1.25:
  o Added 'Load From Capture File' option, which allows you to load
    the list of computers and devices on your network from a capture file
    (WinPcap capture file or Microsoft Network Monitor 3.x capture file).

* Version 1.21:
  o Updated the internal MAC addresses file.

* Version 1.20:
  o You can now save the devices list detected on your network from
    command-line, without displaying any user interface.

* Version 1.15:
  o Updated the internal MAC addresses file.

* Version 1.14:
  o The information of the selected network adapter is now displayed
    in the window title.

* Version 1.13:
  o WhoIsConnectedSniffer now automatically loads the new version of
    WinPCap driver from https://nmap.org/npcap/ if it's installed on your
    system.

* Version 1.12:
  o Updated the internal MAC addresses file.

* Version 1.11
  o Added 4 columns to the adapters list in the 'Capture Options'
    window: 'Connection Name', 'MAC Address', 'Instance ID', 'Interface
    Guid'.
  o When using WinPCap driver , WhoIsConnectedSniffer now displays
    more accurate information in the adapters list of the 'Capture
    Options' window.
  o WhoIsConnectedSniffer now tries to load the dll of Network
    Monitor Driver 3.x (NmApi.dll) according to the installation path
    specified in HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Netmon3. This
    change should solve the problem with loading the Network Monitor
    Driver 3.x on some systems.

* Version 1.10:
  o Updated the internal MAC addresses file.

* Version 1.09:
  o Fixed bug: WhoIsConnectedSniffer failed to remember the last
    size/position of the main window if it was not located in the primary
    monitor.
  o Added support for detection of Windows 10.

* Version 1.08:
  o Added 'Copy MAC Address' option.

* Version 1.07:
  o Updated the internal MAC addresses file, and reduced its size
    inside the .exe file.

* Version 1.06:
  o Added 'MAC Address Format' option (XX-XX-XX-XX-XX-XX,
    XX:XX:XX:XX:XX:XX, or XXXXXXXXXXXX).

* Version 1.05:
  o Added 'Sort On Every Update' option. If it's turned on,
    WhoIsConnectedSniffer will sort the list every time that a new item
    is added or an existing item is updated.
  o Fixed the Ctrl+X accelerator key to work.
  o WhoIsConnectedSniffer now updates the items count on the bottom
    status bar when a new item is added.

* Version 1.00 - First release.



Start Using WhoIsConnectedSniffer
=================================

Except of the capture driver, WhoIsConnectedSniffer doesn't require any
installation process or additional dll files. In order to start using it,
simply run the executable file - WhoIsConnectedSniffer.exe
After running WhoIsConnectedSniffer in the first time, you should choose
the correct capture driver and the network adapter you want to use.
After you choose the desired capture driver and the network adapter,
WhoIsConnectedSniffer starts to listen the packets on your network
adapter and updates the main window when a device or computer is detected.

You have to wait from a few seconds to a few minutes until the first
computers/devices appear on the main window of WhoIsConnectedSniffer.

After collecting the connected computers/devices information, you can
easily export the list to tab-delimited/comma-delimited/xml/html file by
selecting all items (Ctrl+A), and then using the 'Save Selected Items'
option (Ctrl+S).



Protocols supported by WhoIsConnectedSniffer
============================================


* ARP: WhoIsConnectedSniffer listens to this protocol to get the IP
  address and MAC address of computers and devices.
* UDP: When a computer broadcasts a UDP packet to all other computers,
  WhoIsConnectedSniffer extracts from it the IP address and the MAC
  address.
* DHCP: When a computer connects to the network, it usually sends a
  DHCP request. WhoIsConnectedSniffer uses this request to get the host
  name and IP address of the computer.
* mDNS: This protocol is used on Linux and Mac OS systems.
  WhoIsConnectedSniffer uses it to get the host name and IP address of
  the computer, and also the operating system (on Linux)
* BROWSER: This protocol is mainly used by Windows, but some Linux
  systems supports this protocol too. WhoIsConnectedSniffer uses it to
  get the name of the computer, description text of the computer, and the
  operating system.



Command-Line Options
====================



/cfg <Filename>
Start WhoIsConnectedSniffer with the specified configuration file. For
example:
WhoIsConnectedSniffer.exe /cfg "c:\config\wcs.cfg"
WhoIsConnectedSniffer.exe /cfg "%AppData%\WhoIsConnectedSniffer.cfg"

/CaptureTime <Time In Seconds>
Specifies the number of seconds to capture the traffic, when using one of
the save command-line options (/stext, /stab, and so on...)
If you don't specify this command-line option, the default capture time
is 10 seconds. If you specify '0', the capture will continue until
running WhoIsConnectedSniffer with /StopCommandLineCapture command-line
option.

/LoadConfig <Config File>
Loads the specified configuration file.

/SaveToFileInterval <Time In Seconds>
Saves the capture result every xx seconds.

/StopCommandLineCapture
Stops a command-line capture that is currently running and saves all
captured information to a file

/stext <Filename>
Save the connected devices list into a simple text file.

/stab <Filename>
Save the connected devices list into a tab-delimited text file.

/scomma <Filename>
Save the connected devices list into a comma-delimited text file (csv).

/stabular <Filename>
Save the connected devices list into a tabular text file.

/shtml <Filename>
Save the connected devices list into HTML file (Horizontal).

/sverhtml <Filename>
Save the connected devices list into HTML file (Vertical).

/sxml <Filename>
Save the connected devices list into XML file.

/sort <column>
This command-line option can be used with other save options for sorting
by the desired column. If you don't specify this option, the list is
sorted according to the last sort that you made from the user interface.
The <column> parameter can specify the column index (0 for the first
column, 1 for the second column, and so on) or the name of the column,
like "IP Address" and "First Detected On". You can specify the '~' prefix
character (e.g: "~Last Detected On") if you want to sort in descending
order. You can put multiple /sort in the command-line if you want to sort
by multiple columns.



Command-line Examples:
WhoIsConnectedSniffer.exe /shtml c:\temp\connected-devices-list.html
/CaptureTime 120 /SaveToFileInterval 10 /Sort "Name"
WhoIsConnectedSniffer.exe /cfg c:\temp\config1.cfg /scomma
c:\temp\traffic.csv /Sort "~Last Detected On"
WhoIsConnectedSniffer.exe /shtml c:\temp\traffic.html /CaptureTime 0
/SaveToFileInterval 15



Translating WhoIsConnectedSniffer to other languages
====================================================

In order to translate WhoIsConnectedSniffer to other language, follow the
instructions below:
1. Run WhoIsConnectedSniffer with /savelangfile parameter:
   WhoIsConnectedSniffer.exe /savelangfile
   A file named WhoIsConnectedSniffer_lng.ini will be created in the
   folder of WhoIsConnectedSniffer utility.
2. Open the created language file in Notepad or in any other text
   editor.
3. Translate all string entries to the desired language. Optionally,
   you can also add your name and/or a link to your Web site.
   (TranslatorName and TranslatorURL values) If you add this information,
   it'll be used in the 'About' window.
4. After you finish the translation, Run WhoIsConnectedSniffer, and
   all translated strings will be loaded from the language file.
   If you want to run WhoIsConnectedSniffer without the translation,
   simply rename the language file, or move it to another folder.



License
=======

This utility is released as freeware. You are allowed to freely
distribute this utility via floppy disk, CD-ROM, Internet, or in any
other way, as long as you don't charge anything for this and you don't
sell it or distribute it as a part of commercial product. If you
distribute this utility, you must include all files in the distribution
package, without any modification !



Disclaimer
==========

The software is provided "AS IS" without any warranty, either expressed
or implied, including, but not limited to, the implied warranties of
merchantability and fitness for a particular purpose. The author will not
be liable for any special, incidental, consequential or indirect damages
due to loss of data or any other reason.



Feedback
========

If you have any problem, suggestion, comment, or you found a bug in my
utility, you can send a message to nirsofer@yahoo.com

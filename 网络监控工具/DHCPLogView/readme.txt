


DHCPLogView v1.00
Copyright (c) 2025 Nir Sofer
Web site: https://www.nirsoft.net/utils/dhcp_log_view.html



Description
===========

DHCPLogView is a tool for Windows that monitors the DHCP requests sent by
every device connect to your network and displays the information on the
main window.
For every device that connects your network the following information is
displayed: DHCP Request Time, MAC Address, MAC Address Company, Requested
IP Address, Host Name, Vendor Class ID, User Class, PRL Bytes (Parameter
Request List), and the operating system of the device (For common
versions of Windows and Android)



System Requirements
===================

This tool works on any version of Windows starting from Windows XP and up
to Windows 11. Both 32-bit and 64-bit systems are supported.



Start Using DHCPLogView
=======================

DHCPLogView doesn't require any installation process or additional DLL
files. In order to start using it, simply run the executable file -
DHCPLogView.exe
Be aware that when you run this tool in the first time, the firewall of
Windows operating system will display a warning and you need to allow
this tool to access your network.
In order to verify that DHCPLogView actually works, you should simply
connect one of your devices to your network. If the device is already
connected, you have to disconnect it and then connect it again. You
should immediately see a new line of the connected device in the main
window of DHCPLogView.

While DHCPLogView is running you can use the following options:
* Turn on the 'Put Icon On Tray' option, close the main window, and
  allow DHCPLogView to collect information about devices connected to
  your network.
* Turn on also the 'Notification On DHCP Request' option in order to
  get notification every time that a device is connected to your network.
* Select one or more devices, copy the devices list to the clipboard
  (Ctrl+C) and then paste them to Excel or any other application.
* Use the 'Save All Items' option (Shift+Ctrl+S) to export the
  displayed devices to csv/tab-delimited/xml/html5/JSON file. You can
  also use the 'Save Selected Items' option to export only the selected
  devices.
* Use the 'Clear All' option (Ctrl+X) to clear the devices list
  collected until now.



DHCPLogView Columns
===================


* DHCP Request Time: This column specifies when the device sent the
  DHCP request.
* MAC Address: The MAC Address of the device.
* MAC Address Company: The name of company/manufacturer of the device
  according to the MAC address.
* Requested IP: The IP address that the device requested.
* Host Name: The name of the device that sent the DHCP request.
* Vendor Class ID: This string can be used to identify the operating
  system of the device. For example: the Vendor Class ID of Microsoft
  Windows is 'MSFT 5.0'. Be aware that some devices/operating systems
  don't provide this string.
* User Class: The user class string of the device. It may contain
  additional information about the device. Only some devices provide this
  string.
* PRL: Parameter Request List in the DHCP request. This sequence of
  bytes together with the 'Vendor Class ID' string can be used to detect
  the operating system of the device. You can find a long list of PRLs
  and Vendor Class IDs in the following Web page:
  https://github.com/daviswr/dhcpd.fingerprint/blob/master/signatures.md
* Operating System: The operating system of the device that sent the
  DHCP request. DHCPLogView automatically detects common versions of
  Android and Windows. You can add support for more operating systems by
  using the dhcpos.txt file.



Detect more operating systems with dhcpos.txt
=============================================

If you want to detect more operating systems, you can create a simple
comma-delimited file named 'dhcpos.txt' and add to it the needed
information to detect the desired operating system. You have to put this
file in the same folder of DHCPLogView.exe

Here's an example for the dhcpos.txt file:

"1:f:3:6:2c:2e:2f:1f:21:2b","MSFT 5.0","Windows 2000"
"1:f:3:6:2c:2e:2f:1f:21:f9:2b","MSFT 5.0","Windows XP/2003"
"1:f:3:6:2c:2e:2f:1f:21:79:f9:2b","MSFT 5.0","Windows Vista/7/2008"
"1:f:3:6:2c:2e:2f:1f:21:79:f9:fc:2b","MSFT 5.0","Windows 8/10/2012"
"1:3:6:f:1f:21:2b:2c:2e:2f:79:f9:fc","MSFT 5.0","Windows 10/2016"
"1:3:6:f:1f:21:2b:2c:2e:2f:77:79:f9:fc","MSFT 5.0","Windows 10/11/2019"


This comma-delimited file contains 3 fields in every line:
1. The Parameter Request List (PRL). You can optionally omit this
   field by specifying empty string ("") and use only the Vendor Class ID.
2. The Vendor Class ID of the operating system. You can optionally
   omit this field by specifying empty string ("") and use only the PRL
   field.
3. The name of the operating system.

The following Web page may help you to find the PRL and the Vendor Class
ID for the desired operating system:
https://github.com/daviswr/dhcpd.fingerprint/blob/master/signatures.md



Translating DHCPLogView to other languages
==========================================

In order to translate DHCPLogView to other language, follow the
instructions below:
1. Run DHCPLogView with /savelangfile parameter:
   DHCPLogView.exe /savelangfile
   A file named DHCPLogView_lng.ini will be created in the folder of
   DHCPLogView utility.
2. Open the created language file in Notepad or in any other text
   editor.
3. Translate all string entries to the desired language. Optionally,
   you can also add your name and/or a link to your Web site.
   (TranslatorName and TranslatorURL values) If you add this information,
   it'll be used in the 'About' window.
4. After you finish the translation, Run DHCPLogView, and all
   translated strings will be loaded from the language file.
   If you want to run DHCPLogView without the translation, simply rename
   the language file, or move it to another folder.



License
=======

This utility is released as freeware. You are allowed to freely
distribute this utility via CD-ROM, DVD, Internet, or in any other way,
as long as you don't charge anything for this and you don't sell it or
distribute it as a part of commercial product. If you distribute this
utility, you must include all files in the distribution package, without
any modification !



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
utility, you can send a message to support@nirsoft.net




NetworkConnectLog v1.17
Copyright (c) 2013 - 2025 Nir Sofer
Web site: https://www.nirsoft.net



Description
===========

NetworkConnectLog is a simple utility that repeatedly scans your local
area network (Using ARP and Netbios protocols) and add a new log line
every time that a new computer or device connects to your network, and
when a computer or device disconnects from your network.
After the connect/disconnect log lines are accumulated, you can easily
export the log lines to comma-delimited/tab-delimited/html/xml file.



System Requirements
===================


* This utility works on any version of Windows, starting from Windows
  2000 and up to Windows 11. Both 32-bit and 64-bit systems are supported.



Known Issues
============


* In some circumstances, Smartphone devices don't respond to ARP
  requests, even when the device shows that it's actually connected to
  the network. In this situation, NetworkConnectLog will show that the
  device is disconnected.



Versions History
================


* Version 1.17:
  o Added 'Save All Items' option (Shift+Ctrl+S).
  o Updated the internal MAC addresses database.
  o Added 'Black Background' option (Under the View menu). When it's
    turned on, the main table is displayed in black background and white
    text, instead of default system colors.

* Version 1.16:
  o Fixed to display a check mark when the 'Put Icon On Tray' option
    is turned on.

* Version 1.15:
  o Updated to work properly in high DPI mode.
  o Updated the internal MAC addresses database.

* Version 1.13:
  o Updated the internal MAC addresses database.

* Version 1.12:
  o Updated the internal MAC addresses database.

* Version 1.11:
  o Updated the internal MAC addresses database.

* Version 1.10:
  o Added option to set the interval between scans, in milliseconds
    ('Scan Options' window).
  o Added option to automatically export the log to a file on every
    change (In 'Scan Options' window).

* Version 1.06:
  o Added option to choose another font (name and size) to display in
    the main window.

* Version 1.05:
  o Added 'Always On Top' option.

* Version 1.04:
  o Updated the internal MAC addresses database.

* Version 1.03:
  o Fixed the sorting of 'IP Address' column.

* Version 1.02:
  o Added 'MAC Address Format' option (XX-XX-XX-XX-XX-XX,
    XX:XX:XX:XX:XX:XX, or XXXXXXXXXXXX).

* Version 1.01:
  o Fixed the sorting of the 'IP Address' column.

* Version 1.00 - First release.



Start Using NetworkConnectLog
=============================

NetworkConnectLog doesn't require any installation process or additional
dll files. In order to start using it, simply run the executable file -
NetworkConnectLog.exe

After you run NetworkConnectLog.exe, it immediately starts to scan your
network. The first scan is fast, in order to detect all computers and
devices that are currently connected to your network. After the first
scan, NetworkConnectLog repeatedly scans your network in lower speeds in
order to check if computer/devices connected or disconnected to your
network. Every time that NetworkConnectLog detects that computer or
device connected or disconnected to your network, a new log line is added.
If from some reason NetworkConnectLog fails to detect your network
properly, you should go to the 'Scan Options' window (F9) and choose the
correct network adapter or IP addresses range to scan.



Translating NetworkConnectLog to other languages
================================================

In order to translate NetworkConnectLog to other language, follow the
instructions below:
1. Run NetworkConnectLog with /savelangfile parameter:
   NetworkConnectLog.exe /savelangfile
   A file named NetworkConnectLog_lng.ini will be created in the folder
   of NetworkConnectLog utility.
2. Open the created language file in Notepad or in any other text
   editor.
3. Translate all string entries to the desired language. Optionally,
   you can also add your name and/or a link to your Web site.
   (TranslatorName and TranslatorURL values) If you add this information,
   it'll be used in the 'About' window.
4. After you finish the translation, Run NetworkConnectLog, and all
   translated strings will be loaded from the language file.
   If you want to run NetworkConnectLog without the translation, simply
   rename the language file, or move it to another folder.



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

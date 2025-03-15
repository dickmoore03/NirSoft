


ManageWirelessNetworks v1.16
Copyright (c) 2021 - 2025 Nir Sofer
Web site: https://www.nirsoft.net/utils/manage_wireless_networks.html



Description
===========

ManageWirelessNetworks is an alternative tool to the standard 'Manage
Wireless Networks' of Windows (or 'Manage Known Networks' on Windows 10).
It displays extensive information about every wireless profile on your
system, even if the network adapter is not active. For every wireless
profile, the following information is displayed: Profile Name, SSID,
Connection Type, Connection Mode, Authentication, Encryption, Key Type,
Auto Switch (Yes/No), Non Broadcast (Yes/No), Profile Position, Created
Time, Modified Time, Wireless Key, and more...

ManageWirelessNetworks also allows you to edit a single profile with the
standard editor of Windows, edit the XML of the wireless profile (For
advanced users only !), quickly switch between manual and automatic mode,
quickly switch between WPAPSK/WPA2PSK/AES/TKIP modes, rename the profile,
rename the SSID, move profile position up and down, copy multiple
wireless profiles to another wireless card on your system, and more...



System Requirements
===================


* This tool works on any version of Windows, starting from Windows
  Vista and up to Windows 11. Both 32-bit and 64-bit systems are
  supported.
* This tool is just a small standalone .exe file that you can run on
  any system without installing anything.



Version History
===============


* Version 1.16:
  o Added 'Save All Items' option.

* Version 1.15:
  o Added 'Black Background' option (Under the View menu). When it's
    turned on, the main table is displayed in black background and white
    text, instead of default system colors.

* Version 1.14:
  o Added 'Set Connection Mode' toolbar dropdown.

* Version 1.13:
  o Fixed issue: When copying data to the clipboard or exporting to
    tab-delimited file, every line contained an empty field in the end of
    the line.

* Version 1.12:
  o Added 'Sort By' toolbar button.

* Version 1.11:
  o Added 'Copy QR Code' option (Under the Edit menu), which allows
    you to copy the QR Code image to the clipboard.

* Version 1.10:
  o Added 'Connect Selected Profile' option, which allows you to
    instantly connect the wireless network of the selected profile.

* Version 1.08:
  o Added 'Always On Top' option.
  o Fixed the default columns size in high DPI mode.

* Version 1.07:
  o Added 'Add Header Line To CSV/Tab-Delimited File' option (Turned
    on by default).

* Version 1.06:
  o Added /Columns command-line option, which allows you to set the
    columns to display or the columns to export from command-line, for
    example:
    ManageWirelessNetworks.exe /Columns "Profile
    Name,SSID,Authentication,Encryption,Key Type,Interface Name"

* Version 1.05:
  o Added 'Double-Click Action' option, which allows you to choose
    what to do when you double-click a wirless network item with the
    mouse: None, Open Properties Window, Edit Wireless Profile, Edit
    Profile XML, Rename SSID, Rename Profile.
  o Added 'Enter Action' option, which allows you to choose what to
    do when you press the Enter key: None, Open Properties Window, Edit
    Wireless Profile, Edit Profile XML, Rename SSID, Rename Profile.

* Version 1.02:
  o Added 'Copy Clicked Cell' option to the right-click context menu,
    which copies to the clipboard the text of cell that you right-clicked
    with the mouse.

* Version 1.01:
  o Added option to choose another font (name and size) to display in
    the main window.

* Version 1.00 - First release.



Start Using ManageWirelessNetworks
==================================

ManageWirelessNetworks doesn't require any installation process or
additional DLL files. In order to start using it, simply run the
executable file - ManageWirelessNetworks.exe
After you run the ManageWirelessNetworks tool, the main window displays
the details of all wireless profiles on your system. You can select one
or more profiles from the list and then choose the desired action from
the top menu or from the right-click context menu.

Be aware: ManageWirelessNetworks displays all wireless profiles on your
system, even if the wireless adapter is not active. However, most actions
(like edit profile, rename SSID, and so on...) only works for wireless
profiles with active network adapter. If you want to view only the
wireless profiles that their wireless adapter is active, simply turn on
the 'Load Only Active Network Interfaces' option.
Wireless profiles of active network adapters are displayed with green
icon, while Wireless profiles of inactive network adapters are displayed
with gray icon.



Export wireless profiles list
=============================

In order to export the wireless profiles list into a file, simply select
one or more files in the main window (or press Ctrl+A to select all
items), press Ctrl+S (Save Selected Items) and then in the save
dialog-box choose the type of file to export (Text File, Tab Delimited
Text File, JSON File, HTML File - Horizontal, HTML File - Vertical, XML
File, or Comma Delimited Text File), type the filename to save, and then
click the Save button.

Optionally, you can also press Ctrl+C (Copy Selected Items) to copy the
wireless profiles list as tab-delimited format, and then paste the
profiles list into Excel or other spreadsheet application.



Copy wireless profiles to another wireless network adapter
==========================================================

If you have a new wireless network adapter and you want to connect the
same wireless networks that you used with another network adapter, simply
select the profiles you want to use with the new adapter, choose the
'Copy Profiles To Another Network Interface' option from the File menu,
select your new wireless adapter, and ManageWirelessNetworks tool will
copy all previous profiles to the new adapter. This feature works even if
the previous network adapter is not active.



Rename SSID
===========

If you changed the name of your wireless network (SSID), you can easily
update the new SSID by using the 'Rename SSID' option. Only the SSID of
your profile will be updated. All other settings, like the network key,
will remain the same as before. Optionally, you can also update the
profile name by using the 'Rename Profile' option.



Edit Wireless Profile
=====================

The 'Edit Wireless Profile' option allows you the change the settings of
existing wireless profile, using the standard wireless profile editor of
Windows operating system. Be aware that this option works only for
wireless profiles of active network adapter (Active Interface = Yes).



Delete wireless profiles
========================

ManageWirelessNetworks allows you to delete one or more wireless profiles
on your system, by using the 'Delete Selected Profiles' option
(Ctrl+Delete). If you want to delete wireless profiles of inactive
wireless adapter (Active Interface = No), you have to run
ManageWirelessNetworks as Administrator (Ctrl+F11).



Duplicate Profile
=================

If you want to duplicate an existing wireless profile on the same
wireless network adapter, simply select the desired profile, choose
'Duplicate Profile' from the menu, type the name of the new duplicated
profile and then ManageWirelessNetworks will create a new profile with
exactly the same settings of the original profile. After the duplicated
profile is created, you can use the 'Edit Wireless Profile' and other
options to change the settings of the duplicated profile.



Set connection mode for multiple profiles
=========================================

ManageWirelessNetworks allows you to quickly choose the wireless profiles
that Windows will try to connect automatically. Simply select the desired
wireless profiles, and then press F7 to connect the selected wireless
profiles automatically (Set Connection Mode -> Automatic), or press F8 to
stop connecting the selected wireless profiles automatically (Set
Connection Mode -> Manual).



View Wireless Keys
==================

If you want the view the wireless key of your wireless profiles, go to
the Options menu and turn on the 'Show Wireless Keys' options.
ManageWirelessNetworks displays the wireless key only for profiles of
active wireless adapter (Active Interface = Yes).
Be aware that on systems prior to Windows 10 you have to run
ManageWirelessNetworks as Administrator (Ctrl+F11) in order to view the
wireless keys.



Command-Line Options
====================



/stext <Filename>
Save the wireless profiles list to a simple text file.

/stab <Filename>
Save the wireless profiles list to a tab-delimited text file.

/scomma <Filename>
Save the wireless profiles list to a comma-delimited text file (csv).

/shtml <Filename>
Save the wireless profiles list to HTML5 file (Horizontal).

/sverhtml <Filename>
Save the wireless profiles list to HTML5 file (Vertical).

/sxml <Filename>
Save the wireless profiles list to XML file.

/sjson <Filename>
Save the wireless profiles list to JSON file.

/sort <column>
This command-line option can be used with other save options for sorting
by the desired column. The <column> parameter can specify the column
index (0 for the first column, 1 for the second column, and so on) or the
name of the column, like "SSID" and "Profile Name". You can specify the
'~' prefix character (e.g: "~Position") if you want to sort in descending
order. You can put multiple /sort in the command-line if you want to sort
by multiple columns.

/cfg <Config Filename&gt
Start ManageWirelessNetworks with the specified config file.

/Columns <Comma Delimited Columns List>
Allows you to set the columns to display or the columns to export from
command-line. You have to specify the column names, delimited by comma,
for example:
ManageWirelessNetworks.exe /scomma c:\temp\wireless-networks-list.csv
/Columns "Profile Name,SSID,Authentication,Encryption,Key Type,Interface
Name"

You can also specify the column names without space characters, for
example:
ManageWirelessNetworks.exe /Columns
"ProfileName,SSID,Authentication,Encryption,KeyType,InterfaceName"



Translating ManageWirelessNetworks to other languages
=====================================================

In order to translate ManageWirelessNetworks to other language, follow
the instructions below:
1. Run ManageWirelessNetworks with /savelangfile parameter:
   ManageWirelessNetworks.exe /savelangfile
   A file named ManageWirelessNetworks_lng.ini will be created in the
   folder of ManageWirelessNetworks utility.
2. Open the created language file in Notepad or in any other text
   editor.
3. Translate all string entries to the desired language. Optionally,
   you can also add your name and/or a link to your Web site.
   (TranslatorName and TranslatorURL values) If you add this information,
   it'll be used in the 'About' window.
4. After you finish the translation, Run ManageWirelessNetworks, and
   all translated strings will be loaded from the language file.
   If you want to run ManageWirelessNetworks without the translation,
   simply rename the language file, or move it to another folder.



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

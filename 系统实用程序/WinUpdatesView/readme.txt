


WinUpdatesView v1.18 - Windows Updates History Viewer
Copyright (c) 2019 - 2024 Nir Sofer
Web site:
https://www.nirsoft.net/utils/windows_updates_history_viewer.html



Description
===========

WinUpdatesView is a simple tool that displays the history of Windows
updates on your system. WinUpdatesView can load the Windows updates
history from your local system, using API, and it can also read and parse
the Windows updates database file (DataStore.edb) from external drive or
from remote computer on your network.
For every Windows update history record, WinUpdatesView displays the
following fields: Title, Description, Install Date, Update Operation
(Install, Uninstall, Not Started, In Progress), Operation Result
(Succeeded, Succeeded With Errors, Failed, Aborted), Category,
Information URL, Support URL, Uninstall Notes, Client Application ID,
Service ID, Update ID, Revision Number, Unmapped Result Code, Server
Selection, hResult



System Requirements
===================

This tool works on any version of Windows, starting from Windows XP, and
up to Windows 11. Both 32-bit and 64-bit systems are supported.



Versions History
================


* Version 1.18
  o Added 'Sort By' toolbar button.

* Version 1.17
  o Added 'Add Header Line To CSV/Tab-Delimited File' option (Turned
    on by default).

* Version 1.16
  o Added option to change the sorting column from the menu (View ->
    Sort By). Like the column header click sorting, if you click again
    the same sorting menu item, it'll switch between ascending and
    descending order. Also, if you hold down the shift key while choosing
    the sort menu item, you'll get a secondary sorting.

* Version 1.15
  o Fixed some display issues in high DPI mode.

* Version 1.14
  o Fixed the /cfg command-line option to load the .cfg file from the
    current directory if full path is not specified.
  o Added 'Copy Clicked Cell' option to the right-click context menu,
    which copies to the clipboard the text of cell that you right-clicked
    with the mouse.

* Version 1.13
  o Fixed the 'Hide Windows Defender Updates' option to work properly
    with the latest Windows Defender updates (The Category field is now
    'Microsoft Defender Antivirus' instead of 'Windows Defender' )
  o Added 'Save All Items' option (Shift+Ctrl+S).

* Version 1.12
  o Added /cfg command-line option to start WinUpdatesView with the
    specified config file.

* Version 1.11
  o Added 'KB Number' column.

* Version 1.10
  o Added 'Hide Windows Defender Updates' option.
  o Fixed to save the 'Case Sensitive' option of the Quick Filter in
    the .cfg file.

* Version 1.06
  o Added option to choose another font (name and size) to display in
    the main window.

* Version 1.05
  o Added 'Hide Items For API Compatibility' option. This option is
    added because when reading the Windows 10 updates database directly,
    there are more items than getting the Windows updates list using API.
    When this option is turned on, and WinUpdatesView reads the Windows
    10 updates history database directly - it automatically hides items
    that are not provided by Windows API, so you'll get the same result
    for both API method and database reading method.
  o Added 'Show Time In GMT' option.

* Version 1.00 - First release.



Start Using Windows Updates History Viewer
==========================================

WinUpdatesView doesn't require any installation process or additional DLL
files. In order to start using it, simply run the executable file -
WinUpdatesView.exe
After running WinUpdatesView, it loads the Windows updates history from
your local system, using API, and displays the information on the main
window. You can select one or more items and then export them to
csv/tab-delimited/HTML5/XML/JSON file (File -> 'Save Selected Items' or
Ctrl+S ), or you can copy them to the clipboard (Ctrl+C) and then paste
them to Excel or other application.

If you want to load the Windows updates history from another source
(remote computer or external drive), go to the 'Advanced Options' window
(F9) and choose the desired options.



Quick Filter
============

If you want to search a specific Windows update, simply press Ctrl+Q, and
in the 'Quick Filter' window, type the string you want to find, and
WinUpdatesView will instantly display the Windows updates contain the
string you typed.



Getting Windows updates history from a remote computer
======================================================

You can view the Windows updates history of a remote computer, by opening
the 'Advanced Options' window (F9), choosing 'Remote computer' in the
'Load From' combo-box and typing the remote computer name.
In order to access the Windows updates database on the remote computer,
you need a full admin access with admin share ( \\ComputerName\Admin$ ).
Also, in many systems the Windows updates database is locked for reading,
so in order to release the file, WinUpdatesView provides an option to
temporarily stop the Windows Update service. If you choose this option,
WinUpdatesView automatically stops the Windows Update service on the
remote computer if the database is locked, reads the database file, and
then starts again the Windows Update service.

Warning !! You should not use 'Temporarily stop the Windows Updates
service' option while updates are downloaded and installed, because
stopping the Windows update service will disrupt the update process.




Getting Windows updates history from external drive
===================================================

In order to load the Windows updates history from external drive, simply
go to the 'Advanced Options' window (F9), choose 'External database file'
in the 'Load From' combo-box and then type the location of the database
file. You can find the Windows updates database file in
Windows\SoftwareDistribution\DataStore\DataStore.edb



Windows version on status bar
=============================

The status bar displays the Windows version and build number taken from
hal.dll, for both local computer and remote computer. Be aware that the
displayed build number from hal.dll might be a little different from the
build you see when using ver command.



Command-Line Options
====================



/cfg <Filename>
Start WinUpdatesView with the specified configuration file. For example:
WinUpdatesView.exe /cfg "c:\config\wuv.cfg"
WinUpdatesView.exe /cfg "%AppData%\WinUpdatesView.cfg"

/stext <Filename>
Save the Windows updates history to a simple text file.

/stab <Filename>
Save the Windows updates history to a tab-delimited text file.

/scomma <Filename>
Save the Windows updates history to a comma-delimited text file (csv).

/shtml <Filename>
Save the Windows updates history to HTML5 file (Horizontal).

/sverhtml <Filename>
Save the Windows updates history to HTML5 file (Vertical).

/sxml <Filename>
Save the Windows updates history to XML file.

/sjson <Filename>
Save the Windows updates history to JSON file.

/sort <column>
This command-line option can be used with other save options for sorting
by the desired column. The <column> parameter can specify the column
index (0 for the first column, 1 for the second column, and so on) or the
name of the column, like "Install Date" and "Title". You can specify the
'~' prefix character (e.g: "~Description") if you want to sort in
descending order. You can put multiple /sort in the command-line if you
want to sort by multiple columns.

/LoadFrom <Load From>
Specifies the type of data source to load:
1 - Local computer, with API
2 - Local computer, Read database file directly.
3 - Load from external database file.
4 - Load from remote computer.

/ExternalFilename <Filename>
Specifies the external database file (for using with /LoadFrom 3 )

/ComputerName <Filename>
Specifies the computer name (for using with /LoadFrom 4 )

/StopWinUpdatesService <0 | 1>
Specifies whether to temporarily stop the Windows Update service if the
database file is locked. 0 = No, 1 = Yes.



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

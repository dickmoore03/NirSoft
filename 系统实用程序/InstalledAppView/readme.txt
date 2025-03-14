


InstalledAppView v1.09
Copyright (c) 2019 - 2024 Nir Sofer
Web site: https://www.nirsoft.net/utils/installed_app_view.html



Description
===========

InstalledAppView is a tool for Windows 10 and Windows 11 that displays
the details of Windows 11/10 apps installed on your system. For every
Windows app, the following information is displayed: App Name, App
Version, Registry Name, Registry Modified Time, Install Folder, Install
Folder Owner, Uninstall Command, and more...
InstalledAppView allows you to load the Windows 11/10 apps list from your
local system, remote computer on your network, and from external disk
plugged to your computer.
InstalledAppView also allows you to view the XML files of the Windows app
(AppxManifest.xml and AppxBlockMap.xml), uninstall apps, quietly
uninstall apps, open the install folder of the app, and more...



System Requirements
===================

This tool works on Windows 11, Windows 10, and Windows 8. Both 32-bit and
64-bit systems are supported.



Versions History
================


* Version 1.09
  o Added 'Black Background' option (Under the View menu). When it's
    turned on, the main window is displayed in black background and white
    text, instead of default system colors.

* Version 1.08
  o Fixed a bug with saving the installed apps list from command-line.

* Version 1.07
  o Fixed a few high DPI mode issues.
  o Added 'Sort By' toolbar button.

* Version 1.06
  o Updated to work properly in high DPI mode.

* Version 1.05
  o Added option to change the sorting column from the menu (View ->
    Sort By). Like the column header click sorting, if you click again
    the same sorting menu item, it'll switch between ascending and
    descending order. Also, if you hold down the shift key while choosing
    the sort menu item, you'll get a secondary sorting.

* Version 1.01
  o Fixed bug: The 'App Version' column displayed the App Name
    instead of App Version.

* Version 1.00 - First release.



Start Using InstalledAppView
============================

InstalledAppView doesn't require any installation process or additional
DLL files. In order to start using it, simply run the executable file -
InstalledAppView.exe
After you run InstalledAppView, the upper pane of the main window
displays the list of installed Windows Apps on your system. When
selecting a single Windows app on the upper pane, the lower pane displays
the XML of the app (AppxManifest.xml or AppxBlockMap.xml).
You can also select one or more apps in the upper pane and then use the
'Save Selected Items' option (CTRL+S) to export the apps list to
csv/tab-delimited/xml/html/JSON file. You can also copy the selected
items to the clipboard and them paste them into Excel or other
spreadsheet application.



View Windows 10 Apps on remote computer
=======================================

In order to load the installed Windows 10 Apps from a remote computer on
your network, simply press F9 ('Advanced Options' window), choose the
'Remote computer' or 'Remote computer - all users' option from the 'Load
From' combo-box, and then type the name of the remote computer. It's also
recommended to turn on the 'Automatically turn on the remote Registry
service' option, because the Remote Registry service is needed to read
the installed apps list from the remote computer.

Be aware that you need full admin access on the remote computer in order
to use this feature.



View Windows 10 Apps on external disk
=====================================

In order to load the installed Windows 10 Apps from external disk plugged
to your computer, simply press F9 ('Advanced Options' window), choose
'External drive' option from the 'Load From' combo-box, and then type the
right paths of the external drive.



Uninstall Windows 10 Apps
=========================

In order to uninstall Windows 10 app with InstalledAppView, simply
selected the desired app, and then choose 'Uninstall Selected App' from
the right-click context menu or from the File menu (or simply press
Ctrl+U). You can also activate a silent uninstall by using the 'Quietly
Uninstall Selected App' option.



Command-Line Options
====================



/stext <Filename>
Save the Windows 11/10 apps list to a simple text file.

/stab <Filename>
Save the Windows 11/10 apps list to a tab-delimited text file.

/scomma <Filename>
Save the Windows 11/10 apps list to a comma-delimited text file (csv).

/shtml <Filename>
Save the Windows 11/10 apps list to HTML5 file (Horizontal).

/sverhtml <Filename>
Save the Windows 11/10 apps list to HTML5 file (Vertical).

/sxml <Filename>
Save the Windows 11/10 apps list to XML file.

/sjson <Filename>
Save the Windows 11/10 apps list to JSON file.

/sort <column>
This command-line option can be used with other save options for sorting
by the desired column. The <column> parameter can specify the column
index (0 for the first column, 1 for the second column, and so on) or the
name of the column, like "App Name" and "App Version". You can specify
the '~' prefix character (e.g: "~Registry Modified Time") if you want to
sort in descending order. You can put multiple /sort in the command-line
if you want to sort by multiple columns.



Translating InstalledAppView to other languages
===============================================

In order to translate InstalledAppView to other language, follow the
instructions below:
1. Run InstalledAppView with /savelangfile parameter:
   InstalledAppView.exe /savelangfile
   A file named InstalledAppView_lng.ini will be created in the folder of
   InstalledAppView utility.
2. Open the created language file in Notepad or in any other text
   editor.
3. Translate all string entries to the desired language. Optionally,
   you can also add your name and/or a link to your Web site.
   (TranslatorName and TranslatorURL values) If you add this information,
   it'll be used in the 'About' window.
4. After you finish the translation, Run InstalledAppView, and all
   translated strings will be loaded from the language file.
   If you want to run InstalledAppView without the translation, simply
   rename the language file, or move it to another folder.



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

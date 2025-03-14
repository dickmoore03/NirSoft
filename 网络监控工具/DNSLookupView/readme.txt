


DNSLookupView v1.13
Copyright (c) 2020 - 2024 Nir Sofer
Web site: https://www.nirsoft.net/utils/dns_lookup_view.html



Description
===========

DNSLookupView is a DNS tracing tool for Windows 10 and Windows 11 that
allows you to view the details of every DNS query sent through the DNS
Client service of Windows. For every DNS query, the following information
is displayed: Host Name, Query Type (A, AAAA, and so on), Query Status
(Error or succeeded), Query Result, Query Timestamp, ID and name of the
process that requested the DNS lookup.



System Requirements
===================

This tool works only on Windows 11, Windows 10, and Windows 8.1. Both
32-bit and 64-bit systems are supported. This tool doesn't work on older
versions of Windows, because the operating system doesn't support the DNS
tracing.



How it works ?
==============

This tool uses the event tracing of Windows operating system with the
'Microsoft-Windows-DNS-Client' provider (
1C95126E-7EEA-49A9-A3FE-A378B03DDB4D ). The captured event ID is 3008,
which contains the information about every DNS query handled by the DNS
Client service of Windows.



Version History
===============


* Version 1.13:
  o Added 'Sort By' toolbar button.

* Version 1.12:
  o Added 'Black Background' option (Under the View menu). When it's
    turned on, the main table is displayed in black background and white
    text, instead of default system colors.
  o Added 'Full Screen' mode (View -> Full Screen or F11 key).
  o Added 'Automatically Start DNS Tracing' option. If you turn it
    on, DNSLookupView automatically starts the DNS tracing when you run
    the program.

* Version 1.11:
  o Added milliseconds to the 'Time' column.

* Version 1.10:
  o Added new option: Show only records of the specified domains/host
    names (In 'Advanced Options' window).
  o Added new option: Don't show records of the specified
    domains/host names (In 'Advanced Options' window).
  o Added option to add the DNS queries into a log file
    (Comma-delimited or tab-delimited file) in the 'Advanced Options'
    window.

* Version 1.06:
  o Added 'Add Header Line To CSV/Tab-Delimited File' option (Turned
    on by default).

* Version 1.05:
  o Added 'Put Icon On Tray' option.

* Version 1.01:
  o Added option to choose another font (name and size) to display in
    the main window.
  o Fixed problem with the 'Choose Columns' window in high DPI mode.

* Version 1.00 - First release.



Start Using DNSLookupView
=========================

DNSLookupView doesn't require any installation process or additional DLL
files. In order to start using it, simply run the executable file -
DNSLookupView.exe
After running DNSLookupView, the main window is displayed, and you can
press the 'Start DNS Tracing' toolbar button (or simply press the F5 key)
to start capturing the DNS queries on your system.
When you want to stop capturing the DNS queries, you can simply press the
F6 key or the 'Stop DNS Tracing' toolbar button.
You can select one or more DNS queries (or select all of them by pressing
Ctrl+A) and then export them to
comma-delimited/tab-delimited/html/xml/JSON file by using the 'Save
Selected Items' option (Ctrl+S), or you can copy the selected DNS queries
to the clipboard (Ctrl+C) and then paste them to Excel or other
spreadsheet application.



Command-Line Options
====================



/CaptureTime <Milliseconds>
Specifies the capture time in milliseconds for the save command-line
options (/stext, /stab, /scomma, and so on...)
The default is 10000 milliseconds (10 seconds).

For example, if you want to capture the DNS activity for 20 seconds and
then save the result to csv file:
DNSLookupView.exe /CaptureTime 20000 /scomma "c:\temp\dns.csv"

/stext <Filename>
Save the DNS lookup records to a simple text file.

/stab <Filename>
Save the DNS lookup records to a tab-delimited text file.

/scomma <Filename>
Save the DNS lookup records to a comma-delimited text file (csv).

/shtml <Filename>
Save the DNS lookup records to HTML5 file (Horizontal).

/sverhtml <Filename>
Save the DNS lookup records to HTML5 file (Vertical).

/sxml <Filename>
Save the DNS lookup records to XML file.

/sjson <Filename>
Save the DNS lookup records to JSON file.



Translating DNSLookupView to other languages
============================================

In order to translate DNSLookupView to other language, follow the
instructions below:
1. Run DNSLookupView with /savelangfile parameter:
   DNSLookupView.exe /savelangfile
   A file named DNSLookupView_lng.ini will be created in the folder of
   DNSLookupView utility.
2. Open the created language file in Notepad or in any other text
   editor.
3. Translate all string entries to the desired language. Optionally,
   you can also add your name and/or a link to your Web site.
   (TranslatorName and TranslatorURL values) If you add this information,
   it'll be used in the 'About' window.
4. After you finish the translation, Run DNSLookupView, and all
   translated strings will be loaded from the language file.
   If you want to run DNSLookupView without the translation, simply
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

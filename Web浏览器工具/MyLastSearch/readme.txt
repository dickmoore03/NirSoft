


MyLastSearch v1.66
Copyright (c) 2007 - 2025 Nir Sofer
Web site: http://www.nirsoft.net




Description
===========

MyLastSearch utility scans the cache and history files of your Web
browser, and locate all search queries that you made with the most
popular search engines (Google, Yahoo and MSN) and with popular social
networking sites (Twitter, Facebook, MySpace). The search queries that
you made are displayed in a table with the following columns: Search
Text, Search Engine, Search Time, Search Type (General, Video, Images),
Web Browser, and the search URL.
You can select one or more search queries and then copy them to the
clipboard or save them into text/html/xml file.



Versions History
================


* Version 1.66:
  o Updated to read the cache files of the latest Chrome version
    (Version 132).
  o Fixed a crash problem when reading the old IE11 cache file
    (WebCacheV01.dat) on Windows 11 24H2.

* Version 1.65:
  o Added support for Yandex and DuckDuckGo search engines.

* Version 1.64:
  o Fixed to work with the latest build of Windows 10 (For IE11 Web
    browser)

* Version 1.63:
  o Added support for the new cache structure of Firefox 32.

* Version 1.62:
  o Fixed issue with Chrome Web browser: MyLastSearch loaded only 4
    data files: data_0, data_1, data_2, data_3. It seems that when the
    cache of Chrome is large enough, it starts to create more cache data
    files (data_4, data_5...) Starting from this version, MyLastSearch
    will read these additional cache data files.

* Version 1.61:
  o Fixed to work properly with the history data of Firefox 22.

* Version 1.60:
  o Added support for Internet Explorer 10. Be aware that in order to
    get accurate results for IE10, you may need to wait a few minutes
    after you exit from Internet Explorer, so the entire cache database
    will be written to the disk. Alternatively, you can log off and then
    log on again to force the writing to disk.
  o Fixed the 'Exclude the queries made by Google Instant' option to
    work properly again (there was a change in the URL format of Google)

* Version 1.58:
  o Fixed bug: In rare cases, MyLastSearch failed to read a few
    records of Internet Explorer history.
  o Added 'Auto Size Columns+Headers' option, which allows you to
    automatically resize the columns according to the row values and
    column headers.

* Version 1.57:
  o MyLastSearch now also reads the turbo subfolder located under the
    main cache folder of Opera Web browser.

* Version 1.56:
  o Fixed MyLastSearch to detect the correct cache folder of Firefox
    if the user changed it from Firefox config
    (browser.cache.disk.parent_directory).

* Version 1.55:
  o The search queries are now displayed while scanning the
    history/cache files of your Web browsers.
  o Added 'Stop' menu item displayed while scanning the Web browser
    data, which allows you to stop the scanning process.

* Version 1.50:
  o Added 'Mark Odd/Even Rows' option, under the View menu. When it's
    turned on, the odd and even rows are displayed in different color, to
    make it easier to read a single line.
  o On Windows Vista/7/2008: The cache of Internet Explorer is now
    loaded from both the base cache folder and the 'Low' subfolder. (In
    the previous versions, only one of them was loaded, according to the
    last modified date/time of the index.dat file)

* Version 1.49:
  o Fixed to work properly with the history file of Firefox 4 Beta.

* Version 1.48:
  o Fixed to work properly with the cache of Firefox 4 Beta.

* Version 1.47:
  o Fixed MyLastSearch to read the cache files of Chrome Web browser
    when it's opened and locks the files.

* Version 1.46:
  o Added 'Exclude the queries made by Google Instant' option. This
    option is turned on by default. The new 'Google Instant' feature
    generates a search query for every letter that the user type in the
    search box, and fills the search queries displayed by MyLastSearch
    with junk queries of incomplete words. This option removes all these
    junk queries.

* Version 1.45:
  o You can now send the search engine queries list to stdout by
    specifying an empty filename ("") in the command-line of all save
    parameters.
    For example: MyLastSearch.exe /stab "" >> c:\temp\queries.txt
  o Added 'Add Header Line To CSV/Tab-Delimited File' option. When
    this option is turned on, the column names are added as the first
    line when you export to csv or tab-delimited file.

* Version 1.44:
  o Fixed a problem with crash/exception when reading the cache of
    Chrome Web browser.

* Version 1.43:
  o Fixed MyLastSearch to work with Opera 10.50

* Version 1.42:
  o Added support for sorting the saved search queries list from
    command-line - /sort
  o Fixed MyLastSearch to automatically detect the cache folder of
    Opera 10.

* Version 1.41:
  o Added support for search queries of Microsoft Bing.

* Version 1.40:
  o Added support for search queries of Wikipedia, Friendster, hi5,
    Twitter, Facebook, and MySpace.

* Version 1.36:
  o Added support for Chrome 2.x

* Version 1.35:
  o Added filter by Web browser (in Advanced Options)

* Version 1.32:
  o Fixed bug: in some cases, MyLastSearch crashed when loading the
    cache of Firefox Web browser.

* Version 1.31:
  o Improved the support for Firefox 3 history file.

* Version 1.30:
  o Added support for the cache of Chrome Web browser.

* Version 1.25:
  o Added support for the cache of Opera Web browser.

* Version 1.21:
  o Fixed bug: MyLastSearch failed to work with history file of
    Firefox 3.0.1

* Version 1.20:
  o Added support for history files of Firefox 3.
  o Fixed bug: The main window lost the focus when the user switched
    to another application and then returned back to MyLastSearch.

* Version 1.14:
  o The URLs in HTML report are now created as links.

* Version 1.13:
  o Added support for YouTube search queries.

* Version 1.12:
  o Added support for saving into comma-delimited (.csv) file.
  o Added /scomma command-line option.

* Version 1.11:
  o Added support for AOL.

* Version 1.10:
  o Added Ask.com and Alexa search engines
  o Added support for images, news, video, and group searches.
  o Added 'Search Type' column.
  o Added /loadfrom command-line option

* Version 1.01 - Fixed support for reading the cache of Internet
  Explorer under Vista with UAC turned on.
* Version 1.00 - First release.



Using MyLastSearch
==================

MyLastSearch utility doesn't require any installation process or
additional DLL files. In order to start using it, simply copy the
executable file (MyLastSearch.exe) to any folder you like, and run it.
After running it, MyLastSearch scans the cache and history files of your
Web browsers (Internet Explorer and/or Firefox), and find all search
queries stored in them. The scanning process may take from a few seconds
to 1 minute, depending on the size of your cache and history files.
After the scanning process is finished, the main window should display
the list of all search queries the you made with the most popular search
engines.



Command-Line Options
====================



/loadfrom <IE History Folder> <IE Cache Folder> <Mozilla History File>
<Mozilla Cache Folder> <Opera Cache Folder> <Chrome Cache Folder>
Load the search queries from the specified cache/history folders of
Mozilla/IE/Opera. You can omit parameters that you don't need by
specifying an empty string in quotes - ""

/stext <Filename>
Save the search queries into a regular text file.

/stab <Filename>
Save the search queries into a tab-delimited text file.

/scomma <Filename>
Save the search queries into a comma-delimited text file.

/stabular <Filename>
Save the search queries into a tabular text file.

/shtml <Filename>
Save the search queries into HTML file (Horizontal).

/sverhtml <Filename>
Save the search queries into HTML file (Vertical).

/sxml <Filename>
Save the search queries to XML file.

/sort <column>
This command-line option can be used with other save options for sorting
by the desired column. If you don't specify this option, the list is
sorted according to the last sort that you made from the user interface.
The <column> parameter can specify the column index (0 for the first
column, 1 for the second column, and so on) or the name of the column,
like "Filename" and "Created Time". You can specify the '~' prefix
character (e.g: "~Created Time") if you want to sort in descending order.
You can put multiple /sort in the command-line if you want to sort by
multiple columns.

Examples:
MyLastSearch.exe /shtml "f:\temp\1.html" /sort 3
MyLastSearch.exe /shtml "f:\temp\1.html" /sort "~Search Engine" /sort
"Search Text"

/nosort
When you specify this command-line option, the list will be saved without
any sorting.

Examples:

MyLastSearch.exe /loadfrom "C:\Documents and Settings\Administrator\Local
Settings\History" "C:\Documents and Settings\Administrator\Local
Settings\Temporary Internet Files" "C:\Documents and
Settings\Administrator\Application
Data\Mozilla\Firefox\Profiles\dy18v2u5.default\history.dat" "C:\Documents
and Settings\Administrator\Local Settings\Application
Data\Mozilla\Firefox\Profiles\dy18v2u5.default\Cache"

MyLastSearch.exe /loadfrom "" "" "C:\Documents and
Settings\Administrator\Local Settings\Application
Data\Mozilla\Firefox\Profiles\dy18v2u5.default\Cache"

MyLastSearch.exe /shtml "c:\temp\search1.html" /loadfrom "C:\Documents
and Settings\Administrator\Local Settings\History" "C:\Documents and
Settings\Administrator\Local Settings\Temporary Internet Files"
"C:\Documents and Settings\Administrator\Application
Data\Mozilla\Firefox\Profiles\dy18v2u5.default\history.dat" "C:\Documents
and Settings\Administrator\Local Settings\Application
Data\Mozilla\Firefox\Profiles\dy18v2u5.default\Cache"

MyLastSearch.exe /shtml "c:\temp\search1.html"

MyLastSearch.exe /shtml "c:\temp\search1.html" /sort "~Search Time"



Translating MyLastSearch to other languages
===========================================

In order to translate MyLastSearch to other language, follow the
instructions below:
1. Run MyLastSearch with /savelangfile parameter:
   MyLastSearch.exe /savelangfile
   A file named MyLastSearch_lng.ini will be created in the folder of
   MyLastSearch utility.
2. Open the created language file in Notepad or in any other text
   editor.
3. Translate all string entries to the desired language. Optionally,
   you can also add your name and/or a link to your Web site.
   (TranslatorName and TranslatorURL values) If you add this information,
   it'll be used in the 'About' window.
4. After you finish the translation, Run MyLastSearch, and all
   translated strings will be loaded from the language file.
   If you want to run MyLastSearch without the translation, simply rename
   the language file, or move it to another folder.



License
=======

This utility is released as freeware. You are allowed to freely
distribute this utility via floppy disk, CD-ROM, Internet, or in any
other way, as long as you don't charge anything for this. If you
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

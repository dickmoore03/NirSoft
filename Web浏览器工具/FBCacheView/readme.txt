


FBCacheView v1.24
Copyright (c) 2013 - 2025 Nir Sofer
Web site: https://www.nirsoft.net



Description
===========

FBCacheView is a simple tool that scans the cache of your Web browser
(Internet Explorer, Firefox, or Chrome), and lists all images displayed
in Facebook pages that you previously visited, including profile
pictures, images uploaded to Facebook, and images taken from other Web
sites. For every Facebook image, the following information is displayed:
URL of the image, Web browser that was used to visit the page, image
type, date/time of the image, visit time, image file size, and external
URL (For images taken from another Web site).



System Requirements And Limitations
===================================


* This utility works in any version of Windows, starting from Windows
  XP and up to Windows 11. Both 32-bit and 64-bit systems are supported.
* The following Web browsers are supported: Internet Explorer, Mozilla
  Firefox, SeaMonkey, and Google Chrome. Opera is not supported because
  it stores the JPEG images in Webp format.
* FBCacheView won't work if you configure your Web browser to clear the
  cache after closing it.
* It's recommended to close all windows of your Web browser before
  using FBCacheView, to ensure that all cache files are saved to the disk.



Versions History
================


* Version 1.24:
  o Updated to read the cache files of the latest Chrome version
    (Version 132).
  o Fixed a crash problem when reading the old IE11 cache file
    (WebCacheV01.dat) on Windows 11 24H2.

* Version 1.23:
  o Updated to read the cache files of the latest Chrome version.

* Version 1.22:
  o Updated to read the Cache_Data subfolder in the new version of
    Chrome Web browser.
  o Updated to work properly with the cache partitioning string on
    the latest versions of Chrome.

* Version 1.21:
  o Updated to work properly with the cache partitioning of Chrome
    and Firefox.

* Version 1.20:
  o Added support for the new 'Simple Cache for HTTP' cache format of
    Chrome Web browser.

* Version 1.17:
  o FBCacheView now automatically detects the cache folder of Pale
    Moon Web browser.

* Version 1.16:
  o Updated FBCacheView to work with the current URLs of Facebook.

* Version 1.15:
  o FBCacheView now also shows all Instagram images stored in the
    cache.
  o Added 'Show Facebook Images' and 'Show Instagram Images' to the
    Options menu.

* Version 1.12:
  o FBCacheView now automatically detects the cache folder of Vivaldi
    Web browser.

* Version 1.11:
  o Fixed bug: FBCacheView failed to read the cache of IE11 on some
    systems.

* Version 1.10:
  o FBCacheView now automatically detects the cache folders of
    Chromium and Yandex.

* Version 1.07:
  o Fixed to work with the latest build of Windows 10/IE11.

* Version 1.06:
  o Fixed bug: Unicode Byte order mark (FF FE) was added to xml/html
    files.

* Version 1.05:
  o Added support for the new cache structure of Firefox 32.

* Version 1.03:
  o Added secondary sorting support: You can now get a secondary
    sorting, by holding down the shift key while clicking the column
    header. Be aware that you only have to hold down the shift key when
    clicking the second/third/fourth column. To sort the first column you
    should not hold down the Shift key.

* Version 1.02:
  o Added 'Explorer Copy' option (Ctrl+P), which allows you to copy
    one or more files and then paste them into opened folder in Windows
    Explorer.

* Version 1.01:
  o Added 'Copy External URL' option.
  o Fixed to display date/time values according to daylight saving
    time settings.

* Version 1.00 - First release.



Start Using FBCacheView
=======================

FBCacheView doesn't require any installation process or additional DLL
files. In order to start using it, simply run the executable file -
FBCacheView.exe

After running it, FBCacheView begins to scan the cache of your Web
browser and displays the list of all images loaded from Facebook Web
pages. You may need to wait up to a few minutes until the scanning
process is finished. After the scanning process is finished, you can also
watch the image in the lower pane of FBCacheView, by selecting the
desired item in the upper pane.

If from some reason FBCacheView fails to detect the cache of your Web
browser properly, you can go to 'Advanced Options' window (F9), and
choose the desired cache folders to scan for each Web browser.



Columns Description
===================


* URL: The URL of the image on Facebook.
* Web Browser: The Web browser that stores the specified Facebook image
  file in the cache.
* Image Type: The type of the image: Profile image, uploaded image, or
  external image taken from another Web site. For 'External Image' type,
  the original URL of the image is displayed on 'External URL' column.
* Image Time: The date/time of the image as returned by the Web server
  of Facebook. This column usually represents the time that the image was
  uploaded to Facebook.
* Browsing Time: The last time that the specified Facebook image was
  loaded by your Web browser.
* File Size: The file size of the image.
* Filename: The full path of the image filename in the cache of your
  Web browser.
* External URL: Displays the original URL of the image (Only for
  external images)



Command-Line Options
====================



/stext <Filename>
Save the Facebook cached images list into a simple text file.

/stab <Filename>
Save the Facebook cached images list into a tab-delimited text file.

/scomma <Filename>
Save the Facebook cached images list into a comma-delimited text file
(csv).

/stabular <Filename>
Save the Facebook cached images list into a tabular text file.

/shtml <Filename>
Save the Facebook cached images list into HTML file (Horizontal).

/sverhtml <Filename>
Save the Facebook cached images list into HTML file (Vertical).

/sxml <Filename>
Save the Facebook cached images list into XML file.



Translating FBCacheView to other languages
==========================================

In order to translate FBCacheView to other language, follow the
instructions below:
1. Run FBCacheView with /savelangfile parameter:
   FBCacheView.exe /savelangfile
   A file named FBCacheView_lng.ini will be created in the folder of
   FBCacheView utility.
2. Open the created language file in Notepad or in any other text
   editor.
3. Translate all string entries to the desired language. Optionally,
   you can also add your name and/or a link to your Web site.
   (TranslatorName and TranslatorURL values) If you add this information,
   it'll be used in the 'About' window.
4. After you finish the translation, Run FBCacheView, and all
   translated strings will be loaded from the language file.
   If you want to run FBCacheView without the translation, simply rename
   the language file, or move it to another folder.



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

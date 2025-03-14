


ImageCacheViewer v1.32
Copyright (c) 2014 - 2024 Nir Sofer
Web site: https://www.nirsoft.net



Description
===========

ImageCacheViewer is a simple tool that scans the cache of your Web
browser (Internet Explorer, Firefox, or Chrome), and lists the images
displayed in the Web sites that you recently visited.
For every cached image file, the following information is displayed: URL
of the image, Web browser that was used to visit the page, image type,
date/time of the image, browsing time, and file size.
When selecting a cache item in the upper pane of ImageCacheViewer, the
image is displayed in the lower pane, and you can copy the image to the
clipboard by pressing Ctrl+M.



Versions History
================


* Version 1.32:
  o Updated to read the cache files of the latest Chrome version.

* Version 1.31:
  o Fixed to read the cache of Chrome Web browser while it's opened.

* Version 1.30:
  o Updated the preview pane to display webp image files.

* Version 1.27:
  o Updated to read the Cache_Data subfolder in the new version of
    Chrome Web browser.

* Version 1.26:
  o Updated to work properly with the cache partitioning string on
    the latest versions of Chrome.

* Version 1.25:
  o Fixed to extract the URL correctly from the latest versions of
    Firefox.
  o Added 'Web Site' column, which shows the Web site that loaded the
    image (For Firefox and Chrome Web browsers) .

* Version 1.21:
  o Updated to work properly with the new cache partitioning of
    Chrome. (In previous versions, URL was displayed with _dk_ prefix).

* Version 1.20:
  o Added support for the new 'Simple Cache for HTTP' cache format of
    Chrome Web browser.

* Version 1.15:
  o ImageCacheViewer now automatically detects the cache folder of
    Pale Moon Web browser.

* Version 1.12:
  o ImageCacheViewer now automatically detects the cache folder of
    Vivaldi Web browser.

* Version 1.11:
  o Fixed bug: ImageCacheViewer failed to read the cache of IE11 on
    some systems.

* Version 1.10:
  o ImageCacheViewer now automatically detects the cache folders of
    Chromium and Yandex.

* Version 1.08:
  o Fixed to work with the latest build of Windows 10/IE11.

* Version 1.07:
  o ImageCacheViewer now automatically detects the cache folder of
    Opera 15 or later (Which has the same cache structure of Google
    Chrome...)

* Version 1.06:
  o Fixed bug: Unicode Byte order mark (FF FE) was added to xml/html
    files.

* Version 1.05:
  o Added support for the new cache structure of Firefox 32.

* Version 1.00 - First release.



System Requirements And Limitations
===================================


* This utility works in any version of Windows, starting from Windows
  XP and up to Windows 11. Both 32-bit and 64-bit systems are supported.
* The following Web browsers are supported: Internet Explorer, Mozilla
  Firefox, SeaMonkey, and Google Chrome.
* ImageCacheViewer won't work if you configure your Web browser to
  clear the cache after closing it.
* It's recommended to close all windows of your Web browser before
  using ImageCacheViewer, to ensure that all cache files are saved to the
  disk.



Start Using ImageCacheViewer
============================

ImageCacheViewer doesn't require any installation process or additional
DLL files. In order to start using it, simply run the executable file -
ImageCacheViewer.exe

After running ImageCacheViewer, it begins to scan the cache of your Web
browser, and displays all cached images from Web sites you visited in the
last day. If you want to get images from other days, you can remove or
change the last 1-day filter from the 'Advanced Options' window (F9).

After the scanning process is finished, you can also watch the image in
the lower pane of ImageCacheViewer, by selecting the desired item in the
upper pane.

If from some reason ImageCacheViewer fails to detect the cache of your
Web browser properly, you can go to 'Advanced Options' window (F9), and
choose the desired cache folders to scan for each Web browser.



Command-Line Options
====================



/stext <Filename>
Save the cached images list into a simple text file.

/stab <Filename>
Save the cached images list into a tab-delimited text file.

/scomma <Filename>
Save the cached images list into a comma-delimited text file (csv).

/stabular <Filename>
Save the cached images list into a tabular text file.

/shtml <Filename>
Save the cached images list into HTML file (Horizontal).

/sverhtml <Filename>
Save the cached images list into HTML file (Vertical).

/sxml <Filename>
Save the cached images list into XML file.



Translating ImageCacheViewer to other languages
===============================================

In order to translate ImageCacheViewer to other language, follow the
instructions below:
1. Run ImageCacheViewer with /savelangfile parameter:
   ImageCacheViewer.exe /savelangfile
   A file named ImageCacheViewer_lng.ini will be created in the folder of
   ImageCacheViewer utility.
2. Open the created language file in Notepad or in any other text
   editor.
3. Translate all string entries to the desired language. Optionally,
   you can also add your name and/or a link to your Web site.
   (TranslatorName and TranslatorURL values) If you add this information,
   it'll be used in the 'About' window.
4. After you finish the translation, Run ImageCacheViewer, and all
   translated strings will be loaded from the language file.
   If you want to run ImageCacheViewer without the translation, simply
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




OperaCacheView v1.40
Copyright (c) 2008 - 2012 Nir Sofer
Web site: http://www.nirsoft.net



Description
===========

OperaCacheView is a small utility that reads the cache folder of Opera
Web browser, and displays the list of all files currently stored in the
cache. For each cache file, the following information is displayed: URL,
Content type, File size, Last accessed time, and last modified time in
the server.
You can easily select one or more items from the cache list, and then
extract the files to another folder, or copy the URLs list to the
clipboard.



System Requirements
===================

This utility works on any version of Windows, From Windows 98 to Windows
7. However, for Windows 98/ME, you have to download the non-Unicode
version.
You can use this utility even if Opera Web browser is not installed on
your system, as long as you have the entire cache folder that you want to
inspect.



Know Problem
============

The new version of Opera now save or compress the files in different
format and put them in a subfolder under the main folder. Currently,
OperaCacheView cannot extract the files in the new format, and thus
copying the cache files won't work in the new versions of Opera. I hope
that this problem will be fixed in future version.

Versions History
================


* Version 1.40:
  o OperaCacheView now also reads the turbo subfolder located under
    the main cache folder.

* Version 1.37:
  o Partial fix for copying the cache files of Opera 10.50:
    OperaCacheView can now copy the cache files properly, but they will
    be usable only if they are not compresses.

* Version 1.36:
  o Fixed OperaCacheView to read the cache index file of Opera 10.50

* Version 1.35:
  o Added 'Explorer Copy' option, which allows you to copy the cache
    files into the clipboard, and then paste them into Explorer window.
  o Added 'Delete Selected Cache Files' option.
  o Added 'Mark Missing Files' option.
  o Added 'Hide Missing Files' option.

* Version 1.31:
  o Fixed OperaCacheView to automatically detect the default cache
    folder of Opera 10.

* Version 1.30:
  o Added support for saving cache files from command-line.

* Version 1.25:
  o Added new option in 'Copy Selected Cache Files': Update the
    modified time of the copied files according to modified time in the
    Web server.

* Version 1.20:
  o Added support for cache filter. (Display only URLs which contain
    the specified filter strings)

* Version 1.15:
  o Added 'Show Zero-Length Files' option.
  o Added fileter by file type. (text/html, image, audio, video,
    application)

* Version 1.11:
  o New option in 'Select Folder' dialog-box: 'Remember this folder
    in the next time that you use OperaCacheView'

* Version 1.10:
  o New option in 'Copy Selected Files To...': Save the files in the
    directory structure of the Web site.

* Version 1.06:
  o Fixed bug: OperaCacheView created invalid XML file.

* Version 1.05:
  o Added new columns: ETag, Server Response, Content Encoding.

* Version 1.02:
  o Fixed the 'Missing File' column name.
  o Added 'Encoding' column.
  o Added error messages for empty cache index file and for missing
    cache index file.

* Version 1.01 - Added message with error code when OperaCacheView
  fails to load the cache
* Version 1.00 - First release.



Using OperaCacheView
====================

OperaCacheView doesn't require any installation process or additional DLL
files. Just copy the executable file (OperaCacheView.exe) to any folder
you like, and run it.
After you run it, the main window displays the list of files currently
stored in the cache of Opera. If you want to view the cache folder from
another location, simply use the 'Select Cache Folder' option (F9), and
choose the desired cache folder.
You can select one or more cache files from the list, and than export the
list into text/html/xml file ('Save Selected Items' option), copy the URL
list to the clipboard (Ctrl+U), copy the entire table of cache files
(Ctrl+C), and then paste it to Excel or to OpenOffice spreadsheet. You
can also extract the actual files from the cache, and save them into
another folder, You can do that by using the 'Copy Selected Cache Files
To' option (F4).

Notice: The cache items are added to the cache index file only after you
close the relevant window or tab. This means that in order to get the
cache items of a page that is currently opened, you must close it, and
then refresh the list in OperaCacheView (F5).



Command-Line Options
====================



/stext <Filename>
Save the list of all cache files into a regular text file.

/stab <Filename>
Save the list of all cache files into a tab-delimited text file.

/scomma <Filename>
Save the list of all cache files into a comma-delimited text file.

/stabular <Filename>
Save the list of all cache files into a tabular text file.

/shtml <Filename>
Save the list of all cache files into HTML file (Horizontal).

/sverhtml <Filename>
Save the list of all cache files into HTML file (Vertical).

/sxml <Filename>
Save the list of all cache files to XML file.

-folder <Cache Folder>
Start OperaCacheView with the specified cache folder.

/copycache <URL> <Content Type>
Copy files from the cache into the folder specified in /CopyFilesFolder
parameter. In the <URL> parameter, you can specify the URL of the Web
site (for example: http://www.nirsoft.net) or empty string ("") if you
want to copy files from all Web sites. In the <Content Type> parameter,
you can specify full content type (like image/png), partial content type
(like 'image') or empry string ("") if you want to copy all types of
files.

/CopyFilesFolder <Folder>
Specifies the folder to copy the cache files.

/UseWebSiteDirStructure 0 | 1
Save the files in the directory structure of the Web site. 0 = No, 1 = Yes

/UpdateModifiedTime 0 | 1
Update the modified time of the copied files according to modified time
in the Web server. 0 = No, 1 = Yes

/NewNameIfExist 0 | 1
Copy as new name if filename already exists. 0 = No, 1 = Yes

Copy Cache Examples:
* Copy all cache files of www.nirsoft.net to f:\temp in the directory
  structure of the Web site:
  /copycache "http://www.nirsoft.net" "" /CopyFilesFolder "f:\temp"
  /UseWebSiteDirStructure 1


* Copy all image cache files of www.nirsoft.net to f:\temp:
  /copycache "http://www.nirsoft.net" "image" /CopyFilesFolder "f:\temp"
  /UseWebSiteDirStructure 0


* Copy all .png files from the cache to f:\temp:
  /copycache "" "image/png" /CopyFilesFolder "f:\temp"
  /UseWebSiteDirStructure 0


* Copy all files from the cache to f:\temp:
  /copycache "" "" /CopyFilesFolder "f:\temp" /UseWebSiteDirStructure 0





Translating OperaCacheView to other languages
=============================================

In order to translate OperaCacheView to other language, follow the
instructions below:
1. Run OperaCacheView with /savelangfile parameter:
   OperaCacheView.exe /savelangfile
   A file named OperaCacheView_lng.ini will be created in the folder of
   OperaCacheView utility.
2. Open the created language file in Notepad or in any other text
   editor.
3. Translate all string entries to the desired language. Optionally,
   you can also add your name and/or a link to your Web site.
   (TranslatorName and TranslatorURL values) If you add this information,
   it'll be used in the 'About' window.
4. After you finish the translation, Run OperaCacheView, and all
   translated strings will be loaded from the language file.
   If you want to run OperaCacheView without the translation, simply
   rename the language file, or move it to another folder.



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

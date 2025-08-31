## Product:
EasyWeb FileManager Module (home.postnuke.ru)

## Released:
07/23/2004

## Description:
EasyWeb FileManager Module for PostNuke is vulnerable to a directory traversal problem which allows retrieval of arbitrary files from the remote system.

## Systems Affected:
EasyWeb FileManager 1.0 RC-1

## Technical Description:
The PostNuke module works by loading a directory and/or file via the "pathext" (directory) and "view" (file) variables. Providing a relative path (from the document repository) in the "pathext" variable will cause FileManager to provide a directory listing of that diretory. Selecting a file in that listing, or putting a file name in the "view" variable, will cause EasyWeb to load the file specified. Only files and directories which can be read by the system user running PHP can be retrieved.

This URL will show the /etc direcotry (assuming PostNuke is installed at the root level):

http://[victim]/index.php?module=ew_filemanager&type=admin&func=manager&pathext=../../../etc
This URL will show the /etc/passwd file (assuming PostNuke is installed at the root level):

http://[victim]/index.php?module=ew_filemanager&type=admin&func=manager&pathext=../../../etc/&view=passwd

## Fix/Workaround:
Use another file manager module for PostNuke, as the authors do not appear to be maintaining FileManager.

## Vendor Status:
Vendor was contacted but did not respond.

## References:
- OSVDB-8193	EasyWeb FileManager Directory Traversal


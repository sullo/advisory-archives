## Product:
Alkalay.net Scripts

## Released:
09/20/2005

## Description:
Multiple perl scripts from alkalay.net contain remote command execution or arbitrary file retrieval vulnerabilities.

## Software Affected:
- man-cgi (Command Execution)
- notify (Command Execution)
- nslookup.cgi (Command Execution)
- contribute.cgi/contribute.pl (File Retrieval)

## Technical Description:
Various perl scripts on alkalay.net act on unsafe data from the client, which can allow command execution on the web server or retrieval of arbitrary files from the web server (both as the web server user).

## Vendor Status:
Avi Alkalay was notified on 09/12/2005 but did not respond.

## References:
- OSVDB-19519	Avi Alkalay man-cgi topic Variable Arbitrary Command Execution
- OSVDB-19520	Avi Alkalay nslookup.cgi query Variable Arbitrary Command Execution
- OSVDB-19521	Avi Alkalay notifiy from Variable Arbitrary Command Execution
- OSVDB-19522	Avi Alkalay contribute.cgi/contribute.pl template Variable Arbitrary File Retrieval

## Product:
Apache Cocoon

## Released:
03/13/2004

## Description:
Apache Cocoon 2.1.4 and below are vulnerable to an installation path disclosure.

## Systems Affected:
- Apache Cocoon 2.1.4
- Apache Cocoon 1.7.1

## Technical Description:
Default error pages in various versions of the Apache Cocoon Java server reveal the file system path to the Cocoon installation directory.

These URLs will show the path to the Cocoon directory:

- Cocoon 2.1.4: http://[victim]/non-existing-directory/
- Cocoon 1.7.1: http://[victim]/non-existing-file.xml

## Fix/Workaround:
Set custom error pages which do not reveal system information.

## Vendor Status:
Vendor was contacted on 3/13/2004.

## References:
- OSVDB-4231Apache Cocoon Error Page Server Path Disclosure

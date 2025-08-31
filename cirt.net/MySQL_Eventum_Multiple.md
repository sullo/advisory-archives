## Product:
MySQL Eventum Issue / Bug Tracking System

## Released:
12/28/2004

# Default Vendor Account
## Description:
MySQL Eventum 1.3.1 contains an undocumented administrator account with an unknown password.

## Systems Affected:
- MySQL Eventum 1.3.1
- MySQL Eventum 1.3
- MySQL Eventum 1.2.2
- MySQL Eventum 1.2.1
- MySQL Eventum 1.2
- MySQL Eventum 1.1

## Technical Description:
The Eventum bug tracking system contains an enabled administrator account which is not documented. Afer a succesful installation, the system notifies you to change the password and login information for default administrator account admin@example.com), but does not mention system-account@example.com.

The account is created with an MD5 encrypted password which resisted basic dictionary cracking attempts, however anyone knowing the password (i.e., someone from the Eventum dev team, or via cracking) would be allowed login to any Eventum system.

# XSS
## Description:
MySQL Eventum 1.3.1 contains multiple multiple cross site scripting (XSS) vulnerabilities.

## Technical Description:
The Eventum bug tracking system has multiple variables that do not filter user supplied input. This could allow an attacker to perform Cross Site Scripting (XSS)
attacks.

XSS is possible in the following pages/fields:

- index.php, email field: index.php?err=3&email="><script>alert(document.cookie)</script>
- forgot_password.php, email field: forgot_password.php?email="><script>alert(document.cookie)</script>
- preferences.php, fields: full_name, sms_email, list_refresh_rate, emails_refresh_rate
- projects.php, fields: title, outgoing_sender_name
- The preferences.php will save the XSS values and display them to any user that views the user's information (i.e., and administrator). These fields are escaped to prevent SQL injection attacks.

## Fix/Workaround:
MySQL reports Eventum release 1.4 resolves this issue.

## Vendor Status:
MySQL was notified on 12/28/2004. The MySQL bug report system immediately makes issues public, which is why this release coincides with vendor disclosure.

## References:
- OSVDB-12605	MySQL Eventum Default Vendor Account

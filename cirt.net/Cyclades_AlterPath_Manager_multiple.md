## Product:
AlterPath Manager (APM) Console Server

## Released:
01/23/2005

## Systems Affected:
AlterPath Manager 1.1.0 and below

# Admin Access
## Description:
AlterPath Manager (APM) allows any connected user grant themselves administrator access.

## Technical Description:
Any authorized user of the APM 1.1.0 web interface can grant themselves administrator access. When saveUser.do is called, it does not confirm the user has access to modify user accounts. By changing the adminUser value to "true", their user account can be saved and granted administrative privleges.

In the URL below, replace my_id, My+name, email and other user information as desired. Set the adminuser equal to "true" to grant escalated privileges--this will grant the user identified by userID (userID is an internal Cyclades identifier--it can be found in certain APM URLs or HTML pages):

- /application/saveUser.do?userId=9&password=&userName=my_id&fullName=My+name&department=Security&location=Work&phone=555-1212&mobile=&pager=
&email=test%40example.com&status=Enable&localPassword=true&adminUser=true&forward=&action=Save

# Arbitrary Console Connection
## Description:
AlterPath Manager (APM) allows any connected user to access any console, ignoring access restrictions connected to the AlterPath.

## Technical Description:
Access restrictions in the APM prevent users from seeing consoles they are not allowed to connect to. However, this can be bypassed by simply specifying any console's name in the consoleConnect.jsp URL. Once the URL is changed and loaded, the user will be taken directly to the console.

Example (substitute "console_name" with the real name of a console defined in the APM):
- /usermode/consoleConnect.jsp?consolename=console_name
- Note: In versions 1.2.0 and 1.2.1 of the APM, the user must have at one time been authorized to access the console, and have actually connected to it via the web interface. If the user's access to that console is removed, they are still able to access the console via URL modification.

# Information Disclosure
## Description:
AlterPath Manager (APM) reveals sensitive system information without authentication.

## Technical Description:
The APM reveals sensitive information unauthenticated through the web interface via the /about.html page.
- Boot Version
- Kernel Version
- Config Version
- OS Version
- AP Version
- Hardware information


## Fix/Workaround:
Upgrade to version 1.2.0 or higher.

## Vendor Status:
- Cyclades was notified on 12/13/2004 and confirmed receipt on 12/14/2004.
- Cyclades responded to an inquiry on 1/20/2005 to confirm version 1.2.5 would address this issue.
- Cyclades responded to an inquiry on 2/15/2005 to state they still did not have a release date, but did not respond with more information.
- Released on 2/23/2005.
- Cyclades responded on 2/25/2005 to clear up version information.

## References:
- OSVDB-14074Cyclades AlterPath Manager Privilege Escalation

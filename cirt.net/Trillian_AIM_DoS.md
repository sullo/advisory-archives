## Product:
Trillian Pro and Basic 3.1 Build 121

## Released:
02/28/2006

## Description:
It is possible to remotely crash Trillian by sending an empty IM with the AOL AIM protocol. This attack is easily repeatable. The attack does not require the Trillian user to accept the message or have the user in their contact list. Trillian will display an incoming message from the attacker, but does not show any text.

The error message upon crash is:



## Systems Affected:
- Trillian Basic 3.1 Build 121
- Trillian Pro 3.1 Build 121

## Fix/Workaround:
Upgrade to version 3.1.0.122 or higher.

## Vendor Status:
- Cerulean studios was notified on 02/01/2006.
- Cerulean released 3.1.0.126 of the AOL plugin 02/2?/2006.
- Released on 02/28/2006.

## Thanks:
Jericho/attrition.org for being a guinea pig while investigating the Trillian RTF DoS and eventually finding this one, as well as Zel for suffering several unexpected disconnections.

## References:
- OSVDB-23528	Cerulean Studios Trillian Blank AIM Message DoS

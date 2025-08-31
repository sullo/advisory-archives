## Product:
Netgear Gateway Router RT311/RT314/FR314, firmware versions 3.22, 3.24 and 3.25

## Released:
02/03/2002

## Description:
Netgear's RT314 is a four-port gateway router targeted at the small home or small office network.

## Systems Affected:
- RT311
- RT314
- FR314
- RP114
Tested on a Netgear RT314 running firmware versions 3.22, 3.24 and 3.25. Any hardware running this firmware. Any product running ZyXel-RomPager web server 3.02 or earlier is probably also vulnerable.

## Not Affected:
- RO318

## Problem Description:
The Netgear RT314 Gateway Router (FW v3.25) runs a web server (ZyXEL-RomPager/3.02) for easy user configuration. This web server is vulnerable to the standard Cross Site Scripting problems seen in multiple web servers (published in early 2000). Though it may be difficult to exploit (attacker would need to know the address of the victim's router), it still opens the possibility that an attacker could gain unauthorized access to the router, and possibly reconfigure it to allow remote access.

To check Netgear devices for CSS, simply access the following URL in a browser:
- http://<router_ip>/<script>alert('Vulnerable')</script>

## Fix/Workaround:
There is currently no vendor fix for this problem. Rzac has pointed out information on Netgear.org (not affiliated with Netgear) which describes a method of disabling all access to the internal interface of the router. See http://www.netgear.org/pages/how-to.htm for details.

## Vendor Status:
Vendor was contacted on 1/5/2002 (support@netgear.com), but did not respond.

## References:
- CVE: CAN-2002-0238
- Bugtraq: BID-4024
- ISS: XF-8082

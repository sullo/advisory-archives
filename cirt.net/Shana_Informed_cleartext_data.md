## Released:
09/24/2002

## Product Description:
Shana Corporation provides eForm solutions and is the developer of Informed. Their solution is used by more than two million people around the world. Shana's Informed has been chosen by a wide range of organizations in more than 65 countries worldwide. Shana's customer base spans many industries, notably the Aerospace and Digital Government sectors. Shana has strategic technology partnerships with a number of companies, including FileNET Corporation and Entrust Technologies. Other partners include Apple Computer, EDS, Microsoft, NCR, Oracle, and Sierra.

## Event Description:
Shana's Informed product accesses information from disk and pads it into the Informed document. When an Informed document is opened with a hex editor or Microsoft's Wordpad sensitive information may be stored in the clear at the very bottom of the file. The information stored in the clear has been identified to have come from other documents on a user's workstation has well as clear-text data from the actual Informed file as well.

## Risk Explanation:
The Informed files may contain sensitive personal or corporate information that can be viewed by anyone has access to the encrypted file.

## Applications Affected:
- Informed Filler v3.05
- Informed Designer v3.05.

## Solution:
Upgrade to Shana's Informed Filler and Informed Designer release 4.0.

## Timeline:
- The problem was reported to Shana via E-Mail on Saturday, June 29th 2002 4:20pm.
- A response from Shana was received on July 1st explaining that the information had been passed on to the development team for evaluation.
- A follow-up was sent to Shana via E-Mail on Sunday, July 21st 2002 12:38pm again requesting timeframes for addressing the security issue.
- A response acknowling the problem and detailing a fix was received on Tuesday, July 23 2002 12:55pm.

## Vendor Status:
Response: "Thank-you for bringing this issue to our attention. We have fixed the issue in our newest release 4.0. Some file space allocation growth functions were not "zeroing" out new disc space as the file grew. Unused blocks were being captured into the form data, along with any data that may have resided on that location of the drive. The complete file growth areas are now made null to avoid any unwanted data from being captured. It may be worth noting that this does not occur in Windows XP, as the operating system takes better care of this on its own."

References:
- OSVDB: OSVDB-4151
- Bugtraq: BID-5795
- ISS: XF-10192

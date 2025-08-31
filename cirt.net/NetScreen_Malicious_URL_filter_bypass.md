## Released:
11/15/2002

## Product Description:
NetScreen Technologies Inc. is a leading developer of integrated network security solutions that offer the security, performance and total cost of ownership required by enterprises and carriers. NetScreen's innovative solutions provide key security technologies, such as virtual private network, denial of service protection, firewall and intrusion prevention, in a line of easy-to-manage security appliances and systems. NetScreen has created a new function to assist in the containment of malicious worms called the "User-Definable Malicious URL" feature. This will cause requests to be blocked that match the defined pattern.

## Event Description:
From the command line a firewall administrator can define a Malicious URL pattern to be blocked. However, if a segmented request for a blocked pattern is fragmented in the middle of the pattern, it will not be matched. This can be accomplished using a tool such as fragroute available at http://www.monkey.org/~dugsong/fragroute/

## Risk Explanation:
The product does not function properly to help contain malicious worms.

## Applications Affected:
Tested on NS-100; ScreenOS versions 2.7.1, 2.8, 3.0, 3.1, 4.0; HW Version: 3110

## Solution:
Upgrade to ScreenOS 4.0.1 release available 11/25/2002. See the Netscreen advisory for upgrade information.

## Timeline:
- The problem was reported to Netscreen via E-Mail on Tuesday, October 08, 2002 11:23 PM.
- Another email was sent to Netscreen vial E-Mail on Tuesday, November 12, 2002 12:35 AM
- Response #1 was received acknowledging the issue on Thursday, November 14, 2002 9:25 PM
- Response #2 was received will the solution on Saturday, November 23, 2002 5:44 PM

## Vendor Status:
- Response #1: "NetScreen has received your e-mail regarding the Malicious URL feature and we are currently in the process of developing a formal response to this issue. We are also readying changes to our product addressing this issue which will be included in the upcoming ScreenOS 4.0.1 release. We request that you delay publicly announcing this issue until we have officially released that software. We intend to release ScreenOS 4.0.1 before Thanksgiving. We will contact you before the release date to coordinate our announcements. Thank you for your cooperation."
- Response #2: "We have finished the ScreenOS 4.0.1 release, which addresses the circumvention of the Malicious URL feature using IP fragments. We are making the release available to our customers by 1:00PM on Monday (11/25). We will be releasing a formal statement to bugtraq and CERT approximately 15 minutes later (at 1:15PM.) If you will release an announcement of your own, please refrain from sending them prior to our 11/25 1:00PM release date. We are delaying our alerts by 15 minutes in order for your announcement to appear first. Thank you again for cooperating with our release schedule."


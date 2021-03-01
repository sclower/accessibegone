# AccessiBe Gone

If you are blind or low vision and rely on assistive technologies like screen readers, you may have begun finding popular websites becoming less usable-- all in the same ways:

*   Shortly after the page loads, you hear a prompt to either "Press ALT+1 to enable screen reader mode," or "to activate screen reader mode, click the first button of the website." This text repeats endlessly every ten seconds and interrupts anything you might be doing on the page.
*   Activating the screen reader mode introduces unexpected results, such as many nonsensical headings where there were none, oddly named forms, JavaScript code, or a single massive block of text which renders the entire site unusable.

If you have been scratching your head looking for the answer to this vexing plague, the answer is a piece of technology called an accessibility overlay-- rather, a piece of technology masquerading as an accessibility overlay. Most recently, a company known as AccessiBe has been selling and delivering software to thousands of websites, claiming that their one-line solution will make their sites accessible and save them from legal action. The claim is that artificial intelligence negates the need for any knowledge of accessible design patterns. Unfortunately, many businesses believe AccessiBe's claims and integrate the overlay with no thought to whether the technology actually delivers.

For more background on AccessiBe and their current hostile stance towards the disabled, you are encouraged to read [this thorough post by Adrian Roselli](https://adrianroselli.com/2020/06/accessibe-will-get-you-sued.html). Rather than repeat what has already been documented elsewhere, this page describes how to ban AccessiBe from ever reaching your computer and disrupting your online web experience. Note: the approaches below are exemplary. There are, as they say, many ways to skin a cat.

## What to Block

The AccessiBe software is delivered from two domain hosts-- both of which point to the same IP address:

*   acsbap.com
*   acsbapp.com

At a minimum, blocking these domains on your device of choice (or preferably your local network) will be sufficient. You may also wish to block the IP address altogether, though this may change once in a while. At the time of writing, the address is 167.172.136.187\. If in doubt, perform a ping on either domain to obtain the correct IP address.

## How to Block the AccessiBe Domains

### Using an Ad Blocker

A couple of enterprising persons have also taken it upon themselves to create custom AccessiBe block rules that run directly in your browser. For users of AdBlock Plus, Derek Riemer has created [this filter](https://files.derekriemer.com/evilA11yNasties.txt). Users of Apple devices are encouraged to install [Better](https://better.fyi/) which already blacklists AccessiBe and many other bad actors.

### Windows Instructions

The below instructions demonstrate how to block the current AccessiBe overlay distribution IP address via the Windows Firewall. If you are comfortable editing the system hosts file (located in C:\Windows\System32\Drivers\etc), then by all means do so.

1.  In the Start Menu, type "firewall" and press Enter. The Windows Firewall application opens.
2.  Click the "Advanced Options" link. Answer Yes to the User Account Control if it appears.
3.  In the "Windows Defender Firewall with Advanced Security" screen, select the outbound rules treeview item, click the Action menu and select New Rule.
4.  Select the custom rule option.
5.  Choose to apply this rule to all programs.
6.  Set the protocol type to any.
7.  Select "These IP Addresses" and click Add.
8.  In the IP addition screen, select "This IP or Subnet" and enter 167.172.136.187 for the IP address you wish to block, then click OK.
9.  On the following screen, choose to block the connection.
10.  Next, check the items where the rule should apply. The default is for the new filter to apply to the current domain, public, and private networks.
11.  Finally, give the rule a name, and click Finish.
12.  Close the Windows Firewall.

### Mac OS and Linux Instructions

This procedure describes how to edit the hosts file on a Mac to block the AccessiBe domain names. The following steps will also apply to any modern UNIX or Linux like operating system (including some routers and single-board computers such as the Raspberry Pi). If you are using Linux, open a terminal or console window and follow the instructions for editing the hosts file only.

1.  Press Command + Space to open the Spotlight Search. Type "terminal" and press Return.
2.  When the terminal window opens, type "sudo nano /etc/hosts" followed by Return.
3.  At this point you will be prompted for your administrative password. Type it and press Return.
4.  The nano text editor opens. If you have never used nano before, [this guide](https://wiki.gentoo.org/wiki/Nano/Basics_Guide) may be useful.
5.  press the Down Arrow until you reach the line which reads "127.0.0.1 localhost". Press the Down Arrow once more and Return once or twice to add a blank line.
6.  Enter the following exactly as shown: tip, you may copy the following line to the clipboard and paste it directly into the file

7.  Review the change, ensuring there are spaces between the IP address and two domain names.
8.  If all looks good, press Ctrl + X to exit nano. You will be asked if you wish to save your changes. Press Y followed by Return.
9.  At this point you are finished and can press Command + Q to quit the terminal application.

## Check Your Setup

Due to browser security, this page cannot accurately test whether AccessiBe has been successfully blocked. Therefore, the most reliable way to find out is to visit a page which embeds the overlay. A few examples include [Name Cheap](https://www.namecheap.com) or [Ham Radio Outlet](https://www.hamradio.com).

If you do not hear any prompt to press a command for screen reader mode, and more importantly if no such items appear on the above pages after a few seconds, then congratulations! You have taken back control of the web.

## Is That All?

Unfortunately, no. While AccessiBe is the worst offender today, other companies are engaging in similar deceitful practices. Over time instructions for blocking them will be integrated into this page.

Please pass these instructions on to anyone else who would benefit. The web belongs to all of us. Let's reclaim it. Thanks for reading.

No felines were injured during the creation of this document.
---
title: Setting up for access on a local network
description: Torrent Remote Documentation
---
> **Note**
> 
> You must follow the steps on the page  [Turning on the Web UI in
> uTorrent](turning-on-web-ui.html)
> before setting up access on a local network.

Setting up your uTorrent desktop program for remote access on a local network is fairly simple. To outline, the following steps need to be performed:

-   Set a static IP address on the desktop computer running uTorrent.
-   Ensure your firewall software on the desktop computer running uTorrent is configured to allow Web UI traffic through.

## Setting up a static IP address

> **Warning**
> 
> Running the uTorrent Web UI from a computer that is using a non-fixed
> Internet connection (e.g. 3G USB devices, Sierra Wireless, other
> mobile based Internet, etc)  **is not supported on a local network,
> nor is it supported over the Internet**. Normal WiFi (802.11) that
> connects back to a fixed (e.g. fiber, DSL or cable) Internet
> connection will work without any trouble. If you do not have a fixed
> Internet connection on the computer the uTorrent desktop program is
> running, you cannot use the Web UI, and thus you cannot use this 
> Torrent Remote app.


> **Warning**
> 
> Due to restrictions with the Windows Runtime and application
> sandboxing, you cannot use the  Torrent Remote app  to connect to the
> uTorrent desktop program on the same computer **without some extra
> steps**. We apologize for any inconvenience that this silly
> restriction by Microsoft may have caused. If you would like to try
> this anyway, you should see  [Workaround for connecting on the same
> computer](https://docs.scidoner.com/display/UCD/Workaround+for+connecting+on+the+same+computer).
> Note that this configuration is not officially supported.

**Please check the relevant section below for the version of Windows that your computer running uTorrent is using.**

> **Tip**
> 
> If you do choose to set up the app on the same computer (after heeding
> all of the above warnings), please note that you  **do not need to set
> up a static IP address.**  The IP address you need to use when adding
> a server connection to the  Torrent Remote app  is  **127.0.0.1** 
> which is the loopback address for the local computer. In this scenario
> you can skip to the firewall configuration section below.  **However,
> if you plan to access uTorrent from a different device in the future
> (in addition to on the same computer), you must still follow the
> static IP set up below.**

<details>
<summary><strong>For Windows 8 and Windows 7, Windows Server 2008 R2 and Windows Server 2012...</strong></summary>

1.  For Windows 7, Click **Start** and then  click **Control Panel**. For Windows 8, open the  **Settings Charm**  and then click  **Control Panel.**
2.  Ensure that the Control Panel view is set to either  **Large icons** or  **Small icons**  (and not set to  **Category**).
3.  Click to open the  **Networking and Sharing Center.**
4.  In the left pane, click on  **Change adapter settings.**
5.  For Windows 8, double click either  **WiFi** or  **Ethernet****.** For Windows 7, double click either  **Wireless Network Connection** or  **Local Area Connection.**
6.  In the status window that appears, click the  **Details...**  button.
7.  Note down the following properties from the details window:
    1.  IPv4 Address
    2.  IPv4 Subnet Mask
    3.  IPv4 Default Gateway
    4.  IPv4 DNS Server
8.  Click  **Close** to close the details window and then click  **Properties** in the status window behind it.
9.  In the properties window, under  **This connection uses the following items**, double click  **Internet Protocol Version 4 (TCP/IPv4).**
10.  In the properties window that opens, ensure that  **Use the following IP address** is selected and then follow the below:
    1.  From  **Step 7**  above, look at the value for the  **IPv4 Address**  (for example, we will use  **10.0.0.6**  here).
    2.  Modify the last digit in the IPv4 address to one of high range (but lower than 255). To continue the example we will use 100 so the resulting IPv4 address for our example will be  **10.0.0.100**.
    3.  Enter the value you created from Step B above into the field  **IP address**  (in our example this was  **10.0.0.100**, your value may differ).
    4.  In the field  **Subnet mask**, enter the value you recorded for  **IPv4 Subnet Mask** from  **Step 7**  above.
    5.  In the field  **Default gateway**, enter the value you recorded for  **IPv4 Default Gateway** from  **Step 7**  above.
11.  In the properties window, under **Use the following DNS server addresses**, enter the value you recorded for **IPv4 DNS Server** from  **Step 7**  above into the field **Preferred DNS server.**
12.  Click  **OK** twice to dismiss both properties windows and save your changes.
13.  Close  **Close** to close down the remaining status window.
</details>

<details>
<summary><strong>For Windows Vista and Windows Server 2008...</strong></summary>

1.  Click **Start**.
2.  On the right pane, right click the **Network** icon and then select **Properties** from the menu that appears.
3.  In the left pane, click on  **Manage network connections.**
4.  Double click either  **Wireless Network Connection** or  **Local Area Connection.**
5.  In the status window that appears, click the  **Details...**  button.
6.  Note down the following properties from the details window:
    1.  IPv4 Address
    2.  IPv4 Subnet Mask
    3.  IPv4 Default Gateway
    4.  IPv4 DNS Server
7.  Click  **Close** to close the details window and then click  **Properties** in the status window behind it.
8.  In the properties window, under  **This connection uses the following items**, double click  **Internet Protocol Version 4 (TCP/IPv4).**
9.  In the properties window that opens, ensure that  **Use the following IP address** is selected and then follow the below:
    1.  From **Step 6**  above, look at the value for the  **IPv4 Address**  (for example, we will use  **10.0.0.6**  here).
    2.  Modify the last digit in the IPv4 address to one of high range (but lower than 255). To continue the example we will use 100 so the resulting IPv4 address for our example will be  **10.0.0.100**.
    3.  Enter the value you created from Step B above into the field  **IP address**  (in our example this was  **10.0.0.100**, your value may differ).
    4.  In the field  **Subnet mask**, enter the value you recorded for  **IPv4 Subnet Mask** from  **Step 6**  above.
    5.  In the field  **Default gateway**, enter the value you recorded for  **IPv4 Default Gateway** from **Step 6**  above.
10.  In the properties window, under **Use the following DNS server addresses**, enter the value you recorded for **IPv4 DNS Server** from **Step 6**  above into the field **Preferred DNS server.**
11.  Click  **OK** twice to dismiss both properties windows and save your changes.
12.  Close  **Close** to close down the remaining status window.
</details>


<details>
<summary><strong>For Windows XP...</strong></summary>

1.  Click **Start** and then click **Run.**
2.  In the  **Open** box, type  **ncpa.cpl** and then click  **OK.**
3.  Double click either  **Wireless Network Connection** or  **Local Area Connection.**
4.  In the status window that appears, click on the  **Support** tab up the top and then click the  **Details...**  button.
5.  Note down the following properties from the details window:
    1.  IP Address
    2.  IP Subnet Mask
    3.  IP Default Gateway
    4.  First DNS Server
6.  Click  **Close** to close the details window and then click  **Properties** in the status window behind it.
7.  In the properties window, under  **This connection uses the following items**, double click  **Internet Protocol (TCP/IP).**
8.  In the properties window that opens, ensure that  **Use the following IP address** is selected and then follow the below:
    1.  From  **Step 5**  above, look at the value for the  **IP Address**  (for example, we will use  **10.0.0.6**  here).
    2.  Modify the last digit in the IPv4 address to one of high range (but lower than 255). To continue the example we will use 100 so the resulting IPv4 address for our example will be  **10.0.0.100**.
    3.  Enter the value you created from Step B above into the field  **IP address**  (in our example this was  **10.0.0.100**, your value may differ).
    4.  In the field  **Subnet mask**, enter the value you recorded for  **IP Subnet Mask** from **Step 5**  above.
    5.  In the field  **Default gateway**, enter the value you recorded for  **IP Default Gateway** from  **Step 5**  above.
9.  In the properties window, under **Use the following DNS server addresses**, enter the value you recorded for the  **First DNS Server** from  **Step 5**  above into the field **Preferred DNS server.**
10.  Click  **OK** twice to dismiss both properties windows and save your changes.
11.  Close  **Close** to close down the remaining status window.

## Configure firewall software
</details>

## Configure firewall software

> **Note**
> 
> If you are using a third party firewall software package on the
> computer running the uTorrent program, due to the large amount of
> possibilities, we cannot provide specific details. In this case you
> should consult the relevant material to help you through configuring
> your firewall package to allow uTorrent to communicate on the network
> and over the Internet.

### Windows Firewall configuration

Thankfully, if you are running Windows Firewall (i.e. you do not have a third party firewall software package installed), allowing the uTorrent program to communicate on the network and over the Internet is fairly simple. Follow the steps below to learn how to do this.

> **Tip**
> 
> If you know for sure that you have Windows Firewall disabled, you can
> skip this part and continue on to the  **Next step**  below.

This configuration is done from within the preferences of the uTorrent program itself.

1.  On the computer running the uTorrent desktop program, open its main window.
2.  From the menu bar at the top, click  **Options**  and then click  **Preferences**  from the drop down menu.
3.  In the  **Preferences** window, on the left select the **Connection** item.
4.  On the right, make sure a check is placed in the box labeled  **Add Windows Firewall exception**.
5.  Click  **OK** to save your changes.

The  **Add Windows Firewall exception**  option allows uTorrent to add an entry to the Windows Firewall exceptions list that lets it bypass the firewall. This is useful only if you actually have Windows Firewall enabled. This option works only on operating systems released after (and including) Windows XP with at least Service Pack 2 (SP2) installed.

## Next step

If all you want to do is access your uTorrent program on the  **same network**  (i.e. not over the Internet) you are done here!

The next step is to add a new server connection to the  Torrent Remote app  app, so you can connect to it. See  [Adding a connection to the uTorrent Client app](https://docs.scidoner.com/display/UCD/Adding+a+connection+to+the+uTorrent+Client+app).

Otherwise, the next step is to configure your devices for Internet access. See [Setting up for access over the Internet](https://docs.scidoner.com/display/UCD/Setting+up+for+access+over+the+Internet).

---
title: Workaround for connecting on the same computer
description: Torrent Remote Documentation
resource: true
categories: [torrent-remote]
---

{% include torrent-remote-header.md %}

Due to limitations put in place by Microsoft in the Windows Runtime, Windows Store apps by default are unable to connect to a local network service over IP. This is referred to as network isolation and you can view more information about it here:  [How to enable loopback and troubleshoot network isolation (Windows Store apps) (Windows)](http://msdn.microsoft.com/en-us/library/windows/apps/Hh780593.aspx) 

> **Warning**
> 
> Follow this information at your own risk. As this configuration is not
> supported by Microsoft and the Windows Runtime for production use, it
> is not supported officially by the  Torrent Remote app  either. There
> will be no support available for this configuration if you choose to
> use it. You are liable and one hundred percent responsible for any and
> all damages that may occur from following the below steps.  **By
> continuing to follow and execute the below steps on this page, you are
> implicitly assuming all responsibility and liability, as
> aforementioned.**

## Why do I need this information?

Although officially unsupported by the  Torrent Remote app, you need this information if you want to connect to the uTorrent desktop program that is running on the  **same**  computer that you have installed the  Torrent Remote app. This information will help you to configure your computer so that it can escape the network isolation restriction and communicate with the local uTorrent desktop program.

If you are receiving the error  **HRESULT 0x8007274C**  then this page applies to your situation.

> **Note**
> 
> This entire page does not apply if you are not trying to connect to
> the uTorrent desktop program on the same computer that you have
> installed the  Torrent Remote app.

## Removing the restriction

You can follow the below steps to remove the network isolation restriction for the  Torrent Remote app, which will allow you to connect to the uTorrent desktop program on the same computer. As already mentioned, this configuration is not support officially so, execute the below at your own risk.

1.  Open an elevated  **Command prompt** (Run as administrator).
2.  Copy and paste the below into the command prompt window and press  **Enter**.

    `CheckNetIsolation.exe LoopbackExempt -a -n=17540MichaelScidone.uTorrentClient_8wyshmwpt86bp`

4.  The command should display an  **"OK"**  result. Once this is done, exit the command prompt.

After following the above steps, try to launch the app and connect to the server again - you should be successful.

> **Note**
> 
> The above steps remove the restriction for the  Torrent Remote app
> **only.**  It does not affect other apps.

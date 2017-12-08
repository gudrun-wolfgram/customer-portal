---

copyright:

  years: 1994, 2017

lastupdated: "2017-12-05"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Rebooting your server
{: #customerportal_rebootserver}

Sometimes, events occur in {{site.data.keyword.BluSoftlayer_notm}} infrastructure that require you to reboot your server.
{:shortdesc}

Use the following steps to reboot your server:
1. From the customer portal, click the **Support** tab.
2. Click **Reboot**.
3. Select the server to reboot, and click **Reboot**.
4. Select one of the following methods to reboot the server:
  * Default (attempt the reboot with IPMI and then with the power strip)
  * IPMI
  * Power strip
5. Click reboot.

This page also offers the ability to boot into the rescue kernel, which is very helpful if you are experiencing an issue in which the server cannot boot to the OS because of a configuration issue. After booting to the rescue kernel, you can mount the drive, or drives, of your server and then fix the configuration issue. After the issue has been fixed, you can reboot the server from the command line and the server will reboot into the default kernel for your server. After you have issued the reboot command, you will see an estimated time of completion.

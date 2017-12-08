---

copyright:

  years: 1994, 2017

lastupdated: "2017-12-04"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}


# Protecting your systems
{: #customerportal_protsys}

Protecting your systems ensures that your systems are running smoothly and without unnecessary interruptions.

## Use the private network
{: #cp_bpuseprivnet}

You can manage your devices in the most secure environment possible using the  {{site.data.keyword.BluSoftlayer_notm}} infrastructure private network. When possible, interact with your devices using a VPN connection and enable network spanning so that your systems communicate over the private network. To access the private network, edit the user’s VPN access from the [User List ![External link icon](../icons/launch-glyph.svg)](https://control.softlayer.com/account/user/list){:new_window}. Use the [Virtual Private Network ![External link icon](../icons/launch-glyph.svg)](http://www.softlayer.com/vpn-access){:new_window} instructions to connect to one of the various VPN options.

### Don't leave RDP, SSH, or control ports on the public network
{: #cp_bpnordpsshcponpubnet}

The public network is great for many things, but there are certain aspects that, when left available on the public network through open ports, can leave your system vulnerable. Protect yourself by disabling RDP or restricting SSH on the public network. If these services must be available on the public network, consider moving RDP or SSH to a custom port number.

## Safeguard your data through regular backups
{: #cp_bpsafedataregback}

{{site.data.keyword.BluSoftlayer_notm}} infrastructure offers multiple backup solutions to ensure that you can retrieve your data in the event of drive failure or user error. Backup solutions currently include NAS, EVault Backup and R1Soft CDP, which are all available in a variety of storage options. Check out the [Storage ![External link icon](../icons/launch-glyph.svg)](http://www.softlayer.com/services/storagelayer/){:new_window} page for more information on each backup solution.

### Don't assume you have redundancy; know that you do
{: #cp_bpknowredundant}

{{site.data.keyword.BluSoftlayer_notm}} infrastructure offers multiple add-on redundancies, including dual-path, redundant power supplies, and RAID configurations. Verify that you have provisioned one or more of these features to ensure you are working in a redundant environment and are protected in the event of a failure.

### Confirm that your information is backed before performing an OS reload
{: #cp_bpnoperfOSwobackupconf}

Reloading your operating system removes all data from the hard drive of the device. Prior to initiating the OS reload, back up your information and verify the success of that backup so no information is lost. After an OS reload has been completed, lost information cannot be retrieved.

## Don’t remove Adaptec Storage Manager (ASM)
{: #cp_bpsupdontremovasm}

 {{site.data.keyword.BluSoftlayer_notm}} infrastructure uses ASM to monitor your RAID array status. If you delete this software, the support team cannot monitor your device. If ASM is removed from your device, RAID failure alerts on your device are not available and you are not notified of the failure through the automatic notification system.

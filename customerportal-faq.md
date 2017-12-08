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


# FAQs
{: #bicpfaq}

The following frequently asked questions relate to managing infrastructure resources issues.
{:shortdesc}


## How do I retrieve my credentials for the Customer Portal?
{: #bicp_retcreds}

If you use IBMid for authentication, when you place your first order or when you are added as a user to an account, an email is sent that has a link to get you started with your IBMid. If your user name or password is lost or forgotten, go to your [IBMid profile ![External link icon](../icons/launch-glyph.svg)](https://www.ibm.com/account/profile){:new_window} and reset or recover the password using the instructions that follow the sign in process. You will be prompted to enter specific information, which might include providing answers to your security questions.

If you do NOT use IBMid for authentication, when you place your first order or you are added as a user to a [customer portal ![External link icon](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window} account, you receive an email that contains your user name and initial password to get started in the customer portal. Be sure to change your password after you log in for the first time by [editing your user profile](edit-user-profile.html).

If you forget your password after you log in, use the **Forgot Password** feature that is available on the login screen of the [customer portal ![External link icon](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window}. You will be prompted to enter specific information, including a set of security questions you specified while [editing your user profile](edit-user-profile.html).

If you forget your user name, contact your account administrator or master user, who has the ability to retrieve your user name. If you are the administrator or master user on the account, [contact Support](support.html) for additional assistance.


## What is the IBMid, and how does it relate to {{site.data.keyword.BluSoftlayer_notm}} Infrastructure users?
{: #bicp_whatisibmid}

New accounts require IBMid for authentication. Existing accounts continue to use the SoftLayer user name and password for authentication until you run the migration tool to switch to an IBMid. Your SoftLayer account has a master user who then has authority to add more users within that same account. See [How SoftLayer accounts are managed in customer portal](/docs/customer-portal/cphowacctsman.html) for more information.

## How do I link an existing SoftLayer account?
{: #bicp_linkbmxacct}

If you are the master user on your SoftLayer account, login to the customer portal and click **Link an account** in the header.  See [Linking IBMid user accounts](/docs/admin/softlayerlink.html#link_user_accounts) for more information.

## Do I have to be an existing {{site.data.keyword.Bluemix_notm}} user to link accounts?
{: #bicp_bmxusertolink}

No. You can create a new {{site.data.keyword.Bluemix_notm}} account or link an existing {{site.data.keyword.Bluemix_notm}} trial or pay-as-you-go account.


## How will my two-factor authentication work?
{: #bicp_2fa}

There is no impact to two-factor authentication configuration at the account level. Two-factor authentication is not per IBMid; it is still per account. When an IBMid is associated with many accounts, and you switch between accounts, you must confirm your identity every time you switch into a different account that requires two-factor authentication. This is true even if the prior account and the new account were both configured with the same 2FA mechanism.

For more information about IBMid with two-factor authentication, see [Two-factor authentication usage in linked accounts](/docs/admin/softlayerlink.html#2fa).


## Who can link accounts?
{: #bicp_wholinkaccts}

Only {{site.data.keyword.BluSoftlayer_notm}} infrastructure master users can link SoftLayer and {{site.data.keyword.Bluemix_notm}} accounts. A master user's email must also be associated to the primary owner of the {{site.data.keyword.Bluemix_notm}} account being linked.


## What will I use to login to each portal?
{: #bicp_logineachport}

Your account billing is linked and you can easily move between your SoftLayer and {{site.data.keyword.Bluemix_notm}} accounts, but your account identities remain separate.

* If your account does not use IBMid for authentication, continue to use your SoftLayer ID for SoftLayer products and services, and use your IBMid for {{site.data.keyword.Bluemix_notm}} products and services.

* If your account uses IBMid for authentication, you use your IBMid to access both your SoftLayer and your {{site.data.keyword.Bluemix_notm}} accounts.


## I tried to log in with my SoftLayer user name, why am I getting an error?
{: #bicp_SLloginerror}

After you switch to an IBMid, if you log into the customer portal with your {{site.data.keyword.BluSoftlayer_notm}} infrastructure user name you will see the error *"Invalid login credentials provided"*.
This is because, after you switch to an IBMid, you can no longer log into the customer portal with your {{site.data.keyword.BluSoftlayer_notm}} infrastructure user name. You must click **Login with IBMid** in the Account Login dialog.

## I tried to sign in with my IBMid, why am I getting an error?
{: #bicp_IBMidloginerror}

When signing in with your IBMid, if you get the error *"We didn't recognize this IBMid or email"*, make sure that you are entering a fully qualified email address. Also make sure that you are not using your {{site.data.keyword.BluSoftlayer_notm}} infrastructure user name.


##  I have a new SoftLayer account that uses IBMid for authentication; can I use the same ID for both {{site.data.keyword.BluSoftlayer_notm}} infrastructure and {{site.data.keyword.Bluemix_notm}}?
{: #bicp_loginIBMidSLBlusame}

Yes, you can use your same IBMid to log into {{site.data.keyword.BluSoftlayer_notm}} infrastructure and {{site.data.keyword.Bluemix_notm}}.


## I linked an {{site.data.keyword.Bluemix_notm}} account, how do I give my other {{site.data.keyword.BluSoftlayer_notm}} infrastructure team members access?
{: #bicp_linkgiveteamaccess}

You must invite them to {{site.data.keyword.Bluemix_notm}}. In the {{site.data.keyword.Bluemix_notm}} user interface, select **Account and Support** > **Account** > **Invite Team Members**. After you've selected a resource group, you'll see an option to add {{site.data.keyword.BluSoftlayer_notm}} infrastructure team members. You might have to log into {{site.data.keyword.BluSoftlayer_notm}} infrastructure before you can send invitations. {{site.data.keyword.Bluemix_notm}} gets the list of {{site.data.keyword.BluSoftlayer_notm}} infrastructure users, and then you can select which users to invite to the {{site.data.keyword.Bluemix_notm}} account.


## Where's my email to complete the switch to IBMid?
{: #bicp_ibmidswitchemail}

If you followed the wizard to switch to IBMid and haven't received the email, it can take from minutes to hours for the email with your registration code to be sent. You can go back to the **Edit User Profile** page in the customer portal and click **Resend Email** to try again.


## Will I have full, root access to my account?
{: #bicp_fullrootaccaccess}

Master users, and those with administrator permissions, have full root access to accounts on the customer portal and API. Users without administrator permissions have accessibility controlled by those with admin roles. These permissions can be updated at any time by [editing the user profile](edit-user-profile.html) in the customer portal.


## Can I link an {{site.data.keyword.Bluemix_notm}} subscription account?
{: #bicp_linkbmxsubacct}

All linked accounts in {{site.data.keyword.Bluemix_notm}} must be pay-as-you-go accounts. You can create a new pay-as-you-go account or link an existing pay-as-you-go account. Or, you can link an existing trial account, but it will be upgraded to a pay-as-you-go account.


## How do I unlink my {{site.data.keyword.Bluemix_notm}} account with my {{site.data.keyword.BluSoftlayer_notm}} infrastructure account?
{: #bicp_unlinkacct}

After accounts are linked, they cannot be unlinked.


## What is my company profile and where can I find it?
{: #bicp_whatfindcompprof}

The company profile was the information submitted at the time the account was created and includes a primary contact for your company, along with the company name, address and phone number. This information is used for a variety of reasons and should be kept current at all times. To view the company profile for your account or to request changes, see [Updating your company profile](/docs/customer-portal/cpmanacctcompprof.html#customerportal_reqcompprofch).

## Where do I find my device and software passwords?
{: #bicp_devswpw}

Device and software passwords are stored in two locations within the [customer portal ![External link icon](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window}. To retrieve device credentials, including the root or admin user name and password for both {{site.data.keyword.baremetal_short}} and {{site.data.keyword.virtualmachinesshort}}, see [Interact with a Device in the Snapshot View](/docs/vsi/vsi_interact_device_snapshot_view.html). To quickly view and retrieve software credentials that are manually tracked using the customer portal, see [Managing device access](/docs/vsi_device_access.html).

##How do I keep my web data in sync?
{: #bicp_webdatasync}

Though you are responsible for maintaining data consistence between real servers, {{site.data.keyword.BluSoftlayer_full}} provides a private network that you can use to synchronize without incurring usage charges.


## What is the Event Management System?
{: #bicp_whatisems}

The Event Management System is a toolset that optimizes the way {{site.data.keyword.BluSoftlayer_full}} shares information with users about unplanned infrastructure issues and upcoming planned maintenance events. It utilizes targeted, subscription-based email alerts for these incidents to share the type of event that has occurred. It provides subscribed users with additional details about the overall impact of the event and a current status of the unplanned incident in progress (UIP).

## How and where can I cancel a device?
{: #bicp_candev}

You can cancel a device at any time through the [customer portal ![External link icon](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window}. See [Cancel a Device](/vsi/vsi_managing.html) for more information about completing a cancellation request.

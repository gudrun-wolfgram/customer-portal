---

copyright:

  years: 1994, 2017

lastupdated: "2017-12-01"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}



# Monitoring {{site.data.keyword.Bluemix_notm}} infrastructure system events
{: #customerportal_monevent}

You can monitor system events to keep your systems running smoothly.  For information about setting up and managing virtual servers in {{site.data.keyword.BluSoftlayer_full}} infrastructure, see [Getting started with virtual servers](/docs/vsi/vsi_index.html#getting-started-with-virtual-servers).
{:shortdesc}

## Viewing an audit log for an account
{: #cp_viewacctauditlog}

Each customer portal account comes with an audit log that tracks the interactions of each user within the customer portal. Tracked interactions include login attempts (success and failures), port speed updates, power on or off and reboots, and those interactions made by {{site.data.keyword.BluSoftlayer_notm}} infrastructure support staff. Use the following steps to view an audit log for a user account.

1. Access the [Customer Portal ![External link icon](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window} using your unique credentials.
2. Select **Account** > **Manage** > **Audit Log** from the navigation bar to access the audit log.

The audit log initially displays the last 25 interactions taken by users on the account. You can view up to 200 interactions at any time. Update the number of results shown from the **Display** drop down list. If settings were changed, the **Action** column for the interaction will contain a link. Click any link to view the setting impacted by the action and details on the change. Clicking the device name or username for any interaction redirects you to either the device details screen or user profile screen, respectively.

## Viewing a user's access logs
{: #cp_viewuserlogs}

Access Logs display data for each access attempt made by a specific customer portal user. The logs display a date and time stamp and IP address for each access attempt. Use the following steps to view a user's Access Logs.

1. Access the [customer portal ![External link icon](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window} using your unique credentials.
2. Select **Account** > **Users** from the menu bar to access the Users window.
3. From **Actions** drop down list, select **View Audit Log** to view the user's access log.

The access log for each user displays the access attempts made by that user by date, along with the IP address from which the access attempt was made. Information within the access log is read-only, so edits to the content cannot be made at any time. You can view the access logs again at any time by repeating the previous steps. To exit the logs and return to the Users screen, click the **View All Users** link at the top of the screen.

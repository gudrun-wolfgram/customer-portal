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


# Monitoring your environment and system events
{: #customerportal_cpmonenvsysevent}

Monitoring your environment means you have the ability to check on devices at any time and you are automatically notified if one of your devices goes down. You can also monitor system events to keep your systems running smoothly.  
{: shortdesc}

## Monitoring your environment
{: #cpmonenv}

At a minimum, use basic ping monitoring but you can customize your monitoring options in a way that best suits your business needs.

### Staying informed of network maintenance and unplanned events
{: #cp_stayinfomaintevent}

From time to time, scheduled and emergency network maintenance is unavoidable. {{site.data.keyword.BluSoftlayer_full}} infrastructure maintains many channels, such as [Twitter account ![External link icon](../icons/launch-glyph.svg)](https://twitter.com/softlayernotify){:new_window}, to keep you informed of all scheduled and emergency maintenance events. Additionally, you can [subscribe to email notifications](/docs/customer-portal/cpsub2not.html){:new_window} from the Event Management System. This complimentary service automatically emails subscribed users regarding unplanned events which might impact services.

### Using {{site.data.keyword.BluSoftlayer_notm}} infrastructure mobile
{: #cp_bmxinframobile}

Use [{{site.data.keyword.BluSoftlayer_notm}} infrastructure mobile ![External link icon](../icons/launch-glyph.svg)](https://knowledgelayer.softlayer.com/topic/mobile-devices){:new_window} to manage your {{site.data.keyword.BluSoftlayer_notm}} infrastructure devices on the go using your iOS or Android mobile device. Functionality within {{site.data.keyword.BluSoftlayer_notm}} infrastructure mobile includes ticketing support, basic device control, and bandwidth monitoring.

## Monitoring system events
{: #customerportal_monevent}

You can monitor system events by viewing audit logs and access logs.

### Viewing an audit log for an account
{: #cp_viewacctauditlog}

Each customer portal account comes with an audit log that tracks the interactions of each user within the customer portal. Tracked interactions include login attempts (success and failures), port speed updates, power on or off and reboots, and those interactions made by {{site.data.keyword.BluSoftlayer_notm}} infrastructure support staff. Use the following steps to view an audit log for a user account.

1. Access the [Customer Portal ![External link icon](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window} using your unique credentials.
2. Select **Account** > **Manage** > **Audit Log** from the navigation bar to access the audit log.

The audit log initially displays the last 25 interactions taken by users on the account. You can view up to 200 interactions at any time. Update the number of results shown from the **Display** drop down list. If settings were changed, the **Action** column for the interaction will contain a link. Click any link to view the setting impacted by the action and details on the change. Clicking the device name or username for any interaction redirects you to either the device details screen or user profile screen, respectively.

### Viewing a user's access logs
{: #cp_viewuserlogs}

Access Logs display data for each access attempt made by a specific customer portal user. The logs display a date and time stamp and IP address for each access attempt. Use the following steps to view a user's Access Logs.

1. Access the [customer portal ![External link icon](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window} using your unique credentials.
2. Select **Account** > **Users** from the menu bar to access the Users window.
3. From **Actions** drop down list, select **View Audit Log** to view the user's access log.

The access log for each user displays the access attempts made by that user by date, along with the IP address from which the access attempt was made. Information within the access log is read-only, so edits to the content cannot be made at any time. You can view the access logs again at any time by repeating the previous steps. To exit the logs and return to the Users screen, click the **View All Users** link at the top of the screen.

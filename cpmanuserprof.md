---

copyright:

  years: 1994, 2017

lastupdated: "2017-12-06"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}


# Managing a user profile
{: #customerportal_accuserprof}

In the customer portal, a user profile contains a variety of data about the user, including contact information and the API key. It is also the location in which passwords are stored. Additionally, if you have administrative access, you can change permissions and device access from the profile.
{:shortdesc}

Within the user profile, you can manage contact information and passwords, view API keys, and update additional permissions and device access (based on your permissions).

## Editing a user profile
{: #cp_edituserprofile}

After a user profile has been created in the customer portal, you can edit it at any time. Details associated with the user profile include personal information, login settings, API access details, user notification subscriptions, and security questions. Use the following steps to edit a user profile.

1. Access the customer portal using your unique credentials.
2. Select **Account > Users** from the navigation bar.
3. Click the user name to access the associated user profile for that user.
4. Edit the **User Profile** details as necessary. For users in accounts that use IBMid for authentication, update your email and password in your IBMid profile. See Table 1 for more information.
5. If you want to reset your password after you log in, click **Reset Password** to generate a new email allowing you to change your password.
6. Click **Edit User** to submit the changes.

<table border="1"><caption align="bottom">Table 1. Configuration settings for editing a user profile</caption><tr><th>Section</th><th>Field</th><th>Definition</th></tr><tr><td rowspan="5">Personal Information</td><td>First Name, Last Name</td><td>First and last name of the user associated with the user profile.</td></tr><tr><td>Email Address</td><td>Preferred email address to receive notifications from {{site.data.keyword.BluSoftlayer_notm}} infrastructure regarding the account. Changing the email address changes only the record in {{site.data.keyword.BluSoftlayer_notm}} infrastructure. This change does not affect the linkage to the IBMid authentication credentials. You must change the email address for the IBMid from the IBMid profile.</td></tr><tr><td>Time Zone</td><td>Preferred time zone to use when displaying time-stamped data.</td></tr><tr><td>Phone, Alt Phone</td><td>Preferred contact phone numbers to be used by {{site.data.keyword.BluSoftlayer_notm}} infrastructure.</td></tr><tr><td>Street Address, City, Country, State/Province, ZIP/Postal Code</td><td>Full address for contact to be used by {{site.data.keyword.BluSoftlayer_notm}} infrastructure.</td></tr><tr><td rowspan="5">Log In Settings</td><td>Restrict Access to IP</td><td>IP address to restrict access to when attempting to use the customer portal under the associated user profile.</td></tr><tr><td>Expire Password In (only for users in accounts that do NOT use IBMid for authentication)</td><td>Amount of time in which a password should be associated with the user profile before a new password must be selected.</td></tr><tr><td>Parent User</td><td>User account that is considered the parent user of the user profile. The parent user default is the primary account ID.</td></tr><tr><td>Require Security Questions?</td><td>Select this check box when security questions should be required during login. If this box is selected, security questions are required for the user profile.</td></tr><tr><td>VPN Password</td><td>Password to be used for VPN access. Click the **Use Portal Password for VPN** check box to use the customer portal password to access {{site.data.keyword.BluSoftlayer_notm}} infrastructure network through VPN.</td></tr><tr><td>API Access Information</td><td>Allowed IPs</td><td>IP addresses permitted to authenticate to the API using the unique API key associated with the user profile</td></tr><tr><td>User Notification Subscriptions</td><td>Billing</td><td>Select the **Billing** check box to receive an email invoice after it has been created.</td></tr><tr><td rowspan="2">Security Questions</td><td>Security Question</td><td>When editing your profile, this is the question that you must answer to login when security questions have been activated for your profile.</td></tr><tr><td>Answer</td><td>Case sensitive answer to the applicable security question.</td></tr></table>

After submitting edits to a user profile, the changes are applied immediately. You can change the user profile again at any time by repeating the previous steps.  

See [Switching to IBMid](/docs/admin/softlayerlink.html#switching-to-ibmid) for more information about setting up an IBMid account.

## Editing a user's customer portal permissions
{: #cp_editusercpperm}

User permissions in the customer portal are set by the account administrator when the user is added and can be edited at any time by an authorized user. You can edit your own user profile and, if you are an administrative user, some fields of the user profiles for users that you added. Permissions are divided into five tabs: support, devices, network, services, and account. You can update the permissions for one user at a time and you must save your changes for them to become active.

Use the following steps to edit a user's customer portal permissions.

1. Access the customer portal using your unique credentials.
2. Select **Account > Users** from the navigation bar.
3. Click the user name of the user to access the user profile.
4. Click the **Permissions** icon to access the Permissions window.

  You might get a message indicating that changes haven't been saved to the user profile. If no changes have been made to the profile, click through to discard changes and access the Permissions window.
  {: tip}
  
5. Select the permissions:
  * To set quick permissions, select the permission set from the **Quick Permissions** list. After you select a permission set, each permission associated with the set is displayed in orange text with an orange arrow pointing to the check box. Then click **Set Permissions** for each tab.
  * To set individual permissions, select or deselect each check box on the tabs to update the user's permissions. Click **Select All Permissions** or **Deselect All Permissions** on any tab to select or deselect all permissions at once.
6. Click **Edit Portal Permissions** to submit changes and update the user's permissions.
7. To reset the user's permissions to the original settings instead of saving them, click **Reset Permissions**. Click **Cancel** to cancel the changes and return to the Users window.

User permissions are updated immediately after you submit the changes. If permissions have been granted, the user can view or interact with the selected features. If permissions have been removed, the user can no longer view or interact with the selected features. Permissions can be updated again at any time by repeating the previous steps.

## Adding external authentication for a user
{: #cp_addextauthuser}

From the customer portal, you can activate external, two-factor authentication to add additional protection when logging in to the portal. This additional layer of security protects the account from unverified access, ensuring devices, data, and account information are protected. This external authentication is available in the following forms:

* **Symantec Identify Protection** is the most commonly used external authentication tool, providing a dynamic security code used in addition to the username and password when accessing the customer portal.
* **PhoneFactor** authentication provides out-of-band user authentication from a phone, SMS, or mobile app. PhoneFactor requires a valid phone number that you must have access to any time you attempt to authenticate.

You can add both methods of external authentication, per user, for a [small monthly fee ![External link icon](../icons/launch-glyph.svg)](http://www.softlayer.com/services/security/){:new_window}. Use the following steps to add external authentication for a customer portal user.

1. Access the customer portal using your unique credentials.
2. Select **Account > Users** from the navigation bar.
3. Select **Add External Authentication** from the **Actions** list for the user.
4. Select the type of external authentication to order:
  * **Symantec Identity Protection** -- Enter the user's credential ID in the **Credential ID** field.
  * **PhoneFactor** -- Choose an [authentication method](#cp_phonefacauthmeths).
5. Click **Continue**.
6. Complete the prompts on the window for **Promo Code** and **MSA Acknowledgement**.
7. Click **Order External Authentication** to complete the order.

After you add the external authentication for a user, the next steps depend on the authentication type.
* If Symantec Identity Protection is enabled, you must add the security code associated with the user's Credential ID that was entered in the system at the time the Symantec Identity Protection was added to the account.
* If PhoneFactor is enabled, the user must [activate PhoneFactor](#cp_actphonefacauth) to use this type of two-factor authentication with the account.

### Activating PhoneFactor authentication
{: #cp_actphonefacauth}

After you add PhoneFactor, you must manually activate external authentication with PhoneFactor through the customer portal. Because PhoneFactor utilizes manual contact, it is important to ensure that all phone numbers associated with the account are up to date at all times. Failure to keep contact information updated could result in being unable to access the customer portal and VPN when PhoneFactor is active. When PhoneFactor has been successfully added, you will receive an email to confirm that PhoneFactor has been added. After you receive the email, use the following steps to activate PhoneFactor authentication.

1. Access the customer portal using your unique credentials.
2. Select **Account > Users** from the navigation bar.
3. Click the user name to access the associated user profile for that user.
4. Scroll to the **PhoneFactor Settings** section.

  If the PhoneFactor Settings section is not available, first verify that you received the PhoneFactor provisioning email indicating that PhoneFactor has been provisioned. If PhoneFactor has been provisioned and the section is not available, create a support ticket. If PhoneFactor has not yet been provisioned, wait for the email and try again. If PhoneFactor has not yet been added, see [adding external authentication for a user](/docs/customer-portal/cpmanuserprof.html#cp_addextauthuser).
  {: tip}
  
5. Select **Active** from the **Status** list.
6. Edit the **Primary Phone Number** for authentication.
  1. Click the **Edit** link.
  2. Enter the **Country Code**, **Phone Number** and **Extension**, if applicable, in the associated fields.
  3. Click **Authenticate and Save Number** to complete authentication.
  
    When adding a phone number for authentication, you must be by the phone. After you click **Authenticate**, the number is called and you are prompted to complete a step to authenticate the number. Phone numbers cannot be authenticated without completion of these steps.
    {: tip}
    
  4. To add a **Secondary Phone Number**, repeat these steps.
7. Select the **Contact Method** from the **Method** list.
8. Select a **PIN type** from the **PIN Type** list.
9. If you select **One Time** > **PIN Value**, enter the PIN in the **PIN Value** field.
10. Click **Update** to update the changes and activate PhoneFactor authentication.

After activating PhoneFactor, authentication through PhoneFactor is required by the customer portal or VPN. After authenticating with the user credentials, a message tells you that PhoneFactor authentication is being attempted. You, or the user you are adding, must be near the phone listed with PhoneFactor in order to complete authentication. PhoneFactor attempts to authenticate five times. After five unsuccessful authentication attempts, you are locked out for approximately one hour. You, or a user with administrative access to the account, can change the PhoneFactor authentication settings at any time.  You, or an administrator of the account, can deactivate PhoneFactor at any time.

#### PhoneFactor authentication methods
{: #cp_phonefacauthmeths}

If you set up PhoneFactor as the authentication type, you can to choose one of the following options as an authentication method:
<dl>
<dt>Phone call and standard (no pin)</dt>
<dd>With this option enabled, when you log into the portal, you receive a phone call to the primary number enabled. When you answer the call, you are told to press the # key to complete authentication.</dd>
<dt>Phone call with pin</dt>
<dd>With this option selected, you enter a pin value in the customer portal. The pin must be between 4 to 8 numbers. When you try to log into the portal, you receive a call to the primary number listed in the portal. When you answer, you are told to enter your pin number followed by the # to complete the authentication.</dd>
<dt>SMS text and one-time pin</dt>
<dd>With this option selected, you receive a text message with a pin that you use to reply back to the message. When you enter the pin provided, the authentication process completes and logs you into the portal.</dd>
<dt>SMS text with one-time & pin value</dt>
<dd>With this option selected, you create a pin value of 4 to 8 numbers. You then receive a text message, and you reply back with the provided code and your pin number without spaces.</dd>
<dt>PhoneFactor app and standard (no pin)</dt>
<dd>Open the PhoneFactor application (Azure Authenticator) on your device and click  <strong>Authenticate</strong>. It will show that you have successfully authenticated using PhoneFactor and log you into the portal.</dd>
<dt>PhoneFactor app with pin</dt>
<dd>With this option, you set a pin, between 4 to 8 numbers, in the portal. You then bring up the PhoneFactor application (Azure Authenticator) on your device. Next, enter your pin that was created in the portal and click <strong>Authenticate</strong> to log into the portal.</dd>
</dl>

## Changing a user's status
{: #cp_changeuserstat}

Your status in the customer portal determines your accessibility to the customer portal. Status categories that you can update on the account include Active, Disabled, and VPN Only. Your status might be changed for a variety of reasons and the status can be updated at any time. Customer status categories include those that users can update and those that are updated automatically. They include:
<dl>
<dt>Active</dt>
<dd>The user has full access to the customer portal and VPN based on permissions that are set by the account administrator. This status might be manually selected or changed at any time.</dd>
<dt>Disabled</dt>
<dd>The user does not have access to any permissions or subscriptions on the account, including customer portal and VPN. If the status category is set to disabled by another user on the account, this status can be manually selected or changed at any time.</dd>
<dt>VPN Only</dt>
<dd>The user has full access to VPN connectivity, based on his or her permission set, but cannot access the customer portal. This status can be manually selected or changed at any time.</dd>
<dt>Inactive</dt>
<dd>The user has not accessed the customer portal or VPN in the last 60 days. This is a system-generated status.</dd>
<dt>cancel_pending</dt>
<dd>An administrator on the account has canceled this user and the cancellation is currently being processed. This is a system-generated status.</dd>
</dl>

Use the following steps to change a user's status in the customer portal.

1. Access the customer portal using your unique credentials.
2. Select **Account** > **Users** from the navigation bar.
3. Select **Change User Status** from the **Actions** list.
4. From **Status** list, select the appropriate status according to the definitions in the previous list.
5. Click **Save**.

After you update a user's status, changes to customer portal accessibility align with the new status.

## Editing a user's VPN access
{: #cp_edituservpnaccess}

When a [new user is added](/docs/customer-portal/cpmanacctadduser.html#customerportal_addusertocpacct) to a customer portal account, VPN access is selected from a variety of connection methods, including SSL, PPTP, or a combination of the two. With VPN access, the private network can be accessed in its entirety or network access can be limited to one or more specific subnets. You can manage and update VPN access at any time from the Users window. Use the following steps to edit a user's VPN access.

1. Access the customer portal using your unique credentials.
2. Select **Account > Users** from the navigation bar.
3. Click the **current VPN access type** link in the **VPN Access** column to display the VPN Access window.
4. Select a **VPN method** from the **VPN Type** list.
5. Indicate how the **Subnet Access** should be managed:
  * Select **Auto** to automatically manage subnet access
  * Select **Manual** to manually manage subnet access and then select the **Grant Access** check box for each subnet to which the user should have access. Be sure to clear any check boxes that the user should not have access to.
6. Click **Save**.

After updating a user's VPN access, their permissions are updated accordingly and the VPN Access column displays the updated VPN access method, if applicable.

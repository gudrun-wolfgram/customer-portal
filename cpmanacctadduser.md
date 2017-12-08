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


# Adding users to a SoftLayer account
{: #customerportal_addusertocpacct}

One or more users can interact with the products and services associated with an account. If you are the master user, you can add users at any time.
{:shortdesc}

If you are managing {{site.data.keyword.BluSoftlayer_full}} infrastructure users, which SoftLayer accounts you can manage depends on the access that is assigned to your user account and how your account is set up. If you are the master user, or have administrative access as an account owner, you can manage other customer portal users. If your account is not set up as a master user, you can manage your user profile.

Depending on your access, you can manage either your SoftLayer account or the accounts of other users from the Users window. The Users window in the [customer portal ![External link icon](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window} displays users associated with an account. Interactions available on the Users window vary based on your unique account permission set.
  * If you are the master user of the account, you can see all users associated with the account.

  If you must share the master login credentials for your account, share the credentials carefully. Your master login controls every aspect of your account and should be protected. To enable other users to use the customer portal, you set up individual or permission-based users. This allows you to have the most control over who is able to interact with certain aspects of your account.
  {:tip}
  * If you have administrative access, you can see all of the users you’ve created and, if you gave those users permission to administer other users, you can also see any users they’ve created. You can also take actions on any user associated with the account, including editing access to the customer portal, changing user status, and removing users.
  * If you are not the master user of the account and you do not have administrative access, only your profile is shown.  You can interact with your own account, including viewing the API key, editing VPN access, and adding external authentication.

To manage users from the {{site.data.keyword.Bluemix_notm}} console, see [Managing your account](/docs/admin/adminpublic.html#signing-up-for-ibm-cloud) and [Managing identity and access](/docs/iam/quickstart.html#getstarted). See [How the {{site.data.keyword.Bluemix_notm}} console works](/docs/overview/ui.html#ui) for more information about the {{site.data.keyword.Bluemix_notm}} console.

Different people within an organization have different roles and responsibilities, and user permission sets are not one–size-fits-all. Therefore, you can add users to the customer portal with roles to ensure that each person or group only has access to what they should. If changes are made in error or were unauthorized, you can trace them back to the user or group to ensure that you can provide proper training or update user permissions. This minimizes risk in a variety of ways and allows users to focus on their specified role within the customer portal.

Use the following steps to add a user to an account.

1. Access the customer portal using your unique credentials.
2. Select **Account > Users** from the navigation bar.
3. Click **Add User**.
4. Complete the required fields in the **Personal Information** section, including the status, a user name, and the email address for customer portal communication and notifications, including the initial notification to set up a password for the account.

  Optionally, instead of entering an address for the user, you can click the **Use Default Company Information** check box to populate the company address.
  {: tip}

5. Complete the required fields in the **Log In Settings** section, including if the settings can be edited by the user, whether the IP address is restricted, and whether or not the user is required to set up and use security questions. Also, for any users that aren't using IBMid, you can set the length of time before the password expires.
**Notes:**
* If you use IBMid for authentication, update passwords in your [IBMid profiles ![External link icon](../icons/launch-glyph.svg)](https://www.ibm.com/account/profile){:new_window} by following the instructions under **Sign In**.
* Click the **User Portal Password for VPN** check box to sync the customer portal and VPN passwords.
6. Click **Add User**.

After you create an account for a user, the user receives an email notification to finish setting up their account by setting a password and, optionally, security questions if you indicated that they are required.

How users without the administrative access of a master user log into the customer portal depends on the master user who provided the user access in their SoftLayer accounts:
  * If the master user has an IBMid to authenticate, each user that the master user creates has an IBMid.
  * If the master user has an {{site.data.keyword.BluSoftlayer_notm}} Infrastructure ID to authenticate, each user that the master user creates has an {{site.data.keyword.BluSoftlayer_notm}} Infrastructure user name. The master user and each user that the master user creates must run the migration tool to switch to an IBMid.
  * If neither of these cases apply, in the case of IBM business partners for example, contact Support to determine which user ID to use.

## Setting user permissions on the account
{: #cp_setuserpermsacct}

Use the following steps to set the permissions for the user you just added.

1. Click the **Permissions** icon, indicated by a user figure with a lock.
2. Update the **User Permissions** on all tabs for the new user.
> **Note:** Select an option from the **Quick Permissions** list to view recommended permission sets for three types of users. Click **Set Permissions** to select the recommended permissions set, or customize the user's accessibility by selecting individual options on each tab available.
3. Click **Add Portal Permissions** to add the permissions or click **Reset Permissions** to reset permissions for the user.
4. Click the **Device Access** icon, indicated by three servers.
5. Click the device check box for each device you want the user to be able to access.
6. Click **Update Device Access** after you select the devices.

You will receive an email with links and information to guide you through setting up an IBMid for authentication into this account. The steps can include creating a new IBMid if the account is using IBMid for authentication. The invitation expires in 7 days, but you can contact your administrator to resend the invitation.

For all other authentication cases, after adding the new user, the user can log in to the customer portal at any time to work with various products and services associated with the account. You can deactivate the user at any time.

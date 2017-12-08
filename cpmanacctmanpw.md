---

copyright:

  years: 1994, 2017

lastupdated: "2017-12-07"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}


# Managing passwords
{: #customerportal_manpws}

If you are a master user or the owner of an account, you can enable password tracking and you can also set up a password for one-time access to the account. Password tracking enables users to store software password data for devices and their associated software.
{:shortdesc}

## Enabling password tracking
{: #customerportal_enabpwtrak}

The customer portal contains an optional [password tracking ![External link icon](../icons/launch-glyph.svg)](https://control.softlayer.com/devices/passwords){:new_window} tool for every account. Users can retrieve their user names and passwords through the tool if the information is lost or forgotten.

Support teams also use password tracking if remote access to a system is required. User names and passwords are used by Support only when necessary and authorized for ticket resolution.

Tracking passwords within the customer portal is optional and any user with appropriate permissions has the ability to view all passwords that are stored using this tool. User and password information are manually tracked so they are not automatically synced with a device or its software. Therefore, be sure to update the password tracking tool at the same time you update users and passwords on devices and software. Use the following steps to add a user to the password tracking tool.

1. Access the customer portal using your unique credentials.
2. Select **Devices** > **Manage** > **Passwords** from the menu.
3. Click the **Add Credentials** tab.
4. Select the **Device Name** the user is associated with from the **Device Name** drop down list.
5. Select the **Software** the user is associated with from the **Software** list.

  The software listed is provided by {{site.data.keyword.BluSoftlayer_notm}} infrastructure through paid or complimentary subscriptions. No third party software that has been manually installed on the device is available for tracking through the customer portal.
  {: tip}
  
6. Enter the user name and password for the software in the corresponding fields.
8. Optionally, you can enter any applicable comments in the **Notes** field.
9. Click **Add Credentials**.

After adding the user to the password tracking tool, the information is stored within the tool until it is manually deleted. All user name and password combinations are stored based on the device name by default. Entries are alphabetically displayed by device name, then by user name.

### Filtering information in the password tracking tool
{: #cp_filterusinfopwtracktool}

To view, edit, or delete user information from the password tracking tool, you can filter to quickly locate a user when the list spans several rows or pages. Use the following steps to filter by device, software or user in the password tracking tool.

1. Access the customer portal using your unique credentials.
2. Select **Devices** > **Manage** > **Passwords** from the menu.
3. Click the **Filter** tab.
4. Select or enter the device name, software, or user name in the corresponding fields.
5. Click **Filter**.

You can select the user information to view, edit or remove.

### Editing user information in the password tracking tool
{: #cp_editusinfopwtracktool}

After a user has been added to the password tracking tool, you can edit the details associated with the user or password. Use the following steps to edit information for a user in the password tracking tool.

1. Access the customer portal using your unique credentials.
2. Select **Devices** > **Manage** > **Passwords** from the menu.
3. Locate the device-user combination in the tool. Use the filter feature to quickly locate a user.
4. Click anywhere on the row to open the view the user details.
5. Update the **Username** or **Password** fields as necessary.
6. Click **Update** to save your changes.

After editing a user or password in the password tracking tool, the information is updated immediately.

## Configuring an account for one time password access
{: #cp_confportacc1timpwacc}

Before you can configure the account, you must first have set up the Verisign "VIP Access" application. If you have not done this, first download the application for one of the following devices:
* For your phone:  [https://m.vip.symantec.com/home.v ![External link icon](../icons/launch-glyph.svg)](https://m.vip.symantec.com/home.v){:new_window}
* For your desktop:  [https://idprotect.verisign.com/desktop/download.v ![External link icon](../icons/launch-glyph.svg)](https://idprotect.verisign.com/desktop/download.v){:new_window}

Then, complete the following steps:
1. Open the application. Find the Credential ID at the top and your current one-time password at the bottom. You can ignore the password initially, but you need the Credential ID for the portal so keep the application open.
2. Log in to the customer portal as the user for which you would like to configure the one-time password.
3. Click **Account** > **Users** > **Actions** > **Add External Authentication**.
4. Select the type of authentication to add. If you are using the Verisign application choose **Symantect Identity Protection**.
5. Enter the credential ID from step 1 and click **Continue**.
6. Complete the ordering process and your additional security option is automatically applied in just a few minutes.
7. After several minutes, select **Account** > **Users** from the navigation bar and select the user for which you configured the one-time password.
8. Click the **Update Credential** link Under the **Symantec Validation Settings** section.
9. Select **enabled** for the **Credential State** and click **Update credential**.
10. After the additional security option has been processed successfully, you can log in to the customer portal as usual. After you submit your user name and password, you are prompted to enter a security code.
11. Open the Verisign Identity Protection application on your preferred device and provide the code that is displayed to log in.

Save your original Verisign Identity Protection credential ID in a safe location for future reference. Without it, you can't access the portal.

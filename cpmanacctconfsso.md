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


# Configuring single sign-on
{: #customerportal_confssoserv}

If you are the master user of an account or have administrative access to it, you can configure single sign-on. Configuring single sign-on for {{site.data.keyword.BluSoftlayer_full}} infrastructure is a two step process.  First, you select and set up your identity provider. Then, you set up {{site.data.keyword.BluSoftlayer_notm}} infrastructure to receive the authentication request from your identity provider.
{:shortdesc}

## Selecting and setting up your identity provider
{: #cp_setupidprov}

If you do not already have an identity provider, first select one and set it up. You can use the following identity providers  with {{site.data.keyword.BluSoftlayer_notm}}:
* Ping Identity&reg;,
* OneLogin&trade;,
* IBM&reg; Cloud Security Enforcer,
* IBM Cloud Identity Services.
Contact your {{site.data.keyword.BluSoftlayer_notm}} infrastructure Sales Representative for more information.

If you do not already have an identity provider set up, you can contact your identity provider support for specific steps, or use the following high-level steps to configure your identity provider:
1. Prepare your identity provider environment by downloading and installing its executable.
2. Configure your identity provider to work with {{site.data.keyword.BluSoftlayer_notm}} authentication.

## Setting up {{site.data.keyword.BluSoftlayer_notm}} infrastructure for SSO
{: #cp_setupsso}

You must extract the following required fields of Security Assertion Markup Language&trade; (SAML&trade;) 2.0 metadata information from your identity provider to use with {{site.data.keyword.BluSoftlayer_notm}}.
<dl>
<dt>Entity ID</dt>
<dd>The entity ID of the identity provider.</dd>
<dt>Single Sign-on URL</dt>
<dd>The endpoint of the identity provider for SSO.</dd>
<dt>Certificate</dt>
<dd>The identity provider's certificate used to sign requests.</dd>
</dl>

The following field is optional:
<dl>
<dt>Certificate Fingerprint</dt>
<dd>The fingerprint of the certificate. This field can be used instead of the entire certificate.</dd>
</dl>

Use the following steps to set up {{site.data.keyword.BluSoftlayer_notm}} infrastructure to receive the authentication request from your identity provider:
1. Log in to your identity provider, if you are not already logged in, and locate the **SAML configuration** page. Note the following information:
  * Entity ID
  * Single sign-on URL
  * Certificate (This will vary based on your identity provider.)
2. Log in to {{site.data.keyword.BluSoftlayer_notm}} infrastructure as the master user with the master user name and password you used to create your SoftLayer account.
3. Click **Account** > **Manage** > **SAML Authentication**.
4. Enter the **Identity Provider** metadata.
5. Click **Save**.
6. Click **Account** > **Manage** > **SAML Authentication**.
7. Click **Download XML Configuration** to download the service provider metadata or jot down the information.
8. Use the **Service Provider** metadata to configure your identity provider based on the instructions of your identity provider.  

You should now be able to log in to {{site.data.keyword.BluSoftlayer_notm}} infrastructure by using your federated ID.

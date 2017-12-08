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

# Setting up identity federation
{: #cp_setupidfed}

You can set up identity federation to enable a service provider, such as {{site.data.keyword.BluSoftlayer_full}} Infrastructure Management System (IMS), to consume security tokens generated from a trusted identity system for authentication and authorization purposes.
{:shortdesc}

You can set up identity federation in {{site.data.keyword.BluSoftlayer_notm}} infrastructure SSO in one of the following ways:
* Creating users in the identity provider and {{site.data.keyword.BluSoftlayer_notm}} infrastructure
* Creating users in the identity provider

A role defines, for the service provider, what the user is authorized to do (through permissions) in their system after the user has been authenticated. For example, the *User* role might be permitted to only view different screens, but not update or add.

Multiple users can be assigned to a single role. Also, if a role exists in the identity provider but not in {{site.data.keyword.BluSoftlayer}} infrastructure, the user can still log in to {{site.data.keyword.BluSoftlayer}} infrastructure but the user does not have any permissions assigned to a role.
{: tip}


## Creating users in the identity provider and {{site.data.keyword.BluSoftlayer_notm}} infrastructure
{: #cp_scenario1both}

In this model, the following occurs:
* Users are created in both the identity provider and {{site.data.keyword.BluSoftlayer_notm}} infrastructure.
* User permissions are assigned in {{site.data.keyword.BluSoftlayer}} infrastructure IMS using the {{site.data.keyword.BluSoftlayer}} infrastructure customer portal or APIs.
* Users authenticate with the identity provider and federate their credentials.
* {{site.data.keyword.BluSoftlayer}} infrastructure consumes the credentials and access control is based on the permissions defined for the user in {{site.data.keyword.BluSoftlayer}} infrastructure IMS.

Accounts for users that need access to {{site.data.keyword.BluSoftlayer}} infrastructure are first created in {{site.data.keyword.BluSoftlayer}} infrastructure with random passwords. All permissions must be configured in {{site.data.keyword.BluSoftlayer}} infrastructure before the user is able to use SSO through the identity provider. Currently, permissions are set up based on the individual user.

### Setting up a user
Use the following steps to set up a user:

1. [Create users in {{site.data.keyword.BluSoftlayer}} infrastructure](/docs/customer-portal/cpmanacctadduser.html#customerportal_addusertocpacct).
2. Assign permissions in {{site.data.keyword.BluSoftlayer}} infrastructure.
3. Create users in the identity provider.

The **Email**, or **User Name**, field within the individual user profile is used for the Security Assertion Markup Language&trade;  (SAML&trade;) 2.0 token, which maps users between the identity provider and {{site.data.keyword.BluSoftlayer}} infrastructure.

### Example flow for log in authentication
Here's an example flow of how user log in authentication might work when you create users in the identity provider and {{site.data.keyword.BluSoftlayer_notm}} infrastructure:
1. The user accesses the identity provider URL from a browser session.
2. Identity provider authenticates the user, for example through its LDAP.
3. Identity provider returns SAML 2.0 responses.
4. Identity provider sends a SAML 2.0 response to the service provider, in this case {{site.data.keyword.BluSoftlayer}} infrastructure, to authenticate the user ID.
5. {{site.data.keyword.BluSoftlayer}} infrastructure validates the SAML 2.0 response.
6. The user is logged in to the {{site.data.keyword.BluSoftlayer}} infrastructure customer portal based on the trusted set up between the indentity provider and {{site.data.keyword.BluSoftlayer}} infrastructure.


## Creating users in the identity provider
{: #cp_scenario2idp}

In this model, the following things happen:
* Roles are created in the identity provider and assigned to the user.
* Role and permission assignments are set up in {{site.data.keyword.BluSoftlayer}} infrastructure IMS by using {{site.data.keyword.BluSoftlayer}} infrastructure APIs.
* Users authenticate with the identity provider and federate their credentials and role attributes.
* {{site.data.keyword.BluSoftlayer}} infrastructure consumes the user credentials and role attributes. If the user’s identity provider assigned role matches a role in {{site.data.keyword.BluSoftlayer}} infrastructure, the user is granted the permissions for that role when logging in to {{site.data.keyword.BluSoftlayer}} infrastructure.
* Users created in the identity provider are considered federated because they, and their roles, are authenticated through SAML 2.0.

### Setting up a role for a user
Use the following steps to set up a role for a user:

1. Set up roles through {{site.data.keyword.BluSoftlayer}} infrastructure API.
2. Set up roles in the identity provider.
3. Ensure that roles defined in {{site.data.keyword.BluSoftlayer}} infrastructure and the identity provider have the same name.

### Setting up a user
Use the following steps to set up a user:

1. Set up users in the identity provider.
2. Assign roles to users in the identity provider.

In this scenario, there is no need for you to manually create users in {{site.data.keyword.BluSoftlayer}} infrastructure.

### Example flow for user log in authentication
Here's an example flow of how user log in authentication might work when you create users in the identity provider:
1. The user accesses the identity provider URL from a browser session.
2. Identity provider authenticates the user, for example through its LDAP.
3. Identity provider returns SAML 2.0 responses.
4. Identity provider sends a SAML 2.0 response to the service provider, in this case {{site.data.keyword.BluSoftlayer}} infrastructure, to authenticate the user role.
5. {{site.data.keyword.BluSoftlayer}} infrastructure validates the SAML 2.0 response.
6. {{site.data.keyword.BluSoftlayer}} infrastructure redirects the user to the customer portal.
7. The user is logged in to the {{site.data.keyword.BluSoftlayer}} infrastructure customer portal.

Review your identity provider's procedures for setting up new roles and how to associate them with {{site.data.keyword.BluSoftlayer}} infrastructure.

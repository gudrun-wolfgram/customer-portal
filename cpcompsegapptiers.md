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

# Securing and scaling your environment
{: #cp_compsegapptierssecscal}

When hosting an application, two of the most critical aspects to consider for any system administrator are the security and scalability of the application. 
{:shortdesc}

## Securing your systems with firewalls
{: #cp_bpsecuresystem}

Firewalls are add-on services to any devices that you must manually configure and enable to ensure they are effective. You can lock down superfluous ports and disable public ports for private network-based systems to further manage outside accessibility to your systems. Performing regular vulnerability scans in the customer portal identifies any outstanding or unknown security risks so that you can mitigate risks quickly.

### Activating your firewall
{: #cp_bpnofirewalbypass}

Purchasing a firewall is a start to protecting your systems, but merely purchasing a firewall does not protect you. After it is provisioned, your firewall is in **Bypass Mode** and has no rules set. To get your firewall up and running, you must create rules and activate the firewall so that it can begin blocking unwanted activity.


## Securing your environment by segmenting your application tiers
{: #cp_copmsecenv}

By segmenting your logical application tiers into physical infrastructure tiers you can provide greater security through the use of access control lists (ACLs). When segmenting your application tiers, one of the most critical components to take into consideration is what traffic you allow into each tier and from where. To determine this, you will need to think about how your application fundamentally works and what services rely on each other to provide the end user with their requested content.

For example, with a two tiered application that relies on a web front and database back end, you would need to ensure that port 80 and 443 (if you're using SSL) are open to the internet on your web servers. You would probably also want to lock all ports down to the internet and manage your server over VPN by utilizing the {{site.data.keyword.BluSoftlayer_full}} infrastructure private network. In this scenario, you would probably want to unbind the public IP address on your database server and pass all traffic to it across port 1433 (for MSSQL) or port 3306 (for {{site.data.keyword.mysql}}) from your web server.  Your database server could be managed over the private network just like your web server, and you could setup a software firewall on the database server to lock down all traffic from the web server to the specific database ports.

By setting up your environment in this way, you increase security by keeping people from accessing SSH or RDP from the internet and disabling all internet traffic to your database.  Creating ACL’s between your web layer and database layer makes it more difficult to compromise your database in the event that your web server gets compromised.

## Scaling your environment by segmenting your application tiers
{: #cp_copmsecenv}

A multi-tiered environment also provides ease of scalability when compared to vertical or single host architectures. You can set up a multi-tiered environment to make scaling out your application easier by allowing scaling for the services that need additional resources. For example, in the previous scenario, if your web server is being over taxed, you can simply deploy another web server, replicate site or application data, and set up load balancing or round robin DNS to enable your two web servers to split your web load. Round robin DNS or load balancing provides high availability to your environment by enabling  multiple web servers to respond to incoming requests.  If a single server goes down, another node is available to handle end user requests.

You can also scale out your database. For example, with a {{site.data.keyword.mysql}} database, one option is to set up another physical server and use it as a ‘slave’ in a {{site.data.keyword.mysql}} Master/Slave replication setup.  You can segment all of your database writes to the ‘master’ and all reads to one or more ‘slaves’ to scale the database out to support more load.  This type of setup will also add a level of high availability by enabling you change the status of a ‘slave’ to ‘master’ and route both read and write traffic to it in the event that your {{site.data.keyword.mysql}} ‘master’ node goes down.

These ideas are just a few of many ways to secure and scale your environment. If you have any questions or concerns related to the best way to architect your environment from a security or scalability perspective, {{site.data.keyword.BluSoftlayer_notm}} infrastructure has a Sales Engineering team that can help.

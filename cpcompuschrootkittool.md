---

copyright:

  years: 1994, 2017

lastupdated: "2017-12-06"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:pre: .pre}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Creating system reports
{: #cp_compuschrootkit}

You can use the Chrootkit tool to scan, create, and email system reports. 
{:shortdesc}

To use the Chrootkit tool, first SSH as the admin to your server. Do not use telnet, which should already be disabled. Then, use the following steps:

1. Change to the root directory:  
  
  ```
  su -
  ```
  {: pre}
  
2. Run the following command:
  
  ```
  wget ftp://ftp.pangeia.com.br/pub/seg/pac/chkrootkit.tar.gz
  ```
  {: pre}
  
3. Check the MD5 SUM of the download for security:<br/
  
  ```
  ftp://ftp.pangeia.com.br/pub/seg/pac/chkrootkit.md5
  md5sum chkrootkit.tar.gz
  ```
  {: pre}
  
4. Unpack the tarball using the following command:<br/>
  
  ```
  tar xvzf chkrootkit.tar.gz
  ```
  {: pre}
  
5. Change to the directory it created:
  
  ```
  cd chkrootkit*
  ```
  {: pre}
  
6. Compile the results by running the following command:
  
  ```
  make sense
  ```
  {: pre}
  
7. To use chkrootkit, enter the following command:
  
  ```
  ./chkrootkit
  ```
  {: pre}

Everything the chkrootkit tool outputs should be `not found` or `not infected`.

If you see *Checking `bindshell`... INFECTED (PORTS: 465)* and you are running PortSentry, klaxon, or another program that binds itself to unused ports, chkrootkit is likely to give you a false positive on the bindshell test (ports 114/tcp, 465/tcp, 511/tcp, 1008/tcp, 1524/tcp, 1999/tcp, 3879/tcp, 4369/tcp, 5665/tcp, 10008/tcp, 12321/tcp, 23132/tcp, 27374/tcp, 29364/tcp, 31336/tcp, 31337/tcp, 45454/tcp, 47017/tcp, 47889/tcp, 60001/tcp).
{: tip}

8. Change the directory (`cd ..`) and remove the .gz file:  
  
  ```
  rm chkrootkit.tar.gz
  ```
  {: pre}

## Sending daily automated scans
{: #cp_chrootkitdaiautscan}

To set up a daily automated system scan that emails you a report, use the following steps:

1. While in SSH run the following command:
  
  ```
  pico /etc/cron.daily/chkrootkit.sh
  ```
  {: pre}
  
2. Add the following line to the new file:
  
  ```
  #!/bin/bash<br/>
  cd /yourinstallpath/chkrootkit-0.42b/<br/>
  ./chkrootkit | mail -s "Daily chkrootkit from Servername" admin@youremail.com
  ```
  {: pre}

3. Replace `yourinstallpath` with the actual path where you unpacked Chkrootkit.
4. Change `Servername` to the server you're running so you know where it's coming from.
5. Change `admin@youremail.com` to your actual email address where you want the script to email you.
6. Use the following command to save the file in SSH:
  
  ```
  Ctrl+X then type Y
  ```
  {: pre}
  
7. Change the file permissions to run it:
  
  ```
  chmod 755 /etc/cron.daily/chkrootkit.sh
  ```
  {: pre}
  
8.  Optionally, you can run a test report manually in SSH to see how it looks:
  
  ```
  cd /etc/cron.daily/
  ./chkrootkit.sh
  ```
  {: pre}

You're all set to receive a daily email with the report so you don't have to run it manually.

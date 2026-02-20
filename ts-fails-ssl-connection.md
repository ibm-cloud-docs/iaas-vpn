---

copyright:
  years: 2026, 2026
lastupdated: "2026-02-20"

keywords: IBM Cloud VPN, VPN FAQ, MotionPro

subcollection: iaas-vpn

---

{{site.data.keyword.attribute-definition-list}}

# While connecting to the MotionPro client, I receive an error that the MotionPro failed to establish a connection.
{: #troubleshoot-connection-errors}
{: troubleshoot}
{: support}

When connecting to the MotionPro client, an SSL connection error occurs.
{: shortdesc}

MotionPro displays the following SSL connection error:
{: tsSymptoms}

   `The MotionPro client fails to establish the SSL connection. Please check the network connection and your certifcate`

Possible causes include, but are not limited, to the following:
{: tsCauses}

1. Outdated MotionPro client version.
1. Incorrect system date and time.
1. DNS cache issue.

To resolve this issue, follow these steps:
{: tsResolve}

1. Download the latest MotionPro client version available from the [Array Networks Clients page](https://support.arraynetworks.net/prx/001/http/supportportal.arraynetworks.net/downloads/downloads.html){: external}.

   Uninstall the old client. After you install the newest client, restart your PC.
   {: #important}

1. Ensure that your computer is set to the correct time, time zone, and date.
1. Disconnect from any currently running VPN clients.
1. Flush your DNS Cache:

   * On Windows, follow these steps:
      * On the taskbar search, type "CMD."
      * Click "Run as administrator."
      * When the command prompt asks to make changes to your computer, click Yes.
      * Run the command `ipconfig /flushdns`

   * On Mac, follow these steps:
      * Press the _Command key + Space Bar_ or click the magnifying glass in the upper right corner.
      * Type "terminal".
      * Run the command `sudo killall -HUP mDNSResponder`.

1. Reattempt to connect to the MotionPro client.

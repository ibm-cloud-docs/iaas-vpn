---

copyright:
  years: 2022
lastupdated: "2022-08-17"

keywords:

subcollection: iaas-vpn

---

{{site.data.keyword.attribute-definition-list}}

# Why am I receiving an “VPN username/password incorrect” error when attempting to log in to the SSL VPN?
{: #troubleshoot-login-error}
{: troubleshoot}
{: support}

User is unable to connect due to an incorrect username, password, or both.
{: shortdesc}

User is receiving an error that their username or password is incorrect and are prompted to set a new password.
{: tsSymptoms}

There are a few possible causes for this issue:
{: tsCauses}

1. The permissions might have not been set for a new use to be allowed to SSL VPN.
1. Password might have not been set correctly.
1. Password might include too many special characters that our system cannot properly use. ## This requires review as we don't have documentation on what characters can cause issues.
1. Our authentication servers might need a synch to occur to correctly authenticate the user.

To resolve this issue, follow these steps:
{: tsResolve}

1. Ensure that SSL VPN access is enabled for your user. For more information, see [Activating or deactivating SSL VPN access for a user](/docs/iaas-vpn?topic=iaas-vpn-activate-or-deacivate-ssl-vpn-access-for-a-user).
1. Update your SSL VPN password. For more information, see [Updating a user's SSL VPN password](/docs/iaas-vpn?topic=iaas-vpn-update-users-ssl-vpn-password).
1. Ensure that you are using the latest version of MotionPro. For more information, see [Prerequisities](/docs/iaas-vpn?topic=iaas-vpn-standalone-vpn-clients#standalone-prereqs).
1. Toggle your SSL VPN access from on to off, then off to on.
1. Try three different VPN endpoints in different regions. For more information, click [Available VPN endpoints](/docs/iaas-vpn?topic=iaas-vpn-available-vpn-endpoints).
1. If you have exhausted these steps and are still running into the issue, create an [IBM Support case](https://cloud.ibm.com/unifiedsupport/cases/form){: external}.

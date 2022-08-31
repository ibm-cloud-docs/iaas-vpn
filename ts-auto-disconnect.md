---

copyright:
  years: 2022
lastupdated: "2022-03-10"

keywords: 

subcollection: iaas-vpn

---

{{site.data.keyword.attribute-definition-list}}

# Why am I disconnected from VPN after a period of time?
{: #troubleshoot-auto-disconnect}
{: troubleshoot}
{: support}

SSL VPN will auto-disconnect if a user becomes idle. 
{: shortdesc}

{: tsSymptoms}

User is disconnected if idle for a period of time, since this is not a dedicated VPN it does have a few limitations. 
{: tsCauses}

Auto-disconnect is working as expected because SSL VPN is designed to manage classic servers, but not for production use. There is a check against idle clients and the token is terminated if time is up.
{: tsResolve}

---

copyright:
  years: 2022
lastupdated: "2022-03-10"

keywords: 

subcollection: iaas-vpn

---

{{site.data.keyword.attribute-definition-list}}

# When attempting to install MotionPro on Mac, why am I receiving a MotionPro.pkg error?
{: #motionpro-pkg-error}
{: troubleshoot}
{: support}

When downloading MotionPro software, you might encounter a MotionPro.pkg error.
{: shortdesc}
 
You receive this error: `“MotionPro.pkg” can’t be opened because Apple cannot check it for malicious software.`
{: tsSymptoms}

This error might appear when downloading any software on a Mac from unverified sources on the web. 
{: tsCauses}

Follow these steps to resolve this issue:
{: tsResolve}

1. Go to **System Preferences > Security & Privacy**.
1. From `Allow apps downloaded from:`, select `App Store and identified developers`.
1. MotionPro is listed with an option to `Open Anyway`. Click this option.
1. Accept the confirmation prompt, then begin installing.
   For more information, see [Apple documentation](https://support.apple.com/en-us/HT202491){: external}.
1. If you do not see MotionPro and the option to **Open Anyway**, reinstall MotionPro and try again. 

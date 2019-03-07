---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: SSL VPN, Internet Explorer caching, Internet Explorer, Windows

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Resolve errors connecting to SSL VPN with Windows
{:#resolve-errors-connecting-to-ssl-vpn-with-windows}

If you are getting errors when connecting to SSL VPN with Windows, you can troubleshoot with the following steps:

1. Check for proper credentials and SSL permissions in [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/).
2. Check your time/date/time zone/dst on your PC.
3. You must accept and install the ActiveX applet.
4. Turn off PopUp blockers - they may block the ActiveX applet.
5. Check Personal Firewalls - allow ActiveX.
6. Allow Internet Explorer caching - in IE (select **Tools->Internet**, then **Options->Settings**).
7. Use Internet Explorer (IE) Browser only (check for updates).
8. Try a system reboot.

Once you're properly connected, an "A" will appear in the systray.

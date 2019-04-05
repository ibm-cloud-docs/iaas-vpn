---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-06"

keywords: SSL VPN, Internet Explorer caching, Internet Explorer, Windows

subcollection: iaas-vpn

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 解决通过 Windows 连接到 SSL VPN 时发生的错误
{:#resolve-errors-connecting-to-ssl-vpn-with-windows}

如果通过 Windows 连接到 SSL VPN 时遇到错误，那么可以使用以下步骤进行故障诊断：

1. 在[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/) 中检查凭证和 SSL 许可权是否正确。
2. 检查 PC 上的时间/日期/时区/夏令时设置。
3. 必须接受并安装 ActiveX 小程序。
4. 关闭弹出窗口阻止程序 - 这些程序可能会阻止 ActiveX 小程序。
5. 检查个人防火墙 - 允许 ActiveX。
6. 允许 Internet Explorer 高速缓存 - 在 IE 中（选择**工具 -> Internet****选项 -> 设置**）。
7. 使用“仅限 Internet Explorer (IE) 浏览器”（检查更新）。
8. 尝试重新引导系统。

正确连接后，系统托盘中将显示“A”。

# FortiGate
FortiGate scripts

The default DoS policy will clear video conferencing sessions, as it recognizes it as an attack. You can verify this by looking at your anomalies report.
If you are using the default settings for the IPv4 DoS Policy, you will need to create another policy above it that allows video conferencing traffic.

There are scripts, which creates addresses and address groups for most popular video conferencing software. After running this scripts you have to add the created address groups to the created IPv4 DoS Policy (Make sure this policy is above your previous - default policy). In this policy set the action for udp_flood to monitor (increase the Threshold to some bigger value, because if you leave 2000 then will be a lot of logs) or disable. After that video conferencing should works withot any issue.

The IP addresses I recive from this sites:
- Webex - https://help.webex.com/en-us/article/b2exve/Port-Reference-Information-for-Webex-Calling
- Pexip - https://pexip.me/test/firewall
- Zoom - https://support.zoom.us/hc/en-us/articles/201362683-Zoom-network-firewall-or-proxy-server-settings
- Teams - https://learn.microsoft.com/en-us/microsoft-365/enterprise/urls-and-ip-address-ranges?view=o365-worldwide#skype-for-business-online-and-microsoft-teams
- Clickmeeting - https://clickmeeting.com/pl/firewall-configuration

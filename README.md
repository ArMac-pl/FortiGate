# FortiGate
FortiGate scripts

The default DoS policy will clear video conferencing sessions, as it recognizes it as an attack. You can verify this by looking at your anomalies report.
If you are using the default settings for the IPv4 DoS Policy, you will need to create another policy above it that allows video conferencing traffic.

There are scripts, which creates addresses and address groups for most popular video conferencing software. After running this scripts you have to add the created address groups to the created IPv4 DoS Policy (Make sure this policy is above your previous - default policy). In this policy set the action for udp_flood to monitor (increase the Threshold to some bigger value, because if you leave 2000 then will be a lot of logs) or disable. After that video conferencing should works withot any issue.

Linode Dynamic DNS
==================

Linode Dynamic DNS is a script to update the IPv4 and IPv6 addresses for a particular record in the Linode DNS Manager using either the public IP or interface IP for a computer.


Usage
-----

Edit the `ddns` script fill in the parameters for `key`, `zone`, and `label`. The `key` parameter is your Linode API key obtained from "My Profile" -> "API Keys" in the Linode Manager. The `zone` parameter is the DNS zone, such as 'example.com'. The `label` parameter is the label that goes in front of the zone, such as `www`. The label can be empty to modify the root domain. The `ifip` parameter tells whether the script should get the IP from the primary internet interface or from an external service (icanhazip.com). You probably want `ifip=false` unless you know what you are doing.

I recommend copying the `ddns` script to your cron.hourly (with permission 700) so that your dns gets automatically updated.

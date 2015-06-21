Linode Dynamic DNS
==================

Linode Dynamic DNS is a script to update the IPv4 and IPv6 addresses for a particular record in the Linode DNS Manager using either the public IP or interface IP for a computer.


Usage
-----

Install [linode-cli](https://github.com/linode/cli) and edit the `ddns` script to fill in the parameters.

The `key` parameter is your Linode API key obtained from "My Profile" -> "API Keys" in the Linode Manager. The `zone` parameter is the DNS zone, such as 'example.com'. The `label` parameter is the label that goes in front of the zone, such as 'www'. The label can be empty to modify the root domain. The `ifip` parameter indicates whether the script should get the IP addresses from the primary internet interface or from an external service (icanhazip.com). You probably want `ifip=false` unless you know what you are doing.

I recommend copying the `ddns` script to your cron.hourly folder (with root only read permission) so that your DNS record gets automatically updated.

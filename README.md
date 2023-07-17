# IPsec Vodafone Station script for Strongswan Endian daemon
Script to keep IPsec Endian tunnel aligned with leftid parameter proposed by Vodafone Power Station, because Vodafone Power Station is dumb and cannot set the hostname instead of its public IP. You will need a DDNS hostname associated to Vodafone Station public IP, always updated by its DDNS service.

The script needs to be properly modified with you own configuration needs, by modifying the following variables:

VPNFILE: Endian VPN file configuration path, you should not need to modify it unless some upgrades has changed its location.
VFSTATIONIP: Vodafone Station private IP (es. 192.168.3.1). 
VPNCONNNAME: The name of Endian IPsec tunnel, as seen and defined from GUI.
REMOTEHOSTNAME: DDNS hostname associated to Vodafone Station public IP (es. vfstation.myddns.me).
REMOTEDNS: Remote DNS server that you want to use to resolve the DDNS hostnames. This is useful to avoid using local DNS cache, and to be sure the DDNS hostname is immediately resolved with the updated public IP.
MYHOSTNAME: Local DDNS hostname, this is needed to put the updated resolved local public IP as local ID of the IPsec connection, Vodafone Station requires it (it doesn't accept the DDNS hostname)

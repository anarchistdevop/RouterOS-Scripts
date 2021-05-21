# RouterOS-Scripts
Random Scripts and Stuff

1) Facebook IPv4 ASN List Update
This script fetches all FACEBOOK ASN ip ranges from https://api.hackertarget.com/aslookup/ and creates an Address List called FaceBook under ip -> firewall 
Note : It filters out only ipv4 addresses (I do not have ipv6 enabled on my router yet.)

The "FaceBook" address list can then be used to block all trafic to FaceBook's servers 
This includes whatsapp, instagram and any other Facebook owned domains and IP's 

The below rule is what I use on my network to block all Facebook traffic. 
/ip firewall nat add action=reject chain=forward comment="Block All Traffic to Facebook ASN's " dst-address-list=FaceBook in-interface-list=LAN reject-with=icmp-admin-prohibited





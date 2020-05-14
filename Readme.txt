This script is a solution made of others solutions (nothing new). The goal is to update your account on DNSoMatic.com. 
The main advantage on this solution is that DNSoMatic offers the possibility of propagating DNS updates to thirth party DNSlike systems like OpenDNS, 
DynDNS, Change IP and other 27 more.

If you're looking for a script that will run on a MikroTik that is not behind a NAT and behind NAT
-Behind NAT Network
-Not Behind NAT

Current Version

This new version is tested and working on RouterOS Version 5.14 & 6.6. Here are some of the features this script supports.

Works behind a NAT
Supports multiple DNS-O-Matic host update
The first time this script runs, it will not go through a full update to DNS-O-Matic. 
Subsequent runs, however, will work. 
This appears to be a limitation in RouterOS where it will not find a file that was created in the same script instance.

The following permissions are required for this script to run:

write
test
read
policy (for ROS 6.0+)



This will also need you to configure scheduler entry for periodical runs (maybe every minute or so). 
You will probably want a second scheduler event run this script upon RouterOS startup.

If for whatever reason the update fails, the script will not update DNSoMatic until the IP address changes again. 
This is rare, but could happen. 
It would be recommended to set up a third scheduler with longer intervals (maybe 1 hour) 
to run a script with the following code: Backup.txt


Credit for Wiki Mikrotik
https://wiki.mikrotik.com/wiki/Dynamic_DNS_Update_Script_for_DNSoMatic.com_behind_NAT
https://wiki.mikrotik.com/wiki/Dynamic_DNS_Update_Script_for_DNSoMatic.com

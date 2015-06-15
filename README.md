# Bashscript
Write a script which will determine and save to a file the IP address and Ethernet address of each of the available workstations on 

networks 172.16.1.0, 172.17.1.0, 172.18.1.0 and 1.72.19.1.0. To determine the Ethernet addresses ping each possible station on the 

network (use one or more loops in your script), capturing the ICMP packets produced by your pings in file Pingpacketlist. 

Use the command arp (see manual page for arp) to dump the contents of the ARP cache into the file ARPResults (this will contain the 

Ethernet addresses of the hosts that are available). DO NOT use the arp command immediately after pinging each machine, you 

should not dump the arp cache more than twice for each network. 

Use the contents of one or both of the two files, ARPResults and Pingpacketlist, to construct the third file below. Your script should be 

written in bash. You may find some combination of the following commands useful, ping, arp, awk, sed, grep, sort useful within your 

script. 

You may want to begin by writing your script to work on only one of the CMPT 471 virtual networks (172.16.1.0, OR 172.17.1.0,OR 

172.18.1.0 OR 172.19.1.0). DO NOT use the minilab (lab1-01 ...). When your script works on any one of the CMPT 471 virtual networks 

you can then expand it to work for all four of the networks in the 471 virtual labs. 

The script should produce 3 output files with the following names, each containing the following information 

File StationsUp 

• Contains 1 line of output for each possible host on networks 172.17.1.0, 172.18.1.0 and 1.72.19.1.0 in order from 172.16.1.1 to 

172.19.1.254. (Total of 255 lines for each of the four networks) 

• Each line in the file has one of the two following forms 

 IP address 172.16.1.x is not available 

 IP address 172.16.1.x has Ethernet address xx.xx.xx.xx.xx.xx 

• Contains summary lines at the end of the file indicating how many hosts were reachable (available) and how many were not 

• NOTE: If your script indicates many existing hosts are unreachable it may be because of inefficiencies in your script, remember 

entries in the ARP cache are not permanent! 

File ARPResults 

• Contains the contents of the ARP directory on the workstation running the script. Choose an efficient approach and explain why 

you think your choice is efficient. 

File PingPacketList 

• A wireshark output containing only the packets for your pings. You will need to filter out other packets.

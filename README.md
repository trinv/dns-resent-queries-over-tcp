## BIND9 - DNS Re-send queries over TCP using RPZ

I have an authoritative DNS server that uses bind9 software with version 9.16 (Debian). I want to be able to enable/disable DNS Cookies for this server with a configuration file and after that, I want to achieve this on my server:

If a DNS query is sent via UDP protocol to my DNS Server, I want to response to this query with a DNS response, in which the trucated header is set (TC Bit is 1), and I leave the answer section of the response empty. 

My goal with this is to switch the communication protocoll between the DNS resolver and the DNS server from UDP to the TCP protocol. So I will answer all the UDP Packets with a truncated response, where the answer section is empy. 

# Networking Labs

## Lab 01: ICMP Capture over SSH


### Objective

Capture ICMP Echo Requests and Echo Replies on the Ubuntu VM's enp0s8 interface while
pinging the NAT gateway at 10.0.3.2. Transfer the capture to Windows using SCP and analyze it in
Wireshark to verify packet counts, source and destination addresses, and ICMP Type and Code values.


### Results

- Ping reported 4 requests transmitted, 4 replies received, and 0% packet loss.
- tcpdump captured 8 packets and reported 0 packets dropped by the kernel.
- Echo Requests travelled from 10.0.3.15 to 10.0.3.2.
- Echo Replies travelled from 10.0.3.2 to 10.0.3.15.
- Echo Requests had ICMP Type 8, Code 0.
- Echo Replies had ICMP Type 0, Code 0.
- The filter `icmp.type == 8` displayed packets 1, 3, 5, and 7.
- The filter `icmp.type == 0` displayed packets 2, 4, 6, and 8.

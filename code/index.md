---
layout: default
course_number: CS335
title: Code
---

This page contains links to useful code snippets.

DNS
------------------------------------
- Add to `/etc/bind/`
  - [etc/bind/191.168.0](dns\191.168.0)
  - [etc/bind/cs335.com.db](dns\cs335.com.db)
- Append to `/etc/bind/named.conf`
  - [cs335zone](dns\cs335_zone)
- [dns_spoof.py](dns\dns_spoof.py)

TCP
------------------------------------
- Client: [tcp_client.c](tcp\tcp_client.c)
- Server: [tcp_server.c](tcp\tcp_server.c) & [tcp_server_multi.c](tcp\tcp_server_multi.c)
- Sent RST packet: [rst_packet.py](tcp\rst_packet.py)


Packet Sniffing and Spoofing
------------------------------------
- Sniffing
  - Packet Sniffing using raw sockets: [sniff_raw.c](sniff\sniff_raw.c)
  - Packet Sniffing using pcap API: [sniff_pcap.c](sniff\sniff_pcap.c)
  - Packet Sniffing using pcap API (ether): [sniff_ether.c](sniff\sniff_ether.c)
  - Send Raw Packets (method only): [spoof.c](sniff\spoof.c)
  - Sniff using Scapy: [sniff.py](sniff\sniff.py)
- Spoofing
  - Spoof ICMP using raw sockets: [spoof_icmp.c](sniff\spoof_icmp.c)
  - Spoof UDP using raw sockets: [spoof_udp.c](sniff\spoof_udp.c)
  - Spoof TCP using raw sockets: [spoof_tcp.c](sniff\spoof_tcp.c)
  - Spoof UDP using Scapy: [spoof_udp.py](sniff\spoof_udp.py)
  - Spoof ICMP using Scapy: [spoof_icmp.py](sniff\spoof_icmp.py)
- Misc
  - UDP client: [udp_client.c](sniff\udp_client.c)
  - UDP server: [udp_server.c](sniff\udp_server.c)
  - TCP/IP Header Structures: [ip.h](sniff\ip.h)
  - Calculating Checksum: [checksum.h](sniff\checksum.c)
- Sniffing along with Spoofing
  - Create packet using Scapy: [create_udp_packet.py](sniff\create_udp_packet.py)
  - Send created packet using raw sockets: [send_udp_packet.c](sniff\send_udp_packet.c)
  - Sniffing and the Spoofing ICMP using Scapy: [sniff_snoop_icmp.py](sniff\sniff_snoop_icmp.py)

Buffer Overflow
------------------------------------
- Memory Layout: [mem_layout.cpp](buffer_overflow\mem_layout.cpp)

Shell Shock
------------------------------------
- Attack on Set-UID: [vul.c](shell_shock\vul.c)
- Vulnerable Bash program: [variables.c](shell_shock\variables.c)
- Attack on CGI program: [test.cgi](shell_shock\test.cgi)

Reverse Shell
------------------------------------
- File Descriptors: [fd.c](reverse_shell\fd.c)
- Redirection (demo): [red.c](reverse_shell\red.c)
- Redirection (dup): [dup.c](reverse_shell\dup.c)
- Redirection (dup2): [dup2.c](reverse_shell\dup2.c)
- Redirection (tcp): [tcp_out.c](reverse_shell\tcp_out.c)
- Redirection (tcp): [tcp_in.c](reverse_shell\tcp_in.c)

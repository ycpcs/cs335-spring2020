---
layout: default
course_number: CS335
title: Code
---

This page contains links to useful code snippets.

Reverse Shell
------------------------------------
- File Descriptors: [fd.c](reverse_shell\fd.c)
- Redirection (demo): [red.c](reverse_shell\red.c)
- Redirection (dup): [dup.c](reverse_shell\dup.c)
- Redirection (dup2): [dup2.c](reverse_shell\dup2.c)
- Redirection (tcp): [tcp_out.c](reverse_shell\tcp_out.c)
- Redirection (tcp): [tcp_in.c](reverse_shell\tcp_in.c)


Shell Shock
------------------------------------
- Attack on Set-UID: [vul.c](shell_shock\vul.c)
- Vulnerable Bash program: [variables.c](shell_shock\variables.c)
- Attack on CGI program: [test.cgi](shell_shock\test.cgi)

Buffer Overflow
------------------------------------
- Memory Layout: [mem_layout.cpp](buffer_overflow\mem_layout.cpp)

Packet Sniffing and Spoofing
------------------------------------
- UDP server: [udp_server.c](sniff\udp_server.c)
- UDP client: [udp_client.c](sniff\udp_client.c)
- Packet Sniffing (raw): [sniff_raw.c](sniff\sniff_raw.c)
- Packet Sniffing (pcap): [sniff_pcap.c](\sniff\sniff_pcap.c)
- Packet Sniffing (ether): [sniff_ether.c](sniff\sniff_ether.c)
- Header Structures: [ip.h](sniff\ip.h)
- Calculating Checksum: [checksum.h](sniff\checksum.c)
- Send Raw Packets: [spoof.c](sniff\spoof.c)
- Spoof ICMP: [spoof_icmp.c](sniff\spoof_icmp.c)

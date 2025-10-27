# cyber-intern-task5
Wireshark packet capture &amp; analysis . Identified protocols (DNS, ICMP, TCP) and submitted a .pcap report.
Task 5: Wireshark Packet Capture & Analysis

The objective of this task was to capture live network packets on my Kali Linux machine, analyze the traffic using Wireshark, and identify at least three different protocols.

Tools Used:

Operating System: Kali Linux

Analysis Tool: Wireshark

Execution: 

Here is a summary of the 8 steps I followed to complete this task:

Install Wireshark:
Wireshark was already pre-installed as part of the standard Kali Linux distribution.

Start Capturing:
I launched Wireshark with sudo privileges and started a live capture on my primary network interface (eth0 or wlan0).

Generate Traffic:
To ensure a good mix of protocols for analysis, I generated traffic by:

Using the ping google.com command in the terminal (to generate ICMP traffic).

Opening a web browser and visiting http://example.com (to generate DNS and TCP/HTTP traffic).

Stop Capture:
After about one minute of capturing this activity, I stopped the packet capture in Wireshark to begin the analysis.

Filter Captured Packets:
I used Wireshark's display filter bar to isolate specific protocols. The three main filters I used were icmp, dns, and tcp.

Identify Protocols:
By filtering the packets, I successfully identified the following three protocols:

ICMP (Internet Control Message Protocol)

DNS (Domain Name System)

TCP (Transmission Control Protocol)

Export the Capture:
The complete, unfiltered packet capture was saved as a .pcapng file, which is included in this repository.

Summarize Findings:
This README serves as the summary report. The findings, including screenshots of the filtered packets, are detailed below.

Summary of Findings & Identified Protocols

By analyzing the captured packets, I was able to observe the behavior of the following protocols:

1. ICMP (Internet Control Message Protocol)

How it was generated: By using the ping google.com command.

Observation: The filter icmp clearly showed the "Echo (ping) request" packets sent from my machine and the corresponding "Echo (ping) reply" packets from the Google server. This protocol is used for network diagnostics.

2. DNS (Domain Name System)

How it was generated: By my system needing to resolve the domain names google.com (for the ping) and example.com (for the browser).

Observation: The filter dns showed the "Standard query" packets asking "What is the IP address for google.com?" and the "Standard query response" packets from the DNS server providing the IP address.

3. TCP (Transmission Control Protocol)

How it was generated: By the web browser when connecting to http://example.com.

Observation: The filter tcp showed the famous "three-way handshake" ([SYN], [SYN, ACK], [ACK]) that TCP uses to establish a reliable connection before any actual HTTP data was sent.

Deliverables

All required files for this task are included in this repository.

1. Full Packet Capture File
[wireshARK.PNG.pcapng (2).txt](https://github.com/user-attachments/files/23165698/wireshARK.PNG.pcapng.2.txt)


(This is the complete, unfiltered packet capture file.)

2. Filtered Protocol Screenshots

Below are the screenshots from Wireshark showing the filtered results for each identified protocol.

ICMP (icmp) Filter Results:
This screenshot shows the ping command's "request" and "reply" packets.
![WhatsApp Image 2025-10-27 at 19 08 40](https://github.com/user-attachments/assets/43f5589b-fb09-404a-a481-66194261bcaf)


DNS (dns) Filter Results:
This screenshot shows the "Standard query" from my machine and the "Standard query response" from the DNS server.
![WhatsApp Image 2025-10-27 at 19 09 40](https://github.com/user-attachments/assets/125754db-d53b-415a-bdcb-f4b971125f84)


TCP (tcp) Filter Results:
This screenshot shows the [SYN], [SYN, ACK], and [ACK] packets of the TCP three-way handshake.
![WhatsApp Image 2025-10-27 at 19 08 32](https://github.com/user-attachments/assets/c5a76a8e-cb3a-4e46-8c93-8260125b926a)

\# Cybersecurity Tool Testing



\## 1. Wireshark — Network Traffic Analysis



\*\*Objective:\*\* Capture and inspect network packets in the lab environment.



\*\*Environment:\*\* Kali Linux and the lab network.



\*\*Steps performed:\*\*

1\. Opened Wireshark and selected the lab network interface.

2\. Generated network traffic using ping.

3\. Applied the display filter `icmp`.

4\. Inspected ICMP packets.



\*\*Observation:\*\* icmp echo request and echo reply has been appeared.



\*\*Evidence:\*\* `screenshots/capture.pcap.png`



\*\*Capture file:\*\* `results/capture.pcap.png`



\*\*Result:\*\* captured successfully.



\---



\## 2. Nmap — Port and Service Discovery



\*\*Objective:\*\* Identify open TCP ports and the services running on the lab target.



\*\*Target:\*\* Metasploitable 2 (`192.168.56.102`)



\*\*Command:\*\* `nmap -sV 192.168.56.102 -oN nmap-results.txt`



\*\*Observation:\*\* The host was up. Nmap reported 977 closed TCP ports and identified multiple open ports, including FTP (21), SSH (22), Telnet (23), HTTP (80), MySQL (3306), and PostgreSQL (5432).



\*\*Security relevance:\*\* Service discovery helps identify the exposed network attack surface. An open port alone does not prove a vulnerability.



\*\*Evidence:\*\* `screenshots/nmap result.png`



\*\*Results file:\*\* `results/nmap-results.txt`



\*\*Result:\*\* Completed.



\---



\## 3. Burp Suite — HTTP Request Interception



\*\*Objective:\*\* Understand how HTTP requests can be intercepted and inspected.



\*\*Steps performed:\*\*

1\. Started Burp Suite.

2\. Opened its built-in browser.

3\. Visited the test website.

4\. Inspected the intercepted HTTP request.

5\. Forwarded the request and disabled interception.



\*\*Observation:\*\* the request method, host, and the request was forwarded successfully.



\*\*Evidence:\*\* `screenshots/burp suite.png`



\*\*Result:\*\* test completed successfully.



\---



\## 4. Netcat — Basic TCP Connection Test



\*\*Objective:\*\* Test a basic TCP connection using Netcat.



\*\*Environment:\*\* Kali Linux, local loopback interface.



\*\*Listener command:\*\* `nc -lvnp 4444`



\*\*Client command:\*\* `nc 127.0.0.1 4444`



\*\*Observation:\*\* verified, the test message sent by the client appeared in the listener terminal.



\*\*Evidence:\*\* `screenshots/net cat 1.png`,`screenshots/netcat2.png`



\*\*Result:\*\* test completed successfully



\---



\## Overall Conclusion



These practicals introduced network traffic inspection, port and service discovery, HTTP request interception, and basic TCP connectivity testing. The results demonstrate how common cybersecurity tools can support network analysis and security assessment in an authorized lab environment.


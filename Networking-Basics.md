\# Networking Basics



\## Objective

Understand basic networking concepts and practise network inspection in a controlled cybersecurity lab.



\## 1. IP Addressing

An IP address identifies a device on an IP network. IPv4 addresses use 32 bits and are commonly written as four decimal numbers separated by dots.



\## 2. Default Gateway

A default gateway forwards traffic to networks outside the local network when a suitable route exists.



\## 3. DNS

The Domain Name System (DNS) translates domain names into IP addresses and other DNS records.



\## 4. TCP and UDP

\- \*\*TCP:\*\* Connection-oriented transport protocol that provides reliable, ordered delivery.

\- \*\*UDP:\*\* Connectionless transport protocol with lower overhead and no built-in delivery guarantee.



\## 5. Ports and Services

Port numbers help identify applications and services communicating over a network. Examples include HTTP on port 80, HTTPS on port 443, and SSH on port 22.



\## 6. Lab Connectivity

\*\*Target:\*\* Metasploitable 2  

\*\*Target IP:\*\* 192.168.56.102



Nmap was used to inspect the lab target and identify open TCP ports and services. See `results/nmap-results.txt` for the recorded scan results.



\*\*Ping test:\*\* ping test has been tested successfully.



\## 7. Network Traffic Analysis

Wireshark was used to capture and inspect network traffic. The `icmp` display filter was used during the ping test to focus on ICMP packets.



\*\*Observation:\*\* i have observed the icmp echo request and echo reply packets



\## Conclusion

The practical introduced IP addressing, network services, ports, and packet inspection. These concepts help cybersecurity analysts understand network communication and identify exposed services during authorized assessments.


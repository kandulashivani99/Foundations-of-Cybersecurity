\# Cybersecurity Basics



\## 1. Introduction



Cybersecurity is the practice of protecting computers, networks, applications, and data from unauthorized access, misuse, damage, and cyberattacks.



Its goal is to maintain the confidentiality, integrity, and availability of information and systems.



\## 2. The CIA Triad



The CIA triad is a fundamental information security model.



\### Confidentiality

Ensures that information is accessible only to authorized people and systems.



\*\*Example:\*\* Using access controls and encryption to protect sensitive files.



\### Integrity

Ensures that information remains accurate and is not modified without authorization.



\*\*Example:\*\* Using SHA-256 hashes to check whether a file has changed.



\### Availability

Ensures that systems and information remain accessible when needed.



\*\*Example:\*\* Maintaining backups and protecting services against denial-of-service attacks.



\## 3. Common Cybersecurity Threats



\### Phishing

Fraudulent emails, messages, or websites designed to trick people into revealing information or opening malicious links.



\*\*Prevention:\*\* Verify senders, inspect links, and avoid unexpected attachments.



\### Malware

Malicious software designed to damage systems, steal information, or provide unauthorized access.



Examples include viruses, worms, Trojans, spyware, and ransomware.



\*\*Prevention:\*\* Keep software updated and use trusted security tools.



\### Ransomware

Malware that encrypts or otherwise blocks access to data and demands payment.



\*\*Prevention:\*\* Maintain offline or protected backups, patch systems, and restrict access.



\### Denial-of-Service (DoS)

An attack that attempts to make a system or service unavailable by overwhelming or disrupting it.



\*\*Prevention:\*\* Use traffic filtering, rate limiting, monitoring, and suitable network protections.



\### SQL Injection

A vulnerability in which untrusted input changes the meaning of a database query.



\*\*Prevention:\*\* Use parameterized queries, safe database APIs, and input validation.



\### Brute-Force Attacks

Repeated attempts to guess passwords or other credentials.



\*\*Prevention:\*\* Use strong unique passwords, multi-factor authentication, and login rate limiting.



\### Social Engineering

Manipulating people into disclosing information or performing unsafe actions.



\*\*Prevention:\*\* Verify unusual requests and follow established security procedures.



\### Insider Threats

Security risks caused by people with legitimate access, whether intentional or accidental.



\*\*Prevention:\*\* Apply least privilege, monitor access, and review permissions regularly.



\## 4. Authentication and Authorization



\*\*Authentication\*\* verifies a user's identity.



\*\*Authorization\*\* determines what an authenticated user is permitted to access or do.



For example, successfully logging in does not mean a user should be able to access an administrator-only page.



\## 5. Basic Security Practices



\- Use strong, unique passwords and a password manager.

\- Enable multi-factor authentication where possible.

\- Install security updates promptly.

\- Back up important data.

\- Limit user privileges according to job requirements.

\- Use firewalls and appropriate endpoint protection.

\- Avoid suspicious links and attachments.

\- Monitor logs for unusual activity.

\- Encrypt sensitive information where appropriate.

\- Test systems only with proper authorization.



\## 6. Vulnerability Assessment



A vulnerability assessment identifies and evaluates potential weaknesses in systems, applications, and networks.



Common activities include asset discovery, port scanning, service identification, vulnerability identification, risk assessment, and remediation recommendations.



Tools such as Nmap can help discover open ports and services. A scan result alone does not prove that a vulnerability is exploitable.



\## 7. Lab Activities



The practical work for this project includes:



\- Linux command-line operations and file permissions.

\- Encryption and decryption using OpenSSL.

\- SHA-256 hash comparison for file integrity verification.

\- Network packet capture and inspection using Wireshark.

\- Port and service discovery using Nmap.

\- HTTP request inspection using Burp Suite.

\- Basic TCP connection testing using Netcat.



Refer to `Tool-Testing.md` and the `results/` directory for the practical observations and evidence.



\## 8. Conclusion



Understanding cybersecurity fundamentals helps identify threats, reduce security risks, and protect information systems. The CIA triad, access control, secure configuration, monitoring, and authorized security testing form an important foundation for further cybersecurity learning.


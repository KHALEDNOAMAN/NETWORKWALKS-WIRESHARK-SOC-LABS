# Networkwalks – Wireshark SOC Labs

## Overview

This repository documents my practical work completing six Security Operations Centre (SOC) labs using Wireshark as part of the Networkwalks Cybersecurity Internship.

The exercises focused on analysing network traffic, investigating suspicious activity, identifying potential attackers, inspecting TCP conversations, detecting exposed credentials, and investigating suspicious VoIP calls.

## Tools Used

- Wireshark
- Linux
- TCP/IP
- HTTP
- FTP
- SIP
- RTP
- Network packet analysis

## Labs Completed

### 1. Identify the Attacker's IP

**Objective:** Identify a suspicious IP address responsible for unusual network activity.

**Activities:**

- Analysed captured network traffic.
- Inspected source and destination IP addresses.
- Used Wireshark filters to narrow down suspicious packets.
- Investigated traffic patterns to identify the suspected attacker.

**Key Learning:** Understanding how packet analysis can help identify suspicious hosts and investigate network attacks.

**Evidence:** `screenshots/01-attacker-ip/`

---

### 2. Follow TCP Stream 1

**Objective:** Reconstruct a TCP conversation and inspect the information exchanged between two hosts.

**Activities:**

- Applied TCP display filters.
- Used Follow TCP Stream to reconstruct the conversation.
- Examined client-server communication.
- Inspected the transmitted data.

**Key Learning:** TCP stream reconstruction helps analysts understand application-level communication and identify potentially exposed information.

**Evidence:** `screenshots/02-follow-tcp-stream/`

---

### 3. Follow TCP Stream – Part 2

**Objective:** Investigate another network capture and identify information hidden within TCP communication.

**Activities:**

- Examined TCP conversations.
- Reconstructed communication between hosts.
- Inspected transmitted content.
- Investigated information that could be exposed through network traffic.

**Key Learning:** Packet captures can contain valuable evidence that is not immediately visible in the packet list.

**Evidence:** `screenshots/03-follow-tcp-stream-part-2/`

---

### 4. HTTP Plain Text Credentials

**Objective:** Investigate how credentials can be exposed when transmitted over unencrypted HTTP.

**Activities:**

- Filtered HTTP requests.
- Inspected HTTP POST requests.
- Examined request data.
- Investigated credentials transmitted without transport encryption.

**Key Learning:** HTTP does not encrypt transmitted information. HTTPS using TLS helps protect sensitive information while it is in transit.

**Evidence:** `screenshots/04-http-credentials/`

---

### 5. Catch the Brute Force Attacker

**Objective:** Investigate repeated login attempts and identify the suspected source of a brute-force attack.

**Activities:**

- Analysed authentication-related traffic.
- Inspected repeated login attempts.
- Examined FTP commands and responses.
- Investigated the source IP associated with suspicious login activity.

**Key Learning:** Repeated authentication attempts can indicate password-guessing activity. Network monitoring and account protection mechanisms help detect and prevent these attacks.

**Evidence:** `screenshots/05-brute-force-attacker/`

---

### 6. Catch the Call Scammer

**Objective:** Investigate VoIP traffic and analyse a suspicious phone conversation.

**Activities:**

- Examined SIP signalling.
- Identified call-related information.
- Investigated RTP voice traffic.
- Identified the audio codec.
- Explored the security risks of unencrypted voice communication.

**Key Learning:** Unencrypted RTP traffic can expose voice conversations to anyone with access to the captured packets. SRTP helps protect voice traffic through encryption.

**Evidence:** `screenshots/06-call-scammer/`

---

## Skills Practised

- Network traffic analysis
- Packet inspection
- TCP stream reconstruction
- IP address investigation
- HTTP request analysis
- Authentication traffic investigation
- Brute-force attack detection
- SIP and RTP analysis
- VoIP security fundamentals
- Wireshark display filters

## Security Lessons

These exercises demonstrated several important network security risks:

1. Unencrypted HTTP can expose sensitive information.
2. Repeated login attempts can indicate brute-force attacks.
3. TCP conversations can reveal information exchanged between hosts.
4. Unencrypted RTP can expose private voice conversations.
5. Network traffic analysis helps security analysts investigate suspicious activity.

## Conclusion

Completing these six labs strengthened my practical understanding of network traffic analysis and introductory SOC investigation techniques.

This repository serves as evidence of my hands-on learning and continued development in networking and cybersecurity.

**Programme:** Networkwalks Cybersecurity Internship
**Module:** Wireshark Project Module (Extra)
**Platform:** Ubuntu Linux
**Primary Tool:** Wireshark

*All activities were conducted in authorised training lab environments.*

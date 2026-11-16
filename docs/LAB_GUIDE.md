# Wireshark SOC Labs - Lab Guide

## Lab Overview
| Lab | Topic | Skills |
|-----|-------|--------|
| 1 | Traffic Analysis | Packet capture, filtering |
| 2 | TCP Investigation | Stream reassembly, flags |
| 3 | HTTP Credentials | Cleartext detection |
| 4 | Brute Force Detection | Login attempt patterns |
| 5 | Attacker ID | IP tracing, GeoIP |
| 6 | VoIP Security | SIP/RTP analysis |

## Common Filters
| Filter | Purpose |
|--------|---------|
| http.request.method == "POST" | Login attempts |
| tcp.flags.syn == 1 && tcp.flags.ack == 0 | SYN scans |
| dns.qry.name contains "malicious" | DNS exfiltration |
| ip.src == 10.0.0.1 | Source IP filter |

## SOC Analyst Workflow
```
Alert --> Capture --> Filter --> Analyze --> Document --> Escalate
                      |           |
                  Display     Follow TCP
                  Filters     Stream
```

## Tools Required
- Wireshark 4.0+
- Kali Linux (recommended)
- VirtualBox for lab VMs
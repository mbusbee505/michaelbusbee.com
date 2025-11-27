# Sample Challenge

This is a sample challenge writeup to demonstrate the layout and styling.

## Overview

This challenge involves analyzing network traffic to identify malicious activity.

## Tools Used

- Wireshark
- Splunk
- CyberChef

## Investigation Steps

1. **Initial Analysis**: First, I examined the PCAP file in Wireshark
2. **Pattern Recognition**: I noticed unusual DNS queries
3. **Threat Identification**: The queries matched a known C2 pattern

## Key Findings

> This is an important note about the investigation.

### Network Traffic Analysis

The attacker used the following techniques:
- DNS tunneling for data exfiltration
- Base64 encoded payloads
- Multiple C2 domains

## Code Example

```python
import base64

def decode_packet(data):
    decoded = base64.b64decode(data)
    return decoded.decode('utf-8')
```

## Conclusion

The investigation revealed a sophisticated attack campaign using DNS tunneling for command and control communications.

**IOCs Identified:**
- Domain: `malicious.example.com`
- IP Address: `192.168.1.100`
- Hash: `5d41402abc4b2a76b9719d911017c592`

---

*End of writeup*

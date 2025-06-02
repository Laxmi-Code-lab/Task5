# Task5  Capture and Analyze Network Traffic Using Wireshark

1. Objective
The objective of this task is to perform a detailed network traffic analysis using Wireshark by capturing live packets and identifying key protocols and data flows. The analysis focuses on typical internet activity such as web browsing and pinging public DNS servers.

---

 2. Tools and Environment

| Component       | Details                            |
|----------------|-------------------------------------|
| Tool Used       | Wireshark (Latest Version)         |
| OS Platform     | Windows 10 / Ubuntu 22.04          |
| Network Adapter | Wi-Fi (Active Interface)           |
| Capture File    | `438d8106-7a4a-405b-a5ec-e649b610ff5a.pcapng` |

---

3. Methodology

1. **Installation**: Installed Wireshark from the official site [https://www.wireshark.org/](https://www.wireshark.org/).
2. **Interface Selection**: Selected active network interface (Wi-Fi).
3. **Traffic Generation**:
   - Opened websites: `https://google.com`, `https://youtube.com`
   - Executed ping command: `ping 8.8.8.8`
4. **Capture Duration**: ~1 minute of live traffic
5. **File Saved As**: `.pcapng` format for analysis

---

 4. Protocols Identified

| Protocol | Description                              | Usage Scenario                       |
|----------|------------------------------------------|--------------------------------------|
| DNS      | Resolves domain names to IP addresses    | Name resolution for web browsing     |
| TCP      | Connection-oriented transport protocol   | Used in HTTP/HTTPS communication     |
| HTTP     | Application protocol for web traffic     | Browsing websites                    |
| ICMP     | Network diagnostic and control           | Used for ping (echo request/reply)   |

---

 5. Detailed Packet Analysis

### a) DNS Query Packet
- **Source IP**: `192.168.x.x`
- **Destination IP**: `8.8.8.8`
- **Query**: `www.google.com`
- **Transport Layer**: UDP

### b) HTTP Request Packet
- **Request Method**: GET
- **Host**: `www.youtube.com`
- **Response Code**: 200 OK
- **Transport Layer**: TCP

### c) ICMP Echo Packet
- **Type**: Echo Request (Ping)
- **Destination**: `8.8.8.8` (Google DNS)
- **Response Time**: ~30 ms

---

 6. Observations

- **DNS resolution** occurred before HTTP traffic, showing correct network resolution flow.
- **TCP handshakes** were observed before HTTP GET requests.
- **ICMP packets** confirmed successful external connectivity.
- The traffic showcases a standard client-server communication lifecycle.

---

 7. File Attachment
  438d8106-7a4a-405b-a5ec-e649b610ff5a.pcapng



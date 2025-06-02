# CYBER SECURITY INTERNSHIP
# Task 5 - Wireshark Network Traffic Analysis

## Objective:
Capture live network traffic using Wireshark and identify at least three different protocols to understand how packet-based communication works in real time.

## Tools Used:
- Wireshark (free network protocol analyzer)

## Steps Performed:
1. Installed Wireshark on the system.
2. Started packet capture on the active network interface (eth0).
3. Generated network traffic by visiting Netflix website.
![Screenshot From 2025-06-02 10-41-35](https://github.com/user-attachments/assets/5c986a46-10c7-47a4-91d7-c67abfe6e86e)
4. Captured traffic for around 1 minute and stopped the capture.
5. Applied protocol filters like `http`, `dns`, and `tcp` to inspect specific traffic types.
  - **http**
    ![Screenshot From 2025-06-02 10-42-49](https://github.com/user-attachments/assets/069a2b35-741d-4889-abcc-194a7b7eef9b)
  - **DNS**
    ![Screenshot From 2025-06-02 10-43-34](https://github.com/user-attachments/assets/2f72601f-6afd-40a6-b20a-d56d136bf501)
  - **tcp.port == 80||udp.port == 80**
    ![Screenshot From 2025-06-02 10-44-39](https://github.com/user-attachments/assets/e0ba69f8-5b6e-482b-bfd0-a25e8586f3ce)
  - **ip.addr == 10.0.2.15**
    ![Screenshot From 2025-06-02 10-45-50](https://github.com/user-attachments/assets/749192c8-9713-4805-9c54-c92328fde3ac)
6. Saved the capture file in `.pcap` format.
  - **.pcapng-file drive link:** https://drive.google.com/file/d/1Hx-onjUCrTf_ucBo3zZDDh1lMHd1Xs4n/view?usp=drive_link
7. Analyzed the packet details and documented findings:

## Protocols Identified:

### 1. HTTP (Hypertext Transfer Protocol)
- **Description**: Used for loading web pages over the internet.
- **Port**: 80
- **Packet Info**: GET requests and response headers observed.
- **Example**: Source IP: 10.0.2.15 → Destination IP: 142.251.223.3

### 2. DNS (Domain Name System)
- **Description**: Resolves domain names to IP addresses.
- **Port**: 53
- **Packet Info**: Standard query and response for domains like `www.google.com`.

### 3. TCP (Transmission Control Protocol)
- **Description**: Provides reliable, ordered, and error-checked delivery of data.
- **Port**: 443 (used for HTTPS)
- **Packet Info**: SYN, SYN-ACK, and ACK observed for connection handshakes.

## Sample Filters Used:
- `http`
- `dns`
- `tcp.port == 80||udp.port == 80`
- `ip.addr == 10.0.2.15`



# Wireshark Packet Capture Summary

This summary is based on the Wireshark session from `eth0` as seen in the screenshots.

## 🔍 Observed Behavior

- **Source IP**: `192.168.35.128`
- **Destination IP**: `50.116.58.136`
- **Src Port**: 58891
- **Dst Port**: 5963
- **TCP Flags**: 
  - SYN from source
  - RST, ACK from destination
- **Status**: Target refused TCP handshake (likely filtered or closed port)

## 📊 Stats

- **Total Packets Captured**: 478
- **Displayed Packets**: 478
- **Capture Interface**: `eth0`
- **Profile**: Default

## 📌 Key Packet

```
Frame 9: 58 bytes on wire (464 bits), 58 bytes captured (464 bits)
Ethernet II, Src: VMware_cd:cb:b1 → Dst: VMware_f2:a8:53
IPv4, Src: 192.168.35.128 → Dst: 50.116.58.136
TCP, Src Port: 58891 → Dst Port: 5963, Seq=0, Len=0
```

## 🛠 Notes

This traffic confirms the active scanning behavior from the attacker's host. The target system consistently responds with TCP RST-ACK, indicating no service is open or accepting connections on that port.

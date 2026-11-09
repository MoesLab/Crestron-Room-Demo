# Network and IP Table

## VLAN plan

| VLAN | Name | Subnet | Mask | Gateway | DHCP pool |
|---|---|---|---|---|---|
| 10 | Data | 192.168.10.0 | 255.255.255.0 | 192.168.10.1 | 192.168.10.100 to .150 |
| 20 | AV Control | 192.168.20.0 | 255.255.255.0 | 192.168.20.1 | 192.168.20.200 to .250 |
| 30 | AV Audio | 192.168.30.0 | 255.255.255.0 | 192.168.30.1 | 192.168.30.200 to .250 |
| 40 | AV Telco | 192.168.40.0 | 255.255.255.0 | 192.168.40.1 | 192.168.40.200 to .250 |
| 50 | AV Video | 192.168.50.0 | 255.255.255.0 | 192.168.50.1 | 192.168.50.200 to .250 |
| 100 | Management | 192.168.100.0 | 255.255.255.0 | 192.168.100.1 | None |

## Device addresses

| Device | Model | IP address | VLAN | Switch port | PoE |
|---|---|---|---|---|---|
| Control processor | Crestron CP3 | 192.168.20.10 | 20 | 7 | No |
| Touch panel | Crestron TSW-1060 | 192.168.20.30 | 20 | 16 | PoE+ |
| AV switcher | Crestron HD-MD-400-C-E | 192.168.20.21 | 20 | 17 | No |
| AV switcher | Crestron HD-MD4X1-4K-E | 192.168.20.22 | 20 | 18 | No |
| Display | Sharp PN-LE701 | 192.168.20.61 | 20 | 19 | No |
| PTZ camera | Vaddio RoboSHOT 12 USB | 192.168.20.24 | 20 | XX | XX |
| Ceiling microphone, control | Shure MXA910W | 192.168.20.91 | 20 | 21 | PoE+ |
| Ceiling microphone, audio | Shure MXA910W | 192.168.30.111 | 30 | 5 | PoE+ |
| Audio DSP, control | Q-SYS Core 110f | 192.168.20.81 | 20 | 6 | No |
| Audio DSP, audio | Q-SYS Core 110f | 192.168.30.81 | 30 | 9 | No |
| USB bridge | QSC I/O-USB-Bridge | 192.168.30.63 | 30 | 4 | No |
| Wireless presentation | Barco CSE-200 | 192.168.10.XXX | 10 | 24 | PoE+ |
| Room PC | PC | 192.168.10.XXX | 10 | 12 | No |
| Network switch, management | Cisco SG350X | 192.168.100.2 | 100 | N/A | N/A |
| Network switch, control | Cisco SG350X | 192.168.20.2 | 20 | N/A | N/A |
| Network switch, audio | Cisco SG350X | 192.168.30.2 | 30 | N/A | N/A |
| Network switch, telco | Cisco SG350X | 192.168.40.2 | 40 | N/A | N/A |

## CP3 IP table

| IP ID | Device | Connection | Address | Port |
|---|---|---|---|---|
| 11 | PTZ camera | TCP/IP client | 192.168.20.24 | 23 |
| 40 | Ceiling microphone | TCP/IP client | 192.168.20.91 | 2202 |
| 43 | HD-MD-400-C-E | Crestron device | 192.168.20.21 | Auto |
| 45 | HD-MD4X1-4K-E | Crestron device | 192.168.20.22 | Auto |
| 4A | Display | TCP/IP client | 192.168.20.61 | 10002 |
| 4D | TSW-1060 | Panel connects to CP3 at 192.168.20.10 | 127.0.0.1 | Auto |

The Q-SYS core is reached through the Q-SYS module at 192.168.20.81 and does not use an IP ID.

## Site record

Fill in on site. Store completed values outside this repository.

| Device | Hostname | MAC address | Serial number | Username | Password |
|---|---|---|---|---|---|
| CP3 | XXX-CP3-01 | XX:XX:XX:XX:XX:XX | XXXXXXXXXXXX | XXXXXXXX | XXXXXXXX |
| TSW-1060 | XXX-TSW-01 | XX:XX:XX:XX:XX:XX | XXXXXXXXXXXX | XXXXXXXX | XXXXXXXX |
| HD-MD-400-C-E | XXX-MD400-01 | XX:XX:XX:XX:XX:XX | XXXXXXXXXXXX | XXXXXXXX | XXXXXXXX |
| HD-MD4X1-4K-E | XXX-MD4X1-01 | XX:XX:XX:XX:XX:XX | XXXXXXXXXXXX | XXXXXXXX | XXXXXXXX |
| Display | XXX-DISP-01 | XX:XX:XX:XX:XX:XX | XXXXXXXXXXXX | XXXXXXXX | XXXXXXXX |
| PTZ camera | XXX-CAM-01 | XX:XX:XX:XX:XX:XX | XXXXXXXXXXXX | XXXXXXXX | XXXXXXXX |
| Ceiling microphone | XXX-MIC-01 | XX:XX:XX:XX:XX:XX | XXXXXXXXXXXX | XXXXXXXX | XXXXXXXX |
| Q-SYS Core 110f | XXX-CORE-01 | XX:XX:XX:XX:XX:XX | XXXXXXXXXXXX | XXXXXXXX | XXXXXXXX |
| USB bridge | XXX-USB-01 | XX:XX:XX:XX:XX:XX | XXXXXXXXXXXX | XXXXXXXX | XXXXXXXX |
| Wireless presentation | XXX-BARCO-01 | XX:XX:XX:XX:XX:XX | XXXXXXXXXXXX | XXXXXXXX | XXXXXXXX |
| Network switch | XXX-SW-01 | XX:XX:XX:XX:XX:XX | XXXXXXXXXXXX | XXXXXXXX | XXXXXXXX |

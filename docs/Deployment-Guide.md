# Deployment Guide

Work through these steps in order. Addresses are in the [Network and IP Table](Network-and-IP-Table.md).

## Software

| Tool | Version | Use |
|---|---|---|
| SIMPL Windows | 4.28 or later | Compile the program |
| Crestron Toolbox | Current | Address and load devices |
| VT Pro-e | 6.2 or later | Touch panel project |
| Q-SYS Designer | 9.1.2 or later | DSP design |

## 1. Network

1. Create VLANs 10, 20, 30, 40, 50 and 100 on the switch.
2. Assign each switch port to its VLAN.
3. Enable PoE+ on the panel, microphone and wireless presentation ports.
4. Set up QoS for Dante on the audio VLAN.
5. Connect a laptop to the control VLAN and confirm it reaches the gateway at 192.168.20.1.

## 2. Addressing

Set a static IP, mask and gateway on each device.

| Device | IP address | Setting |
|---|---|---|
| CP3 | 192.168.20.10 | Hostname `XXX-CP3-01` |
| TSW-1060 | 192.168.20.30 | Control system 192.168.20.10, IP ID 4D |
| HD-MD-400-C-E | 192.168.20.21 | Control system 192.168.20.10, IP ID 43 |
| HD-MD4X1-4K-E | 192.168.20.22 | Control system 192.168.20.10, IP ID 45 |
| Display | 192.168.20.61 | Enable LAN control, port 10002 |
| PTZ camera | 192.168.20.24 | Enable Telnet control, port 23 |
| Ceiling microphone | 192.168.20.91 | Control port 2202 |
| Q-SYS Core 110f | 192.168.20.81 | LAN A control, LAN B audio |

Record usernames and passwords in a secure location, not in this repository.

## 3. Q-SYS

1. Open the design in Q-SYS Designer and set the core to Core 110f.
2. Confirm every name in the [Crestron to Q-SYS Map](Crestron-to-QSYS-Map.md) exists as a Named Control.
3. Enter SIP details in the softphone: server `XXX.XXX.XXX.XXX`, user `XXXXXXXX`, password `XXXXXXXX`.
4. Subscribe the ceiling microphone over Dante.
5. Deploy the design to the core and run it.

## 4. Control processor

1. Open `BRD-1001_Boardroom_slt01.smw` in SIMPL Windows and compile.
2. In Toolbox, load the `.lpz` to program slot 1.
3. Confirm the IP table in Toolbox matches the [CP3 IP table](Network-and-IP-Table.md#cp3-ip-table).
4. Restart the program and wait for the startup sequence to finish.

## 5. Touch panel

1. Load the `.vtz` to the TSW-1060 with Toolbox.
2. Confirm the panel shows as online in the CP3 IP table.
3. Confirm the Home page appears.

## 6. Device checks

| Device | Check |
|---|---|
| Q-SYS core | Core reports connected in the program |
| HD-MD switchers | Both online in the IP table |
| Display | Powers on and changes input |
| Camera | Moves and recalls presets |
| Ceiling microphone | Mute LED follows Privacy Mute |
| Bluetooth interface | Status shows on panel, COM 2 at 9600 8N1 |
| Cable TV | Channel changes by IR |

## 7. Room test

1. Select each source and confirm picture and sound.
2. Adjust each audio level and mute.
3. Place and end a phone call.
4. Start a web call on the room PC and confirm camera, microphone and speakers.
5. Pair a phone by Bluetooth and play audio.
6. Press Power and confirm the room shuts down.

## 8. Handover

1. Back up the program, panel and Q-SYS files.
2. Complete the site record in the [Network and IP Table](Network-and-IP-Table.md#site-record).
3. Change all default passwords.

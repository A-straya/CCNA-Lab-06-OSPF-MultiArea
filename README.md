

<h1 align="center"> CCNA Lab 06</h1>

<h3 align="center">
Enterprise OSPF Multi-Area Routing
</h3>

<p align="center">

<img src="https://img.shields.io/badge/Cisco-Packet%20Tracer-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white">

<img src="https://img.shields.io/badge/Routing-OSPF-0052CC?style=for-the-badge">

<img src="https://img.shields.io/badge/Level-Intermediate-00C853?style=for-the-badge">

<img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge">

</p>

---

#  Overview

This project simulates an enterprise network using **OSPF (Open Shortest Path First)** to provide dynamic routing between multiple departments.

The objective is to replace static routing with a scalable routing protocol capable of automatically discovering networks, exchanging routing information, and adapting to topology changes.

This lab reflects how medium and large organizations design their internal routing infrastructure.

---

#  Scenario

ABC Technologies has expanded its infrastructure into multiple departments connected through three routers.

As the network administrator, your responsibility is to deploy OSPF to ensure reliable communication between all network segments while maintaining a scalable routing architecture.

---

#  Objectives

- Configure router hostnames
- Assign IPv4 addresses
- Configure OSPF Process ID
- Configure Router IDs
- Advertise connected networks
- Establish OSPF neighbor relationships
- Verify routing tables
- Test end-to-end connectivity
- Troubleshoot routing issues

---

#  Devices

| Device | Quantity |
|---------|---------:|
| Cisco Routers | 3 |
| Cisco Switches | 3 |
| PCs | 6 |

---

#  Planned Topology

```
                    AREA 0

          PC1             PC2
           |               |
          SW1-------------SW2
            |             |
            |             |
           R1============R2
                          |
                          |
                     Serial Link
                          |
                         R3
                          |
                         SW3
                       /     \
                    PC5      PC6

                    AREA 1
```

---

#  IP Addressing Plan

| Device | Interface | IP Address |
|---------|-----------|----------------|
| R1 | G0/0 | 192.168.10.1 /24 |
| R1 | G0/1 | 10.0.12.1 /30 |
| R2 | G0/0 | 10.0.12.2 /30 |
| R2 | G0/1 | 192.168.20.1 /24 |
| R2 | G0/2 | 10.0.23.1 /30 |
| R3 | G0/0 | 10.0.23.2 /30 |
| R3 | G0/1 | 192.168.30.1 /24 |

---

#  Configuration Tasks

- Configure all router interfaces
- Configure router hostnames
- Configure Router IDs
- Enable OSPF
- Advertise connected networks
- Verify neighbor relationships
- Verify routing tables
- Test connectivity using Ping and Traceroute

---

#  Verification Commands

```bash
show ip route

show ip ospf neighbor

show ip ospf interface

show ip protocols

show ip ospf database

ping

traceroute
```

---

#  Expected Results

- All routers establish OSPF neighbor relationships.
- Remote networks appear automatically in the routing table.
- Every PC can communicate successfully with all other networks.
- End-to-end connectivity is verified.
- Dynamic routes update automatically if the topology changes.

---

#  Skills Practiced

- Dynamic Routing
- OSPF Configuration
- Cisco IOS CLI
- Enterprise Network Design
- Routing Verification
- Network Troubleshooting

---

#  Real-World Applications

OSPF is one of the most widely deployed Interior Gateway Protocols (IGPs) and is commonly used in:

- Enterprise Networks
- Universities
- Hospitals
- Financial Institutions
- Government Organizations
- Data Centers

---

#  Future Improvements

- OSPF Authentication
- Stub Areas
- Totally Stubby Areas
- NSSA
- Route Summarization
- IPv6 OSPF
- Redundant Links

---

#  Repository Structure

```
CCNA-Lab-06-OSPF-MultiArea/

│

├── README.md

├── CCNA-Lab-06.pkt

└── images/
```

---

#  Author

### Aya Hathout

**Network & Cybersecurity Student**

Building practical networking and cybersecurity projects while documenting my learning journey through hands-on Cisco labs.

---

<p align="center">

⭐ If you enjoyed this project, consider giving it a star!

</p>

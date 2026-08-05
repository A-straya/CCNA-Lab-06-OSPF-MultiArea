

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

ABC Technologies has expanded its infrastructure into three departments:

-  Administration
-  Sales
-  IT Department

Each department operates on its own LAN while maintaining secure communication with the rest of the organization.

As the network administrator, your task is to deploy OSPF Multi-Area Routing to replace static routes, optimize routing efficiency, and ensure full connectivity across the enterprise network.

---

# 🎯 Objectives

- Configure router hostnames
- Configure IPv4 addressing
- Configure OSPF Process ID
- Configure Router IDs
- Configure OSPF Areas
- Advertise connected networks
- Verify neighbor relationships
- Verify routing tables
- Test end-to-end connectivity
- Troubleshoot routing issues

---

#  Devices

| Device | Quantity |
|---------|---------:|
| Cisco 2911 Routers | 3 |
| Cisco 2960 Switches | 3 |
| PCs | 6 |

---

#  Enterprise Topology

```
                  AREA 0

        Administration LAN

      PC1              PC2
       |                |
      +------------------+
      |       SW1        |
      +------------------+
             |
             |
            R1
             |
=============|================
             |
            R2
             |
      +------------------+
      |       SW2        |
      +------------------+
       |                |
      PC3              PC4

          Sales LAN

=============|================

            R3
             |
      +------------------+
      |       SW3        |
      +------------------+
       |                |
      PC5              PC6

          IT Department

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

#  OSPF Area Design

| Area | Devices |
|------|---------|
| Area 0 | R1 ↔ R2 |
| Area 1 | R2 ↔ R3 |

**R2 acts as the Area Border Router (ABR), connecting Area 0 and Area 1.**

---

#  Configuration Tasks

- Configure router interfaces
- Configure hostnames
- Configure Router IDs
- Enable OSPF
- Assign interfaces to the correct OSPF areas
- Advertise connected networks
- Verify neighbor relationships
- Verify routing tables
- Test end-to-end connectivity

---

#  Verification Commands

```bash
show ip route

show ip ospf neighbor

show ip ospf database

show ip protocols

show ip ospf interface

ping

traceroute
```

---

#  Expected Results

- OSPF neighbor relationships are successfully established.
- R2 functions as the Area Border Router (ABR).
- Dynamic routes appear in every routing table.
- All six PCs communicate successfully.
- The enterprise network converges automatically after topology changes.

---

#  Skills Practiced

- Enterprise Network Design
- Dynamic Routing
- OSPF Multi-Area Configuration
- Area Border Router (ABR)
- Cisco IOS CLI
- Routing Verification
- Network Troubleshooting

---

#  Real-World Applications

OSPF Multi-Area is commonly deployed in:

- Enterprise Networks
- Universities
- Hospitals
- Financial Institutions
- Government Organizations
- Large Corporate Campuses

---

#  Future Improvements

- OSPF Authentication
- Stub Areas
- NSSA
- Route Summarization
- IPv6 OSPF
- Redundant Links
- Dual ISP Connectivity

---

#  Repository Structure

```
CCNA-Lab-06-OSPF-MultiArea/

├── README.md
├── CCNA-Lab-06.pkt
└── images/
```

---


</p>
#  Author

### Aya Hathout

**Network & Cybersecurity Student**

Building practical networking and cybersecurity projects while documenting my learning journey through hands-on Cisco labs.

---

<p align="center">

⭐ If you enjoyed this project, consider giving it a star!

</p>

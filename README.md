<h1 align="center">CCNA Lab 06</h1>

<h3 align="center">
Enterprise OSPF Routing
</h3>

<p align="center">

<img src="https://img.shields.io/badge/Cisco-Packet%20Tracer-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white">
<img src="https://img.shields.io/badge/Routing-OSPF-blue?style=for-the-badge">
<img src="https://img.shields.io/badge/Level-Intermediate-00C853?style=for-the-badge">
<img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge">

</p>

---

#  Overview

This project demonstrates the deployment of **Open Shortest Path First (OSPF)** in a small enterprise network.

The lab replaces static routing with a dynamic routing protocol, allowing routers to automatically exchange routing information and maintain connectivity between different departments.

This project focuses on practical enterprise routing concepts commonly found in real-world Cisco environments.

---

#  Scenario

ABC Technologies has expanded its infrastructure into two departments connected through dedicated routers.

As the network administrator, your objective is to deploy OSPF to create a scalable and reliable routing environment while ensuring seamless communication across the enterprise network.

---

#  Objectives

- Configure router hostnames
- Configure IPv4 addressing
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
| Cisco 1941 Routers | 2 |
| Cisco 2960 Switches | 2 |
| PCs | 4 |

---

#  Enterprise Topology

```

            Administration Department

      PC1                    PC2
       |                      |
+-------------------------------+
|             SW1               |
+-------------------------------+
               |
            Gig0/0
               |
              R1
            Gig0/1
               |
====================================
          10.0.12.0 /30
====================================
               |
            Gig0/0
              R2
            Gig0/1
               |
+-------------------------------+
|             SW2               |
+-------------------------------+
       |                      |
      PC3                    PC4

             IT Department

```

---

#  IP Addressing Plan

| Device | Interface | IP Address |
|---------|-----------|------------|
| R1 | G0/0 | 192.168.10.1 /24 |
| R1 | G0/1 | 10.0.12.1 /30 |
| R2 | G0/0 | 10.0.12.2 /30 |
| R2 | G0/1 | 192.168.20.1 /24 |

---

#  PC Addressing

| Device | IP Address | Gateway |
|---------|------------|----------|
| PC1 | 192.168.10.10 | 192.168.10.1 |
| PC2 | 192.168.10.20 | 192.168.10.1 |
| PC3 | 192.168.20.10 | 192.168.20.1 |
| PC4 | 192.168.20.20 | 192.168.20.1 |

---

#  Configuration Tasks

- Configure router interfaces
- Configure hostnames
- Configure IPv4 addressing
- Enable OSPF
- Configure Router IDs
- Advertise connected networks
- Verify OSPF neighbors
- Verify routing tables
- Test end-to-end connectivity

---

#  Verification Commands

```bash
show ip interface brief

show ip route

show ip ospf neighbor

show ip protocols

show ip ospf interface

ping

traceroute
```

---

#  Expected Results

- OSPF neighbor relationship is successfully established.
- Dynamic routes appear in both routing tables.
- All PCs communicate successfully across departments.
- The routing table updates automatically after topology changes.

---

#  Skills Practiced

- Dynamic Routing
- OSPF Configuration
- Cisco IOS CLI
- Enterprise Routing
- Network Verification
- Network Troubleshooting

---

#  Real-World Applications

The concepts implemented in this lab are widely used in:

- Enterprise Networks
- Universities
- Hospitals
- Financial Institutions
- Government Organizations
- Corporate Campuses

---

#  Future Improvements

- OSPF Authentication
- Route Summarization
- Default Route Advertisement
- Passive Interfaces
- IPv6 OSPF
- Multi-Area OSPF

---

#  Repository Structure

```
CCNA-Lab-06-OSPF/

│

├── README.md

├── CCNA-Lab-06-OSPF.pkt

└── images/
```

---

#  Author

### Aya Hathout

**Network & Cybersecurity Student**



<p align="center">

⭐ If you found this project useful, consider giving it a star!

</p>


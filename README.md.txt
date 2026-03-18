# Small Office Network Design

## Objective

This project simulates a small office network with two departments (Admin and Staff). The goal is to design a structured network using separate subnets and enable communication between them using a router.

---

## Network Topology

(Add your topology image here)

---

## IP Addressing Scheme

| Device | Interface | IP Address  | Subnet Mask   | Default Gateway |
| ------ | --------- | ----------- | ------------- | --------------- |
| R1     | G0/0      | 192.168.1.1 | 255.255.255.0 | N/A             |
| R1     | G0/1      | 192.168.2.1 | 255.255.255.0 | N/A             |
| PC1    | NIC       | 192.168.1.2 | 255.255.255.0 | 192.168.1.1     |
| PC2    | NIC       | 192.168.1.3 | 255.255.255.0 | 192.168.1.1     |
| PC3    | NIC       | 192.168.2.2 | 255.255.255.0 | 192.168.2.1     |
| PC4    | NIC       | 192.168.2.3 | 255.255.255.0 | 192.168.2.1     |

---

## Configuration Summary

* Created two separate subnets to represent Admin and Staff departments
* Configured router interfaces to act as default gateways for each subnet
* Assigned IP addresses manually to all end devices
* Ensured proper connectivity between devices within and across subnets

---

## Testing & Verification

* Verified connectivity within each subnet using ping tests
* Verified inter-network communication by pinging devices across subnets
* Confirmed router interface status using `show ip interface brief`

---

## Design Decisions

Two separate subnets were used to simulate departmental separation within an organization. This improves network organization, scalability, and security by limiting broadcast domains and allowing controlled communication through a router.

---

## Key Learnings

* Understanding how routers enable communication between different networks
* Importance of default gateways in inter-network communication
* Role of subnetting in organizing and scaling networks

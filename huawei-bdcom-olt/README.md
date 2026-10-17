# ISP Core Switching, Transit Routing, and OLT VLAN Architecture

**Author:** Nahid Hossen Munna  
**Experience:** 11 Years in ISP Networking  
**Focus:** Huawei Switching, MikroTik Routing, NAT, Transit IP, Access Routers, and OLT VLANs

## Project Overview

Practical experience operating an ISP network built around three Huawei switches, MikroTik routing, multiple access routers, and OLT infrastructure.

Each Huawei switch has 6 × 100G ports and 48 × 10G ports. The switching infrastructure supports high-capacity uplinks and connectivity between network components.

The network uses transit IP addressing between routing devices, NAT for applicable traffic flows, and VLAN-based separation for OLT PON services.

## Network Infrastructure

### 1. Huawei Core / Distribution Switching

- Operate three Huawei switches, each equipped with 6 × 100G and 48 × 10G ports.
- Use high-speed interfaces for inter-switch and network uplinks according to the network design.
- Connect routing and access infrastructure through designated interfaces.
- Monitor interface status, traffic utilization, optical levels, and errors.
- Troubleshoot uplink instability and physical-layer issues.

### 2. MikroTik Routing and NAT

- Use MikroTik routers for ISP routing and traffic forwarding.
- Configure and manage transit IP connectivity between network devices.
- Apply NAT where required by the network design.
- Connect access routers to the upstream routing infrastructure.
- Troubleshoot routing, reachability, packet loss, and traffic-path issues.

### 3. Access Router Connectivity

- Maintain connectivity between the core/distribution layer and access routers.
- Use appropriate IP addressing and routing between network segments.
- Verify connectivity and traffic forwarding across the intended paths.
- Investigate access-network problems using routing information and interface counters.

### 4. OLT and PON VLAN Management

- Operate OLT connectivity within the ISP access network.
- Use VLANs to separate and transport PON service traffic.
- Maintain the intended VLAN mapping between OLT uplinks and upstream switching infrastructure.
- Troubleshoot VLAN tagging, trunk connectivity, and subscriber service reachability.
- Verify VLAN configuration and traffic flow across the relevant network interfaces.

## Simplified Network Architecture

```text
                Upstream / Transit Networks
                           |
                    MikroTik Routing
                      /          \
                 NAT / Routing   Transit IP
                       \          /
                  Huawei Switch Layer
                  3 × Huawei Switches
                6 × 100G + 48 × 10G each
                           |
                 Access / Distribution
                     Router Layer
                           |
                     OLT Uplinks
                           |
                    VLAN-Based PON
                           |
                     Subscriber ONUs
```

*This is a conceptual overview, not an exact physical topology. Actual connections and traffic paths depend on the deployed network design.*

## Operational Responsibilities

- Monitor high-capacity switch interfaces and uplinks.
- Maintain routing and transit connectivity between network devices.
- Troubleshoot NAT and reachability issues.
- Maintain VLAN separation for OLT/PON traffic.
- Investigate link flapping, optical signal issues, packet loss, and VLAN mismatches.
- Verify connectivity after changes and monitor for recurring faults.

## Evidence to Add

Add sanitized screenshots or diagrams showing:

- Huawei switch interface status
- 100G and 10G interface utilization
- MikroTik transit IP and routing overview
- NAT configuration with sensitive details removed
- OLT uplink and VLAN configuration
- PON VLAN mapping diagram

## Security

Do not publish production passwords, authentication keys, customer IP/MAC addresses, public management IPs, complete live configurations, or confidential network topology.

Use redacted screenshots and illustrative configuration examples.

## Outcome

This project documents hands-on ISP infrastructure experience across high-capacity switching, MikroTik routing, transit IP connectivity, NAT, access routers, and VLAN-based OLT/PON traffic transport.

*The architecture and responsibilities described here reflect practical experience; exact designs vary by deployment.*


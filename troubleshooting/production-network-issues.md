# ISP Network Troubleshooting — Real-World Case Studies

**Author:** Nahid Hossen Munna  
**Experience:** 11 Years in ISP Networking  
**Focus:** Network Troubleshooting, Routing, Switching, OLT Connectivity, and ISP Operations

This document describes three network troubleshooting cases based on my practical ISP operations experience. The findings and recommendations reflect the environments I worked with; results may vary with hardware, firmware, transceiver compatibility, temperature, and network design.

---

## Case Study 01: Huawei Switch Port Flapping with a Third-Party 100G Transceiver

### Problem

A Huawei switch uplink experienced intermittent link flapping while a third-party 100G optical transceiver was installed. In my observed environment, the issue appeared when the transceiver temperature increased, particularly around 45°C.

Link instability can interrupt traffic and affect services that depend on the uplink.

### Investigation

- Checked interface status and link-up/link-down events.
- Reviewed transceiver temperature and available optical diagnostic readings.
- Considered transceiver compatibility and the switch's support for the installed module.
- Correlated the link instability with operating conditions.

### Root Cause — Suspected

The third-party transceiver's compatibility or thermal behavior was a possible contributing factor. The observed temperature correlation alone does not prove the exact cause; further testing with a known-good compatible module is needed to confirm it.

### Solution

- Recommended using a Huawei-supported or otherwise verified-compatible 100G transceiver.
- Checked optical transmit/receive levels and module temperature.
- Monitored interface status and error counters after changing the module.
- Recommended validating compatibility before deploying replacement optics in production.

### Verification

Confirm that the interface remains stable under normal traffic and operating temperature. Review link events, CRC/error counters, optical levels, and temperature over an appropriate monitoring period.

**Key Learning:** Transceiver compatibility, optical health, and thermal conditions should all be considered when troubleshooting intermittent high-speed uplinks.

---

## Case Study 02: BDCOM OLT to MikroTik 10G Link Instability

### Problem

A 10G connection between a BDCOM OLT and a MikroTik router experienced intermittent link-up/link-down events. This created a risk of service interruption for subscribers using the affected path.

### Investigation

- Checked link status on both the OLT and MikroTik.
- Inspected the physical connection and available interface logs.
- Considered DAC cable compatibility, port behavior, and transceiver support.
- Reviewed interface errors and link stability.

### Root Cause — Under Investigation

The instability was associated with the DAC-based connection in the observed environment. Cable compatibility, port compatibility, physical connection quality, or hardware behavior can also cause similar symptoms. The exact cause should be confirmed using interface logs and controlled testing.

### Solution

My recommended alternative in this environment was to test a compatible multimode fiber connection using supported 10G SFP+ optics instead of the DAC cable.

Implementation checklist:

1. Confirm that both devices support the selected 10G SFP+ optics.
2. Verify fiber type, connector type, and the required optical reach.
3. Check transmit/receive optical power after installation.
4. Monitor link status, interface errors, and service stability.
5. Keep the original connection available for rollback until the replacement is verified.

### Verification

Confirm that the link remains stable and that interface errors and subscriber service interruptions do not recur during the monitoring period.

**Key Learning:** DAC and optical connections both have valid use cases. Select the connection type based on device compatibility, distance, optical requirements, and measured stability.

---

## Case Study 03: MikroTik RouterOS PPPoE Connectivity and Packet Loss

### Problem

During ISP operations, I observed PPPoE connectivity issues and packet loss in environments running MikroTik RouterOS versions 7.14.5 and 7.19.7.

These symptoms can have multiple causes, including software behavior, hardware resource limits, configuration, congestion, physical errors, or upstream problems. The RouterOS version alone should not be assumed to be the root cause without testing.

### Investigation

- Checked PPPoE session stability and router resource utilization.
- Reviewed interface errors, CPU load, memory use, and traffic levels.
- Checked packet loss across relevant network segments to isolate where loss occurred.
- Compared behavior under the affected RouterOS builds and available known-good configurations.
- Considered server hardware capacity where PPPoE workloads required additional resources.

### Solution and Recommendations

Based on my operational experience:

- Evaluate suitable Dell server hardware where a server-based routing or PPPoE deployment fits the network design.
- Test RouterOS releases in a lab or controlled maintenance window before production rollout.
- In my environment, RouterOS 7.16.5 and 7.19.6 were versions I considered as alternatives when newer builds showed issues.
- For RouterOS v6 environments, 6.49.5 was another version I used as a reference point.
- I found RouterOS 7.19.6 suitable for my NAT use case, but this should not be treated as a universal performance guarantee.

Before changing versions, verify hardware and architecture support, configuration compatibility, release notes, backup/rollback readiness, and the ability to reproduce the issue.

### Verification

After a change:

1. Monitor PPPoE session drops and reconnections.
2. Test packet loss across the local network and upstream paths.
3. Review CPU, memory, interface errors, and throughput under representative load.
4. Compare before-and-after results over a suitable observation period.
5. Keep a tested rollback plan.

**Key Learning:** RouterOS selection should be based on reproducible testing, workload, hardware compatibility, and stability—not version numbers alone.

---

## Standard Troubleshooting Methodology

My general troubleshooting workflow:

1. **Identify:** Define the symptoms, affected services, and time of occurrence.
2. **Collect evidence:** Review logs, interface counters, optical readings, resource usage, and monitoring graphs.
3. **Isolate:** Check the physical layer, device, configuration, and upstream path systematically.
4. **Change carefully:** Apply one controlled change at a time and prepare rollback.
5. **Verify:** Confirm service restoration and monitor for recurrence.
6. **Document:** Record the issue, evidence, corrective action, and outcome.

## Portfolio Evidence and Security

Screenshots, configuration snippets, and monitoring graphs can be added as supporting evidence after removing sensitive information.

Do not publish production passwords, SNMP communities, API tokens, customer identifiers, subscriber IP/MAC details, or confidential network topology.

**Note:** These case studies describe practical observations and recommendations from my working environment. They are not guarantees that the same symptoms have the same root cause in every network.

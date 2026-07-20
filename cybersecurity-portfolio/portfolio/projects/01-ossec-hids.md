# Host-Based Intrusion Detection with OSSEC

**Focus:** Detection engineering · HIDS · Log analysis · File integrity monitoring
**Environment:** Isolated virtual lab (VirtualBox)

---

## Objective

Deploy a Host-Based Intrusion Detection System (HIDS) and prove it can detect a real intrusion. The goal was not to attack — it was to build the detection capability and verify, from the defender's side, that malicious activity is caught, logged, and alerted on.

## Why HIDS

A HIDS runs *on the host itself* and watches what actually happens on that machine: file changes, user activity, and system logs. This is different from a network-based system (NIDS), which watches traffic. A HIDS gives detailed visibility into a specific system and provides early warning of malicious activity — log analysis, file integrity monitoring, rootkit detection, and centralised alerting through agents.

## Lab setup

| Role | System |
|---|---|
| OSSEC Manager (server) | Ubuntu Server |
| Monitored endpoint | Windows (OSSEC agent) |
| Attacker | Kali Linux |

The Ubuntu manager collected and analysed events from the Windows agent, giving a single place to see alerts from the monitored host.

## What I did

1. **Deployed the OSSEC manager** on Ubuntu and confirmed the service was active and healthy.
2. **Registered and connected a Windows agent**, verifying it appeared as active on the manager and was reporting in.
3. **Ran controlled activity from Kali** against the monitored host to generate detectable events.
4. **Verified detection** on the manager side for:
   - Intrusion / exploitation activity
   - Creation of a new user account
   - Enabling of remote access (RDP)
   - File integrity changes on the monitored system
5. **Reviewed the rules** responsible for each alert to understand *why* it fired, not just *that* it fired.

## Results

Every action taken against the monitored host surfaced as a clear alert in the OSSEC logs on the central manager. The new user account, the RDP change, and file modifications were all recorded and flagged.

## Key takeaways

- The value of a HIDS is in the **centralised, correlated view** — one console showing what happened on the host.
- **File Integrity Monitoring (FIM)** is powerful: unauthorised changes to important files become visible even if other controls are bypassed.
- Reading the detection rules taught me more than the installation did. Understanding rule logic is the difference between running a tool and doing detection engineering.

## Skills demonstrated
HIDS deployment · agent management · log analysis · file integrity monitoring · detection-rule interpretation

## Evidence
> Screenshots: `assets/ossec-*.png` — manager status, active agent list, and triggered alerts. *(Add your screenshots and reference them here.)*

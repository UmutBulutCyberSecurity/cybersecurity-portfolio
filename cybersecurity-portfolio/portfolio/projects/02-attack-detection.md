# Attack Detection & Log Analysis (Metasploitable 2)

**Focus:** Incident investigation · Authentication-log analysis · Brute-force detection
**Environment:** Isolated virtual lab — intentionally vulnerable target (Metasploitable 2)

---

## Objective

Take a common, real-world attack — access via weak or default credentials — and answer the question that actually matters for a SOC analyst: **if someone broke in this way, could I detect it, and what would the evidence look like?**

## Background

The most common breaches are often the least sophisticated. Default and reused credentials open more doors than clever exploits. This lab reproduces that scenario and then investigates it from the defender's side.

## What I did

**Attacker side (to create something to detect):**
1. Enumerated the network with **Nmap** and mapped which hosts and services were exposed.
2. Identified a host running many services, including SSH and a database port.
3. Tested exposed services for weak/default credentials and gained a shell using a default account that had never been changed.

**Defender side (the real point):**
4. Investigated the intrusion by examining system evidence, ranked by how much I could trust it:
   - **Authentication logs** first, because the *system* writes them, not the user. These showed the successful login and — just before it — a burst of failed attempts from a single source, the classic signature of a brute force that succeeded.
   - **Login/session records** (`last`, `lastlog`) to confirm who accessed the host and when.
   - **Command history and file access times** treated as *supporting* evidence only, since an attacker can alter them.
5. Mapped this back to detection: a HIDS/SIEM watching the auth log flags the "multiple failures then success" pattern automatically.

## Key takeaways

- **Rank evidence by who controls it.** System-written logs are trustworthy; user-writable artifacts are not. Knowing the order to look in is a core investigation skill.
- The same login looked like a *win* from the attacker's side and **loud and obvious** from the defender's side.
- Detection isn't one magic log — it's knowing which signals to trust and letting monitoring catch what a human would miss.

## Skills demonstrated
Network enumeration · credential-attack recognition · authentication-log analysis · evidence reliability ranking · detection mapping

## Evidence
> Screenshots: `assets/detection-*.png` — Nmap output, log evidence of the failed-to-success pattern. *(Redact anything sensitive; add and reference your screenshots.)*

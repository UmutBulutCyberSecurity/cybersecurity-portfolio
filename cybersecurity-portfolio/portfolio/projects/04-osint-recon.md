# OSINT & Passive Reconnaissance

**Focus:** OSINT · Attack-surface mapping · Threat intelligence
**Environment:** Passive collection using publicly available data only

---

## Objective

Understand how much can be learned about an organisation's security posture **without touching a single one of its systems** — the reconnaissance phase that precedes any real attack, and the same view defenders need to reduce their exposure.

## Rules of engagement

Passive only. Publicly available information, nothing that scans or touches the target, nothing intrusive. Just what is already visible to anyone on the internet.

## What I did

1. Used **Shodan** and **OSINT techniques** to examine an organisation's internet-facing footprint.
2. Mapped exposed hosts and services from public data.
3. Analysed the results for security-relevant patterns — not just individual findings.

## The interesting finding

The most useful result wasn't a vulnerability — it was an **architecture pattern**. A large number of separate public services, belonging to many different parts of the same organisation, resolved back to a **single shared host**.

On the surface that looks efficient. From a security and resilience view it's a **concentration risk**: one misconfiguration, outage, or compromise at that shared point can affect a wide range of unrelated services at once.

## Key takeaways

- OSINT isn't about breaking in — it's about **seeing the shape of an infrastructure from the outside**, the way an attacker does before choosing a target.
- The valuable insight was **structural**, which is what separates analysis from scanning.
- **Reconnaissance is the first phase of an attack — it should also be the first phase of a defence.**

## Skills demonstrated
Passive reconnaissance · Shodan · OSINT Framework · attack-surface mapping · risk interpretation

## Evidence
> Screenshots / notes: `assets/osint-*.png`. *(Public data only; add and reference your findings.)*

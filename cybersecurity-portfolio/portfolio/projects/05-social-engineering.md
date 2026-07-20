# Social Engineering / Phishing Simulation

**Focus:** Human-layer security · Phishing · Security awareness
**Environment:** Isolated lab, authorised targets only

---

## Objective

Study *why* phishing works — not the tooling, but the psychology — and identify the defences that actually reduce the risk. Most phishing attacks don't break software; they break trust.

## What I did

Ran a controlled social engineering exercise in an isolated lab. The simulated message was built to feel routine and urgent at the same time: it appeared to come from an internal IT team, carried a familiar "Status Report" subject, and was marked high priority. That combination — a trusted authority, a familiar routine, and a sense of urgency — is what makes people click.

*(This writeup deliberately describes the technique at a conceptual level rather than as a reusable how-to.)*

## Key takeaways

- The technical part was the easy part. The real weapon was the **framing** — authority, familiarity, and urgency — not an advanced exploit.
- The **last line of defence is a person** deciding whether to click, which is why security awareness is a core control, not a nice-to-have.

## Defences that actually help

| Control | Why it matters |
|---|---|
| Email authentication (SPF, DKIM, DMARC) | Makes sender spoofing harder |
| Attachment sandboxing | Detonates suspicious attachments safely |
| Security-awareness training | Teaches people to slow down under pressure |
| Reporting culture | Turns every employee into a sensor |

## Skills demonstrated
Social-engineering awareness · phishing analysis · email-security controls · defensive recommendations

## Evidence
> Screenshots: `assets/phishing-*.png`. *(Add your lab screenshots; keep framing defensive.)*

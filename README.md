# copilot-customer-ops

## What it does

Customer Case Assistant: summarises cases, finds missing information and drafts professional customer responses.

Part of the **department-copilots** suite: local-only copilots where the employee provides the input, Claude analyses it on the machine, and the employee decides what to do. No CRM, NMS, email or system integrations.

## Install

```bash
claude plugin marketplace add sara-hamza/department-copilots
```

```bash
claude plugin install customer-ops@department-copilots
```

Paste the complaint, the call notes or the email thread and get back a structured case summary, the list of what is still missing, a customer-friendly reply you can send, or a plain-English translation of the technical note.

| Command | Use when |
|---|---|
| `/customer-ops:case-summary <paste>` | New or escalated case. Issue, timeline, sentiment, what has been done, what is missing, recommended response, internal next step |
| `/customer-ops:missing-info <paste>` | Only want the checklist of what you still need before the case can progress |
| `/customer-ops:draft-reply <paste>` | Draft the customer reply (acknowledge, what we found, what happens next and when, how to reach us) with INTERNAL NOTES kept separate |
| `/customer-ops:plain-english <paste technical text>` | Translate a NOC or field note into customer wording, side by side |

We are a wholesale network operator: the resident's retail relationship is with their RSP. Every draft respects that line (what we can say, what the RSP must handle).

Requires `copilot-common` (privacy rules, document-reader for emailed PDFs, screenshot-reader for screenshots of portals or SMS threads, writing-helper for the customer tone table).

Reference knowledge lives in `skills/customer-case-assistant/references/`. Response-time commitments, escalation contacts and the exact wholesale wording are sensible defaults marked `CUSTOMISE`.

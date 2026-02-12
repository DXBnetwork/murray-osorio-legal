---
description: Generate contextual briefings for immigration law work — daily summary, case research, or urgent matter response
argument-hint: "[daily | case <query> | urgent]"
---

# /brief -- Immigration Law Team Briefing

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Generate contextual briefings for immigration law practice. Supports three modes: daily brief, case research brief, and urgent matter brief.

**Important**: This command assists with immigration law workflows but does not provide legal advice. Briefings should be reviewed by qualified immigration attorneys before being relied upon.

## Invocation

```
/brief daily              # Morning brief of immigration-relevant items
/brief case [query]       # Research brief on a specific immigration issue or case type
/brief urgent [topic]     # Rapid brief on an urgent immigration matter
```

If no mode is specified, ask the user which type of brief they need.

## Modes

---

### Daily Brief

A morning summary of everything an immigration law team member needs to know to start their day.

#### Sources to Scan

Check each connected source for immigration-relevant items:

**Email (if connected):**
- New client intake requests
- USCIS notices (RFEs, NOIDs, approval notices, interview notices)
- Immigration court hearing notices
- Client documentation submissions
- Responses from USCIS or immigration courts
- Visa bulletin updates
- Policy change alerts from AILA or USCIS
- Urgent client communications

**Calendar (if connected):**
- Today's client consultations
- Immigration court hearings or check-ins
- USCIS interviews requiring attorney attendance
- Upcoming filing deadlines (petition deadlines, response deadlines)
- Biometrics appointments
- Team case review meetings

**Chat (if connected):**
- Overnight messages in case management channels
- Direct messages from clients or team members
- Mentions of urgent matters (deportation, ICE, detention, RFE, NOID)
- Case status updates or escalations

**Case Management System (if connected):**
- Cases awaiting document review or filing
- Pending RFE or NOID responses (approaching deadlines)
- Recently approved cases
- Cases with upcoming court dates
- Priority Date movements relevant to pending cases

**CRM (if connected):**
- New consultation requests
- Follow-ups needed on potential clients
- Retainer agreements awaiting signature

#### Output Format

```
## Daily Immigration Brief -- [Date]

### Urgent / Action Required
[Items needing immediate attention: RFE/NOID deadlines, court hearings, detained clients]

### USCIS Notices & Updates
- **RFEs/NOIDs Received**: [count and deadlines]
- **Approvals**: [newly approved cases]
- **Interview Notices**: [upcoming interviews]
- **Policy Updates**: [relevant USCIS or State Dept changes]

### Case Pipeline
- **Ready to File**: [cases with complete documentation]
- **Awaiting Client Documents**: [cases waiting on evidence]
- **Pending Responses**: [RFEs, NOIDs, or motions awaiting filing]

### Court Matters
- **Today's Hearings**: [immigration court appearances]
- **Upcoming Deadlines**: [brief deadlines, evidence submission dates]

### New Client Matters
[Consultation requests, intake forms received, retainer agreements pending]

### Calendar Today
[Client meetings, court appearances, USCIS interviews, and prep needed]

### Visa Bulletin / Priority Dates
[Any movement in priority dates affecting pending cases]

### Team Activity
[Key messages or updates from case management channels]

### This Week's Critical Deadlines
[RFE responses, court filings, petition deadlines]

### Sources Not Available
[Any sources that were not connected or returned errors]
```

---

### Case Research Brief

Research and brief on a specific immigration law question, case type, or procedural issue across available sources.

#### Workflow

1. Accept the case topic or query from the user
2. Search across connected sources:
   - **Documents**: Internal memos, prior case strategies, procedural guides, template arguments
   - **Email**: Prior communications on similar case types
   - **Chat**: Team discussions about the issue
   - **Case Management**: Similar cases, success rates, approval patterns
3. Synthesize findings into a structured brief

#### Output Format

```
## Case Research Brief: [Topic]

### Summary
[2-3 sentence executive summary of findings]

### Case Type Overview
[Visa category, relief type, or procedural issue being researched]

### Firm Precedent
[Prior cases the firm has handled with similar facts, outcomes, strategies used]

### Common Issues & Solutions
[Typical RFE triggers, evidence gaps, arguments that have worked]

### USCIS Adjudication Patterns
[Known trends from firm experience: approval rates, processing times, problematic service centers]

### Key Evidentiary Requirements
[Critical documents and evidence standards based on firm knowledge]

### Strategic Considerations
[Risks, alternative visa categories, timing issues]

### Knowledge Gaps
[What information is missing or requires external legal research]

### Recommended Resources
[AILA practice advisories, relevant statutes/regulations to review, external counsel consultation if needed]

### Next Steps
[What the user should do with this information]
```

#### Important Notes
- Case research briefs synthesize firm knowledge and internal precedent; they do not substitute for formal immigration law research
- If the query requires current case law, AAO decisions, or regulatory interpretation, recommend the user consult AILA resources, immigration law databases, or experienced practitioners
- Always note the limitations of internal sources

---

### Urgent Matter Brief

Rapid briefing for urgent immigration situations requiring immediate attention (ICE detentions, expedite requests, emergency relief, inadmissibility issues at port of entry, etc.).

#### Workflow

1. Accept the urgent matter description
2. Rapidly scan all connected sources for relevant context:
   - **Email**: Communications about the urgent matter
   - **Chat**: Real-time team discussions and escalations
   - **Documents**: Relevant client files, prior emergency filings, bond procedures
   - **Calendar**: Any scheduled hearings or appointments
   - **Case Management**: Client history, pending applications, immigration status
3. Compile into an actionable urgent matter brief

#### Output Format

```
## Urgent Matter Brief: [Topic]
**Prepared**: [timestamp]
**Urgency Level**: [critical/high/moderate]

### Situation Summary
[What is known about the urgent matter]

### Client Background
[Immigration status, pending applications, prior immigration history from case files]

### Timeline
[Chronological summary of events based on available sources]

### Immediate Immigration Considerations
[Removal defense options, bond eligibility, expedite criteria, emergency relief availability]

### Pending Applications
[Any applications in process that may be affected]

### Relevant Case History
[Prior filings, denials, appeals, waivers in client's history]

### Internal Response
[What response activity has already occurred based on email/chat]

### Key Contacts
[Client emergency contact, family members, detention facility, ICE officer, immigration judge]

### Recommended Immediate Actions
1. [Most urgent action - e.g., file stay of removal, request expedite, schedule bond hearing]
2. [Second priority - e.g., gather evidence, contact client]
3. [Additional steps]

### Critical Deadlines
[Response deadlines, hearing dates, custody review timelines]

### Information Gaps
[What is not yet known: A-number, detention location, charging documents, etc.]

### Sources Checked
[What was searched and what was not available]
```

#### Important Notes for Urgent Matter Briefs
- Speed is critical. Produce the brief quickly with available information
- Flag any deportation risk or custody issues immediately
- Note whether client is detained and location if known
- If matter involves potential criminal grounds of inadmissibility, flag immediately
- Identify any expedite criteria that may apply (severe financial loss, emergency, humanitarian, USCIS error)
- For detained clients, note bond eligibility and mandatory detention considerations
- Recommend consultation with experienced removal defense counsel if matter is complex

## General Notes

- If sources are unavailable, note the gaps prominently so the user knows what was not checked
- For daily briefs, learn the user's preferences over time (priority case types, which updates matter most)
- Briefs should be actionable: every item should have a clear next step or reason for inclusion
- Keep briefs concise. Link to source materials rather than reproducing them in full
- Always consider visa category context: employment-based, family-based, humanitarian, removal defense
- Flag any issues that may affect client's ability to maintain status or travel

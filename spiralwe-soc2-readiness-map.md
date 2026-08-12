# SpiralWe SOC 2 Readiness Map — For Humans

**Status:** Working readiness map  
**Purpose:** Prepare SpiralWe for a future SOC 2 review in a way that is understandable to non-specialists and traceable to the repository's existing Initial Project Priorities.  
**Primary working structure:** SpiralWe's 13 Initial Project Priorities.  
**Formal framework:** AICPA Trust Services Criteria (TSC).  
**Implementation source of truth:** `drGelston/spiral-insight-app`.  
**Reviewer/evidence source:** `drGelston/spiral-insight-governance-review`.

> **Important:** This is a readiness and governance map. It is not a SOC 2 report, certification, attestation, legal opinion, or CPA examination.

---

## 1. How to use this map

This map deliberately does **not** replace the 13 Initial Project Priorities in the SpiralWe SOC 2 review repository. Those priorities are the chapters of the work.

The map adds three layers around them:

1. **Plain-English explanation** — What does this priority actually mean?
2. **Control and evidence chain** — What are we trying to prevent, what do we do about it, and how do we prove it?
3. **SOC 2 cross-reference** — Which formal Trust Services Criteria does the work support?

The basic chain is:

```text
SPIRALWE PRIORITY
      ↓
What is the risk?
      ↓
What control reduces the risk?
      ↓
How is the control implemented?
      ↓
Does it actually operate?
      ↓
What evidence proves that?
      ↓
Has the evidence been reviewed?
      ↓
PASS / PARTIAL / MISSING / OUTSIDE_REPO / N/A
```

### The most important rule

**Having a policy or having code is not the same thing as proving that a control works.**

A policy without evidence of execution remains incomplete. A technical safeguard without evidence that it operated remains incomplete. The repository's current review model explicitly requires evidence to support the exact claim being made.

---

# 2. The eight questions every priority must answer

For each of the 13 priorities, the readiness review should answer:

1. **What is SOC 2 asking us to accomplish?**
2. **Does this expectation apply to SpiralWe? Why?**
3. **What does SpiralWe currently have?**
4. **Where is the evidence?**
5. **Is it documented, implemented, operating, evidenced, and reviewed?**
6. **What is missing or weak?**
7. **What needs to happen before an auditor reviews it?**
8. **What can SpiralWe honestly claim today, and what should we not claim yet?**

A ninth question should be used for Type II readiness:

9. **What evidence needs to accumulate over time?**

---

# 3. Status vocabulary

Use the repository's existing status vocabulary rather than inventing a second scoring system.

| Status | Plain-English meaning |
|---|---|
| `PASS` | Enough design, implementation, and operating evidence exists to support the control. |
| `PARTIAL` | Something exists, but implementation, enforcement, operating evidence, or proof is incomplete. |
| `MISSING` | The required control or evidence has not yet been established. |
| `OUTSIDE_REPO` | The control/evidence primarily lives in personnel, contractual, vendor, operational, or other records outside source control. |
| `N/A` | The control does not apply to the defined scope, and the reason is recorded. |

### Reviewer status

| Reviewer status | Plain-English meaning |
|---|---|
| `NOT_REVIEWED` | Evidence has not yet been independently reviewed. |
| `VERIFIED` | Evidence was reviewed and supports the claim. |
| `INSUFFICIENT` | Evidence was reviewed but does not support the claim well enough. |
| `QUESTION` | Something needs clarification before the evidence can be accepted. |

---

# 4. The 13 Initial Project Priorities

## Priority 1 — Source-code and change-control governance

### In normal English
**Who is allowed to change SpiralWe, how are changes reviewed, and how do we know an unsafe change did not simply go straight into production?**

### Why it matters
Software changes can introduce security weaknesses, break services, or change how data is handled. SOC 2 readiness therefore needs a controlled and traceable change process.

### What we need to examine
- Branch and pull-request rules
- Code review
- Testing before release
- Approval and merge controls
- Production deployment controls
- Emergency changes
- Reconciliation of emergency changes
- GitHub platform enforcement versus written policy

### Evidence examples
- Pull request records
- Review/approval records
- Test results
- Merge records
- Deployment records
- Immutable commit identifiers
- Change-control receipts

### Key question
**Is the process merely written down, or is it technically and operationally enforced?**

### SOC 2 connection
Primarily **Security**; exact criteria mapping should be completed in the formal control matrix.

---

## Priority 2 — Identity, authentication, authorization, and privileged access

### In normal English
**Who can get into SpiralWe, how do they prove who they are, and what are they allowed to do once inside?**

### Why it matters
People should receive the access they need for their job or role, not unlimited access simply because they have an account.

### What we need to examine
- Authentication
- Multi-Factor Authentication (MFA)
- Administrative accounts
- Privileged access
- Least privilege
- Access approval
- Access removal
- Periodic access review

### Evidence examples
- Identity-provider configuration
- MFA status
- Access lists
- Privileged-account inventory
- Access review receipts
- Joiner/mover/leaver records

### Key question
**Can SpiralWe show who has access, why they have it, and that inappropriate access is removed?**

### SOC 2 connection
Primarily **Security**; exact criteria mapping should be completed in the formal control matrix.

---

## Priority 3 — Secrets and credential management

### In normal English
**How do we keep passwords, API keys, tokens, and other digital keys out of the wrong hands?**

### Why it matters
A leaked credential can give an attacker the same power as a legitimate user or service.

### What we need to examine
- Secret storage
- Secret scanning
- Rotation
- Exposure response
- Developer practices
- Production versus development credentials
- Access to credential stores

### Evidence examples
- Secret-scan results
- Credential-management configuration
- Rotation records
- Exposure/remediation records
- Sanitized receipts

### SOC 2 connection
Primarily **Security**.

---

## Priority 4 — Development-machine security baseline for both machines

### In normal English
**Are the computers used to build and maintain SpiralWe themselves secure?**

### Why it matters
A secure application can still be compromised through an insecure developer machine.

### What we need to examine
Each authorized development machine must independently demonstrate the required endpoint controls.

Use stable aliases such as:
- `DEV-MACHINE-A`
- `DEV-MACHINE-B`

Avoid unnecessary device serial numbers, personal device names, IP addresses, usernames, or secrets in the evidence repository.

### Evidence examples
- Endpoint baseline receipt
- Operating-system/security configuration checks
- Encryption status
- Screen-lock controls
- Malware protection where applicable
- Patch status
- Account/access configuration

### Key question
**Can each authorized machine independently demonstrate the baseline?**

### SOC 2 connection
Primarily **Security**.

---

## Priority 5 — Application and database access boundaries

### In normal English
**Can one person or organization see or change information that belongs to someone else?**

### Why it matters
SpiralWe handles information that can be sensitive. Technical access boundaries need to enforce who can see and change what.

### What we need to examine
- Server-side authorization
- Database permissions
- Row-Level Security (RLS), where applicable
- Tenant/user boundaries
- Administrative access
- Data access paths
- Tests of access boundaries

### Evidence examples
- Authorization tests
- Database security tests
- RLS validation
- Access-control configuration
- Sanitized test receipts

### Key question
**Are the boundaries enforced by the system, rather than merely described in documentation?**

### SOC 2 connection
Primarily **Security**, with possible **Confidentiality** and **Privacy** implications depending on scope.

---

## Priority 6 — Logging, monitoring, and security-event evidence

### In normal English
**If something important happens, can we tell what happened?**

### Why it matters
Without useful records, it can be difficult to detect, investigate, or prove security events.

### What we need to examine
- Important security events
- Authentication/access events
- Administrative activity
- Change/deployment events
- Monitoring
- Alerting
- Retention
- Protection of logs
- Review of important events

### Evidence examples
- Sanitized log samples
- Monitoring configuration
- Alert records
- Review receipts
- Retention configuration

### SOC 2 connection
Primarily **Security**; availability monitoring may also support **Availability**.

---

## Priority 7 — Vulnerability and dependency management

### In normal English
**How do we find weaknesses in SpiralWe and in the software SpiralWe depends on, and what do we do about them?**

### Why it matters
Software changes over time. New vulnerabilities can appear in code and third-party components.

### What we need to examine
- Vulnerability scanning
- Dependency scanning
- Dependency pinning
- Triage
- Severity decisions
- Remediation timelines
- Exceptions
- Supply-chain controls

### Evidence examples
- Scan results
- Dependency reports
- Remediation records
- Exception approvals
- Dependency pinning evidence

### Key question
**Do we have a repeatable process, or do we only fix problems when someone happens to notice them?**

### SOC 2 connection
Primarily **Security**.

---

## Priority 8 — Incident response

### In normal English
**What happens when something goes wrong? Who responds, who decides, who gets notified, and how do we learn from it?**

### Why it matters
Security incidents cannot be handled reliably by improvisation.

### What we need to establish/evidence
- Incident-response plan
- Roles and responsibilities
- Escalation path
- Severity/classification approach
- Communications
- Evidence preservation
- Customer/regulatory notification decision process where applicable
- Lessons learned
- Periodic exercise

### Evidence examples
- Incident-response plan
- Tabletop exercise record
- Incident tickets
- After-action review
- Remediation tracking

### Current readiness signal
The repository's initial baseline identifies incident response as a major gap requiring a formal program and operating evidence.

### SOC 2 connection
Primarily **Security**.

---

## Priority 9 — Backup, recovery, and restore testing

### In normal English
**If important information or systems are lost, can SpiralWe actually get them back?**

### Why it matters
Having backups is not the same as knowing that the backups can be restored.

### What we need to examine
- Backup scope
- Backup frequency
- Backup protection
- Retention
- Restore procedures
- Restore testing
- Recovery objectives
- Dependencies

### Evidence examples
- Backup configuration
- Restore-test records
- Recovery test results
- Recovery objectives
- Corrective-action records

### Key question
**Have we actually tested recovery, or do we simply believe the backup system will work?**

### SOC 2 connection
Primarily **Availability**, and potentially **Security** depending on the control.

---

## Priority 10 — Data classification, retention, deletion, and privacy boundaries

### In normal English
**What information does SpiralWe have, how sensitive is it, who should handle it, how long should we keep it, and when should we delete it?**

### Why it matters
Trust depends on handling information according to its sensitivity and commitments.

### What we need to examine
- Data categories
- Sensitive/personal information
- Student/child/family/educator information where applicable
- Collection/use boundaries
- Retention periods
- Deletion rules
- Technical deletion enforcement
- Privacy commitments
- Third-party data handling

### Evidence examples
- Data inventory/classification
- Retention schedule
- Deletion records/tests
- Privacy control receipts
- Vendor/subprocessor evidence

### Key question
**Are our promises about data handling backed by actual processes and technical enforcement?**

### SOC 2 connection
Potentially **Privacy**, **Confidentiality**, and **Security**, depending on scope.

---

## Priority 11 — Vendor and subprocessor management

### In normal English
**What happens when another company handles SpiralWe's data or provides an important service that SpiralWe depends on?**

### Why it matters
SpiralWe cannot fully manage risk if it does not know which outside organizations can affect its systems or information.

### What we need to examine
- Vendor inventory
- Critical vendors
- Subprocessors
- Security/privacy review
- Contracts
- Data handling
- Vendor attestations
- Ongoing review
- Vendor termination/offboarding

### Evidence examples
- Vendor register
- Security questionnaires
- SOC reports/attestations where available
- Contracts or approved summaries
- Review receipts

### Key question
**Do we know who our important third parties are and what risk they introduce?**

### SOC 2 connection
Primarily **Security**, with **Availability**, **Confidentiality**, or **Privacy** implications depending on the vendor and service.

---

## Priority 12 — Personnel onboarding, offboarding, training, and access review

### In normal English
**What happens when someone joins SpiralWe, changes roles, or leaves? Do they get the right access and lose it when they should?**

### Why it matters
People are part of the security system. Access and responsibilities need to follow the person's role.

### What we need to examine
- Onboarding
- Role changes
- Offboarding
- Access grants
- Access removal
- Security awareness/training
- Periodic access review
- Responsibility assignment

### Evidence examples
- Onboarding/offboarding records
- Training completion records
- Access-review receipts
- Role/access approvals

### Important distinction
Some of this evidence will naturally be **OUTSIDE_REPO**. The governance-review repository explicitly allows for organizational, personnel, contractual, vendor, and operational evidence outside source control.

### SOC 2 connection
Primarily **Security**.

---

## Priority 13 — Recurring evidence collection and control-owner accountability

### In normal English
**How do we prove next month, next quarter, and during a SOC 2 Type II review that we are still doing all of this?**

### Why it matters
SOC 2 readiness is not a one-time cleanup project. Controls need owners, recurring activities, and evidence.

### What we need to establish
- Control owners
- Evidence owners
- Evidence cadence
- Receipt format
- Evidence retention
- Review cadence
- Finding management
- Re-testing
- Status changes
- Accountability for overdue evidence

### Evidence examples
- Compliance receipts
- Periodic access reviews
- Restore tests
- Incident exercises
- Vendor reviews
- Release-control samples
- Dated readiness reports
- Closed findings with supporting evidence

### Key question
**If an auditor asks what happened six months ago, can we find the evidence without reconstructing the story from memory?**

### SOC 2 connection
This is the evidence/governance layer supporting the other Trust Services Criteria rather than a standalone substitute for them.

---

# 5. How the 13 priorities connect to the SOC 2 Trust Services Criteria

The five Trust Services Criteria are the formal SOC 2 categories:

| Acronym | Full name | Plain-English meaning |
|---|---|---|
| TSC | Trust Services Criteria | The criteria used to evaluate the relevant controls. |
| Security | Security | Protect systems and information from unauthorized access or harmful activity. |
| Availability | Availability | Keep systems available for operation and use as committed. |
| Processing Integrity | Processing Integrity | Make sure systems process information completely, accurately, and as intended. |
| Confidentiality | Confidentiality | Protect information designated as confidential. |
| Privacy | Privacy | Handle personal information appropriately according to applicable commitments and criteria. |

**Important:** Security is the common foundation. The other categories should be included only to the extent they are part of SpiralWe's defined SOC 2 scope and commitments.

The formal criterion mapping belongs in the repository's canonical SOC 2 control matrix. This human map should not invent formal criterion IDs where the source material has not yet established them.

---

# 6. The evidence model

The repository's evidence model should be treated as a core part of the map.

Every material compliance claim should have either:

- a sanitized evidence receipt; or
- an explicitly identified evidence source outside the repository.

A receipt should identify, where applicable:

- Receipt ID
- Control ID
- Date/time
- Evidence type
- Source system
- Source reference
- Immutable source identifier such as a commit SHA, pull request, deployment, migration, test, or scan
- Sanitized evidence summary
- Validation result
- Evidence hash where useful
- Control owner
- Reviewer status
- Reviewer name/date
- Limitations or redactions

### What must never be copied into the reviewer repository

Do not mirror:

- Application source code when a receipt is sufficient
- Environment variables
- API keys, tokens, passwords, signing material, or secret values
- Private SSH keys
- Raw production logs containing personal information
- Raw learner, child, family, educator, school, journal, conversation, or reflection data
- Production database dumps
- Unnecessary exploit details
- Unapproved vendor credentials or contract material

Use summaries, redaction, hashes, counts, identifiers, and reviewer-safe excerpts instead.

---

# 7. What "ready" should mean

Do not use the word **ready** to mean "we wrote a policy."

For this map, a mature control should progress through:

```text
DESIGNED
  ↓
IMPLEMENTED
  ↓
OPERATING
  ↓
EVIDENCED
  ↓
REVIEWED
  ↓
READY FOR EXAMINATION
```

A control may be technically implemented and still be `PARTIAL` because operating evidence has not accumulated.

This distinction is especially important for a future **SOC 2 Type II** examination, where the auditor evaluates whether controls operated over a period of time.

---

# 8. Current-state discipline

The map should always distinguish among four different statements:

### 1. "SpiralWe says it does this."
A policy, design document, README, or governance statement exists.

### 2. "SpiralWe has implemented this."
The technical or operational mechanism exists.

### 3. "SpiralWe can prove this operated."
Evidence shows the mechanism was actually used.

### 4. "The reviewer verified this."
An independent reviewer examined the evidence and accepted it.

These are **not interchangeable**.

---

# 9. Initial readiness focus

The current governance-review repository identifies the following broad strengths and gaps in its initial SOC 2 baseline.

### Areas identified as strengths

- Application access control and server-side access/entitlement controls
- Security validation tooling
- Release governance and deployment discipline
- Recurring repository audit practice
- Supply-chain controls such as dependency pinning

### Areas identified as partial or missing

- Full GitHub branch protection and required-status enforcement
- Centralized/deterministic CI validation and evidence where needed
- Development-machine baseline evidence for both machines
- Fully enforced privacy controls for relevant beta/open-beta boundaries
- Formal incident-response program and exercises
- Formal backup/restore program and tested restoration evidence
- Recovery objectives and business-continuity evidence
- Vendor/subprocessor management
- Personnel/access governance
- Data classification, retention, and deletion evidence
- Recurring evidence collection and control-owner accountability

These are readiness observations from the repository's current baseline, not independent audit findings.

---

# 10. The master working table

This table should eventually become the high-level dashboard for the map.

| # | Priority | Plain-English question | Current status | Evidence | Reviewer status | Next action |
|---|---|---|---|---|---|---|
| 1 | Change control | Who can change SpiralWe and how do we know changes are controlled? | PARTIAL | To inventory | NOT_REVIEWED | Verify enforcement, testing, deployment evidence |
| 2 | Identity & access | Who can get in, and what can they do? | PARTIAL | To inventory | NOT_REVIEWED | Inventory privileged systems and MFA/access evidence |
| 3 | Secrets | How do we protect digital keys? | PARTIAL | To inventory | NOT_REVIEWED | Verify storage, rotation, scanning, exposure response |
| 4 | Development machines | Are the computers used to build SpiralWe secure? | MISSING | To collect | NOT_REVIEWED | Baseline both machines separately |
| 5 | Data boundaries | Can users access only the information they should? | PARTIAL | To inventory | NOT_REVIEWED | Evidence application/database boundaries |
| 6 | Logging | Can we tell what happened? | PARTIAL | To inventory | NOT_REVIEWED | Define required events and retention evidence |
| 7 | Vulnerabilities | How do we find and fix weaknesses? | PARTIAL | To inventory | NOT_REVIEWED | Establish recurring scan/triage/remediation evidence |
| 8 | Incident response | What happens when something goes wrong? | MISSING | To collect | NOT_REVIEWED | Establish plan, roles, escalation, exercise |
| 9 | Backup/recovery | Can we actually get important things back? | PARTIAL | To collect | NOT_REVIEWED | Document backups and perform restore test |
| 10 | Data/privacy | What do we keep, why, who can use it, and when do we delete it? | MISSING/PARTIAL by sub-control | To inventory | NOT_REVIEWED | Complete classification, retention, deletion, privacy evidence |
| 11 | Vendors | What risks come from companies we depend on? | MISSING | To collect | NOT_REVIEWED | Create vendor/subprocessor register and review process |
| 12 | People | What happens when people join, change roles, or leave? | OUTSIDE_REPO | To collect | NOT_REVIEWED | Establish onboarding/offboarding/training/access evidence |
| 13 | Evidence & ownership | How do we prove we keep doing this? | PARTIAL | To inventory | NOT_REVIEWED | Establish recurring evidence cadence and owner accountability |

**Note:** The status column is a working readiness view based on the repository's current baseline and should be updated only when new evidence supports a status change.

---

# 11. What this map is — and is not

### This map IS

- A plain-English explanation of the SpiralWe SOC 2 readiness effort
- Organized around the repository's 13 Initial Project Priorities
- A bridge between business/governance language and audit language
- A guide to controls and evidence
- A way to identify gaps and next actions
- A framework for tracking evidence over time

### This map IS NOT

- A substitute for the AICPA Trust Services Criteria
- A substitute for the canonical SOC 2 control matrix
- A SOC 2 report
- A certification
- A CPA examination
- A claim that SpiralWe currently satisfies every SOC 2 requirement
- A replacement for the production application repository

---

# 12. Recommended next step

Use this map as the **master human-facing guide**, then work through the 13 priorities one at a time.

For each priority:

1. Confirm the scope and applicable SOC 2 expectations.
2. Identify the actual SpiralWe control.
3. Locate the implementation in `spiral-insight-app` or the appropriate operational system.
4. Identify the evidence receipt or outside-repository evidence.
5. Determine whether the control is designed, implemented, operating, and evidenced.
6. Have the reviewer assess the evidence.
7. Record the status.
8. Open a finding for material gaps.
9. Remediate in the appropriate implementation/operational system.
10. Collect new evidence and re-review.

The goal is not to make the repository look green.

The goal is to make the evidence strong enough that an independent reviewer can determine, without guesswork, **what SpiralWe claims, what actually exists, what evidence proves it, what remains incomplete, and who is responsible for the next step.**

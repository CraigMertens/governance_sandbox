# SpiralWe Trust, Institutional Readiness & Grant Readiness Canon

> **Status:** Draft canonical governance charter for review  
> **Client:** SpiralWe  
> **Reviewer:** Craig Mertens, independent reviewer/consultant  
> **Repository role:** Governance orientation, requirements, evidence, assessment, and readiness planning  
> **Implementation authority:** None  
> **Initial version date:** 2026-07-27

## 1. Purpose

This Canon defines how SpiralWe will organize, evaluate, evidence, and communicate trust, institutional readiness, grant readiness, and ongoing governance.

It is designed to help SpiralWe answer two related questions:

1. **Why should a client trust SpiralWe?**
2. **Why should a government agency, university, school district, research partner, or institutional funder believe SpiralWe can responsibly execute the proposed work?**

The Canon establishes a common operating language for claims, requirements, evidence, ownership, status, escalation, and review. It is not a claim that SpiralWe has already satisfied every requirement described here.

The governing traceability rule is:

> **Claim → Requirement → Evidence → Owner → Status → Review Authority**

A claim is not institution-ready merely because it is plausible, intended, documented, demonstrated in a beta environment, or present somewhere in source code. It becomes supportable only when its requirements are identified, its evidence is current and sufficient, an accountable owner is named, its status is accurately represented, and the appropriate authority has reviewed it.

## 2. Scope

This Canon governs SpiralWe work related to:

- client trust;
- education-sector use;
- institutional due diligence;
- grant and government-funding readiness;
- research and IRB readiness;
- AI governance;
- privacy and data protection;
- student and child information;
- security assurance;
- record and artifact integrity;
- human authority and decision rights;
- institutional contracting;
- external claims and representations; and
- ongoing governance operations.

It applies to review materials, proposals, grant narratives, due-diligence responses, institutional discussions, policy drafts, risk and evidence registers, readiness assessments, and recommendations made in this repository.

It does not itself modify application code, production infrastructure, product behavior, contracts, privacy notices, security controls, research protocols, or legal obligations.

## 3. Authority and source-of-truth hierarchy

### 3.1 Application implementation

The Spiral application repository is the source of truth for implementation. The current review materials identify `drGelston/spiral-insight-app` as that source.

This governance repository may describe, assess, excerpt, or recommend. It does not override the application repository and does not authorize implementation changes.

### 3.2 Governance-review evidence

The repository `drGelston/spiral-insight-governance-review` is a curated orientation and review layer. It contains reviewer-facing summaries, boundaries, questions, risks, and recommendations. Those materials are useful evidence of documented posture but are not, by themselves, proof of production behavior or legal compliance.

### 3.3 This repository

`CraigMertens/governance_sandbox` is the working home for the SpiralWe Canon and its associated requirements, evidence, gap, risk, assessment, and roadmap materials.

Documents here may become canonical governance records only when their status, owner, approver, effective date, and review date are explicit. Draft status must never be omitted or obscured.

### 3.4 Conflict rule

When sources disagree:

1. observed and reproducible production evidence governs claims about production;
2. the application repository governs claims about implemented code;
3. approved operational records govern claims about operating practice;
4. signed agreements govern contractual commitments;
5. approved policies govern organizational policy;
6. qualified professional determinations govern legal, privacy, security, and research conclusions; and
7. review summaries and plans must be corrected to match the controlling source.

A newer date does not automatically make a source authoritative. Authority, environment, approval status, and evidence quality must all be considered.

## 4. Mandatory status distinctions

Every material claim must identify the state to which it applies. At minimum, reviewers must distinguish:

| Status | Meaning |
|---|---|
| **Observed beta behavior** | Behavior directly observed in the current beta environment. |
| **Observed production behavior** | Behavior directly observed and reproducible in production. |
| **Implemented on main** | Capability evidenced in the main application branch, whether or not deployed. |
| **Deployed infrastructure** | Infrastructure present in an environment, which may still be inactive or inaccessible. |
| **Gated/default-off** | Capability present but deliberately unavailable until named gates are satisfied. |
| **Design intent** | An approved or proposed design that is not evidence of implementation. |
| **Draft governance** | Scaffolding, a checklist, or a proposed rule not yet approved as operating policy. |
| **Future planning** | Grant, nonprofit, institutional, research, or product planning that is not current capability. |
| **Unknown/unverified** | A matter for which sufficient current evidence has not been reviewed. |
| **Retired/superseded** | A capability or statement that is no longer current and must not be presented as active. |

The phrases “supported,” “available,” “secure,” “compliant,” “approved,” “validated,” “ready,” and “complete” must not be used without an identified scope and evidence basis.

## 5. Canonical governance record

Each material claim or readiness requirement must be traceable through the following fields:

| Field | Required content |
|---|---|
| **Claim ID** | Stable identifier. |
| **Claim** | Exact internal or external assertion being evaluated. |
| **Audience and use** | Client, school, district, university, agency, funder, IRB, researcher, or internal decision. |
| **Requirement** | Legal, contractual, technical, operational, ethical, grant, or institutional condition supporting the claim. |
| **Applicability basis** | Why the requirement applies, or who must determine applicability. |
| **Evidence** | Artifact, observation, test, record, agreement, approval, or professional opinion. |
| **Evidence location** | Repository path, controlled record, or system of record. |
| **Evidence date** | When the evidence was created or last verified. |
| **Owner** | SpiralWe role accountable for completing and maintaining the item. |
| **Status** | One of the mandatory status distinctions, plus readiness state. |
| **Gap or risk** | What remains absent, uncertain, expired, contradictory, or insufficient. |
| **Review authority** | Person or qualified role authorized to review or determine the matter. |
| **Decision** | Accepted, rejected, conditional, deferred, or escalated. |
| **Next review** | Date or event that triggers re-evaluation. |

Missing evidence must be recorded as a gap, not replaced by inference. Absence of a known incident is not evidence that a control exists or works.

## 6. Trust model

SpiralWe trust is built from six mutually reinforcing forms of evidence:

1. **Truthful scope:** external language matches the current product, environment, audience, and operating model.
2. **Bounded authority:** AI, staff, reviewers, administrators, and professionals have clearly separated decision rights.
3. **Responsible information stewardship:** data is known, classified, minimized, protected, retained, corrected, and deleted under documented rules.
4. **Operational capability:** commitments have owners, procedures, resources, training, and review cycles.
5. **Independent review:** claims requiring specialized judgment are routed to appropriately qualified reviewers.
6. **Correctability:** records, claims, assessments, and artifacts can be challenged, corrected, superseded, and audited.

Trust is not a one-time certification. It is a maintained relationship between claims and current evidence.

## 7. Client trust

Before making a material client-facing claim, SpiralWe must be able to explain:

- what service is actually being offered;
- who the intended users are;
- what the service does and does not do;
- what information it handles;
- how AI participates;
- where human judgment remains controlling;
- what security, privacy, support, and incident practices apply;
- how errors and records can be corrected;
- which commitments are contractual;
- which capabilities are beta, gated, planned, or unavailable; and
- who is accountable when a concern is raised.

Marketing, demonstrations, proposals, grant narratives, and due-diligence responses must use the same current claim set. A favorable description in one channel must not outrun the evidence available in another.

## 8. Institutional readiness

Institutional readiness means SpiralWe can withstand structured inquiry and responsibly perform the work being proposed. It is not limited to product functionality.

An institutional readiness assessment must address:

- legal-entity and operating responsibility;
- service description and user population;
- governance and decision rights;
- data flows, systems, vendors, and subprocessors;
- privacy and student-data posture;
- security program and incident handling;
- accessibility and equitable access where applicable;
- AI use, human oversight, testing, and change control;
- contracting and insurance requirements;
- staffing, training, support, and continuity;
- recordkeeping and evidence retention;
- research and publication boundaries;
- financial and grant administration capability; and
- open gaps, compensating controls, and escalation decisions.

No district-, university-, agency-, or funder-readiness conclusion may be generalized to another institution or jurisdiction without reviewing the new requirements.

## 9. Grant and government-funding readiness

Grant readiness requires more than an eligible idea. SpiralWe must be able to connect proposed outcomes to an executable, governable, and measurable delivery model.

Each grant or government-funding opportunity must have evidence for:

- applicant and partner eligibility;
- statement of need and intended beneficiaries;
- permitted activities and costs;
- delivery roles and related-party relationships;
- work plan, milestones, staffing, and dependencies;
- budget basis, cost allocation, and procurement rules;
- data collection and evaluation plan;
- privacy, security, AI, and research boundaries;
- reporting, record-retention, and audit obligations;
- subaward, contractor, and vendor oversight;
- conflicts of interest;
- sustainability after the funding period; and
- a claims review ensuring that proposed capability is not presented as current capability.

Grant-funded service delivery, nonprofit activity, institutional access, and commercial product development must be clearly distinguished. Funds must not be described or structured as disguised product capitalization. Any related-party arrangement— including a nonprofit or program purchasing SpiralWe access, services, or training—requires documented purpose, pricing basis, decision authority, conflict management, and professional review where required.

## 10. AI governance

SpiralWe must describe AI as bounded assistance, not human authority.

AI governance records must identify:

- the AI-supported task;
- the model or service used;
- the input and output data;
- intended users and prohibited uses;
- whether output is suggestion, interpretation, draft, classification, or decision support;
- the human review gate before durable or consequential use;
- testing and known limitations;
- privacy and vendor implications;
- prompt, model, or workflow change controls;
- monitoring and incident processes; and
- the boundary between service operation, service improvement, evaluation, fine-tuning, and model-weight training.

Current review materials state that the system does not diagnose, score, assign clinical labels, or make AI the final human authority. They also describe a posture against using participant data for model-weight training or third-party fine-tuning without separate IRB approval and explicit consent, while noting that the consent surface is not yet live. These are documented postures requiring current implementation, contract, privacy, and research evidence before they are used as institutional assurances.

No AI output may silently become a durable learner record, governed solution, external claim, or consequential decision.

## 11. Data privacy

SpiralWe must maintain a current data inventory and data dictionary before making broad privacy or institutional-readiness claims.

The privacy program must address:

- data elements and classifications;
- source and method of collection;
- purpose and legal or contractual basis;
- data subjects and user roles;
- storage locations and data flows;
- access and disclosure;
- vendors and subprocessors;
- retention and deletion;
- access, correction, withdrawal, and other rights processes;
- de-identification and aggregation;
- secondary use;
- incident and breach response;
- privacy notices and consent surfaces; and
- jurisdiction- and contract-specific requirements.

FERPA, COPPA, state student-privacy laws, GDPR, HIPAA, and other frameworks must remain **open applicability and professional-review questions** unless qualified authority has issued a scoped determination supported by current facts.

## 12. Student and child information

Current review materials describe Spiral as adult-facing and learner/minor accounts as blocked pending unresolved decisions. That boundary must remain visible in every relevant assessment and external statement.

Before any learner-facing or child-directed capability is enabled, SpiralWe must have, at minimum:

- an approved feature and data-flow map;
- age, user-role, and audience determination;
- guardian, school, and consent requirements;
- rights and correction processes;
- retention and deletion rules;
- contract and notice position;
- security and access-control review;
- vendor and redisclosure review;
- safety and crisis-expectation analysis;
- AI and research-use boundaries;
- qualified legal and privacy review; and
- explicit release authority.

Teacher-entered observations about a learner must not be presumed to fall outside education-record or child-data requirements. Classification belongs to qualified privacy counsel based on a complete technical and operational record.

The current absence of crisis detection, automatic escalation, or guardian notification must be stated plainly wherever a partner could otherwise infer those capabilities.

## 13. Record and artifact integrity

SpiralWe must preserve the distinction between:

- evidence and interpretation;
- suggestion and kept idea;
- planned action and completed action;
- candidate and approved record;
- draft and governing policy;
- internal reuse and externalization;
- current statement and superseded statement.

Durable records require an identified human promotion or approval gate. AI output, inferred meaning, or participation alone must not silently create an external claim, learner profile, governed solution, or authorization for disclosure.

Every canonical artifact must have version, status, owner, approval, effective date, review date, and supersession history. Corrections must preserve an audit trail appropriate to the sensitivity of the record.

## 14. Security

Security assurance must be based on documented and tested controls, not design language alone.

The security evidence set should address:

- governance and accountable security ownership;
- asset and data inventory;
- identity, role-based access, and privileged access;
- multifactor authentication;
- encryption in transit and at rest;
- secure development and change management;
- vulnerability, dependency, and secret management;
- logging, monitoring, and auditability;
- backups, recovery, and continuity;
- vendor risk;
- incident response;
- breach assessment and notification;
- secure retention and disposal; and
- periodic independent review.

A recognized framework such as the NIST Cybersecurity Framework may organize the evidence. Framework mapping is not certification. Controls marked as designed, partially audited, or planned must not be represented as verified operating controls.

## 15. Human authority

Human authority must be explicit for:

- learner- or client-affecting judgments;
- promotion of AI output into durable records;
- external communication and publication;
- crisis or safety response;
- access, correction, deletion, and disclosure decisions;
- product release and gate removal;
- institutional commitments;
- grant certifications and financial representations;
- research determination and protocol changes; and
- legal, privacy, security, or compliance conclusions.

AI may assist analysis and drafting. It does not replace professional judgment, organizational accountability, informed consent, or the decision rights assigned in this Canon.

## 16. Research and IRB

Ordinary educational practice, internal service operation, program evaluation, quality improvement, and research intended to contribute to generalizable knowledge must not be treated as interchangeable.

Before cross-participant analysis, efficacy claims, publication, model training, or other research-like use, SpiralWe must document:

- purpose and research question;
- population and data;
- identifiability and de-identification method;
- recruitment and consent;
- risks and benefits;
- data-management and sharing plan;
- investigator and sponsor roles;
- conflicts of interest;
- publication and dissemination plan; and
- the determination of an institutional or independent IRB or qualified research-compliance professional.

Neither this Canon nor Craig may declare an activity exempt from IRB review. No “IRB approved,” “IRB exempt,” “research ready,” or efficacy claim may be made without a scoped, documented determination from the proper authority.

## 17. Institutional contracting

Before accepting school, district, university, agency, or institutional data, SpiralWe must identify and review:

- contracting entity and authority;
- service scope;
- data ownership and permitted use;
- school-official or equivalent role, where applicable;
- confidentiality and redisclosure;
- security commitments;
- incident and breach obligations;
- access, correction, return, and deletion;
- subprocessors;
- audit and assurance rights;
- insurance and indemnity;
- accessibility and service levels;
- research, publication, and AI-use restrictions;
- governing law and jurisdiction; and
- record-retention obligations.

A recognized agreement such as the SDPC National Data Privacy Agreement may provide a baseline for review, but no template substitutes for institution- and jurisdiction-specific legal review.

## 18. Governance operating model

### 18.1 SpiralWe ownership

SpiralWe retains authority and accountability for:

- organizational strategy and risk acceptance;
- product and operational decisions;
- policies and contracts;
- staffing and resources;
- technical implementation;
- security and privacy operations;
- grant representations and administration;
- institutional commitments;
- research sponsorship; and
- approval of external claims.

### 18.2 Craig's role

Craig serves as an independent education, governance, compliance, and process reviewer. A possible expanded role is:

> **Fractional Operations Consultant — Compliance, Rights, and Institutional Readiness**

Subject to a written engagement, Craig may own or coordinate:

- requirements and evidence registers;
- gap and risk registers;
- readiness assessments and gates;
- claim-evidence traceability;
- institutional due-diligence preparation;
- grant-readiness reviews;
- documentation roadmaps;
- review scheduling and follow-up;
- cross-functional evidence collection; and
- escalation to qualified professionals.

Craig does not become product owner, technical architect, implementation authority, legal counsel, privacy counsel, security assessor, researcher of record, IRB, grant certifying official, or organizational risk acceptor merely by maintaining this Canon.

### 18.3 Required escalation

The following must be escalated to qualified authority:

| Matter | Review authority |
|---|---|
| Legal applicability, compliance determination, contract sufficiency | Qualified counsel |
| Privacy classification, notices, rights, and jurisdictional requirements | Qualified privacy counsel/professional |
| Security control design and assurance | Qualified security professional or assessor |
| Human-subjects research and exemption/approval | Institutional or independent IRB/research-compliance professional |
| Clinical or medical-device boundary | Qualified regulatory/clinical counsel |
| Grant eligibility, certifications, accounting, and audit | Authorized grant, finance, accounting, or legal professional |
| Production implementation and release | SpiralWe-authorized technical and product owners |

Escalation is a governance outcome, not a failure to complete the review.

## 19. Readiness gates

A readiness conclusion must use one of these states:

- **Not assessed**
- **Evidence collection**
- **Gap remediation**
- **Professional review required**
- **Conditionally ready**
- **Ready for the named scope**
- **Suspended**
- **Expired/reassessment required**

“Ready” must always name the scope, audience, environment, jurisdiction, use case, approving authority, evidence date, and conditions.

At minimum, no external institutional-readiness claim should pass until:

1. the service and audience are accurately scoped;
2. the data inventory and feature map are current;
3. applicable privacy, student-data, contracting, research, and security questions are routed;
4. AI and human-authority boundaries are documented;
5. material vendors and subprocessors are inventoried;
6. retention, deletion, rights, and incident processes are defined;
7. claims are tied to current evidence;
8. owners and escalation authorities are named; and
9. open gaps are disclosed and accepted by the proper authority.

## 20. Initial evidence and gap priorities

The current Spiral review materials identify these priority artifacts as incomplete or requiring validation:

1. data inventory;
2. data dictionary;
3. feature map for student or child data;
4. retention and deletion schedule and operating process;
5. access, correction, withdrawal, and other rights processes;
6. family-, school-, and district-facing privacy notice;
7. AI-use, service-improvement, and model-training boundary statement;
8. vendor and subprocessor inventory;
9. security posture and access-control audit;
10. incident-response plan;
11. breach-notification decision matrix;
12. district-contract review checklist and agreement position;
13. FERPA, COPPA, and state-law applicability memo for counsel;
14. research and IRB applicability memo;
15. de-identification and aggregation policy; and
16. evidence-backed grant and institutional delivery model.

These are gaps or evidence needs, not implied commitments that the artifacts already exist.

The dependency order is:

1. inventory the data and product features;
2. establish legal and contractual posture;
3. document privacy and security baselines;
4. define AI and data-use boundaries;
5. resolve research and IRB boundaries;
6. assemble the scoped client, institutional, or funder readiness packet; and
7. institute recurring review.

## 21. Claims control

No one working under this Canon may knowingly:

- present a design as implemented;
- present main-branch code as deployed;
- present deployed infrastructure as enabled;
- present beta behavior as production assurance;
- present a gated feature as available;
- present a draft as policy;
- present a checklist as completed compliance;
- present a framework mapping as certification;
- present a reviewer recommendation as SpiralWe authorization;
- present an intended protection as a tested control;
- present grant planning as awarded funding or funded capability;
- present de-identification as established without documented method and review; or
- use “compliant,” “approved,” “secure,” “validated,” “research ready,” or “institution ready” without scope and evidence.

If a claim cannot be supported, it must be narrowed, qualified, deferred, or withdrawn.

## 22. Review cadence and change control

This Canon should be reviewed:

- quarterly;
- before a new institutional pilot or contract;
- before a grant or government-funding submission containing material capability claims;
- before enabling learner- or child-facing capability;
- before a new category of data use or externalization;
- before research, publication, or cross-participant analysis;
- after a material AI model, vendor, infrastructure, policy, or product change;
- after a security, privacy, safety, or research incident; and
- when controlling law, contract, or professional guidance changes.

Changes to the Canon require a documented proposal, rationale, affected requirements, owner, reviewer, approval, effective date, and migration or supersession note. Editing this document does not itself approve a product, legal, policy, or operational change.

## 23. Explicit non-claims

This Canon does not claim:

- FERPA, COPPA, HIPAA, GDPR, or state-law compliance;
- legal sufficiency of any notice, policy, consent, or agreement;
- security certification or complete control effectiveness;
- district, university, agency, or procurement readiness;
- IRB approval, exemption, or non-applicability;
- medical-device or clinical-framework non-applicability;
- accessibility conformance;
- grant eligibility, award, allowability, or audit readiness;
- production availability of beta, gated, designed, or planned capability; or
- that all evidence gaps have been identified.

Those conclusions require current evidence and the authority identified in this Canon.

## 24. Adoption and next artifacts

This draft becomes an operating Canon only when SpiralWe designates:

- an executive owner;
- document approver;
- effective date;
- review cadence;
- repository and evidence-control rules;
- initial risk acceptance authority; and
- qualified escalation contacts.

The next supporting artifacts should implement this Canon through:

- a requirements matrix;
- evidence register;
- gap register;
- risk register;
- readiness gates;
- current-state assessment;
- client, institutional, grant, and research readiness assessments;
- phased roadmap; and
- reusable claim-evidence and due-diligence templates.

Until adoption, this document is a structured proposal for review. Its draft status must remain visible.

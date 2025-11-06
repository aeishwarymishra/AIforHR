```mermaid
flowchart LR
  A[Workforce Planning] --> B[Attraction & Sourcing]
  B --> C[Screening & Hiring]
  C --> D[Onboarding & Enablement]
  D --> E[Performance & Development]
  E --> F[Retention & Engagement]
  F --> G[Succession & Exit]
```
Hiring journey with Mantrika (sequence)
```mermaid
sequenceDiagram
  participant CA as Candidate
  participant CS as Careers Site
  participant RE as Recruiter
  participant MA as Mantrika
  participant AT as ATS
  participant HM as Hiring Manager
  participant LM as LMS

  CA->>CS: View role, start application
  CS->>MA: Send profile signals (consented)
  MA-->>CS: SWTT-aligned content & questions

  CA->>AT: Submit application
  AT->>MA: Sync application data
  MA-->>RE: Ranked shortlist + explain-why

  RE->>HM: Share shortlist
  HM->>MA: Define must-have tasks/skills
  MA-->>RE: Interview plan + scorecards

  RE->>CA: Schedule interviews
  HM->>MA: Submit feedback
  MA-->>RE: Aggregate SWTT + bias checks

  alt Strong fit
    RE->>CA: Extend offer
    MA-->>RE: Offer acceptance likelihood
  else Needs development
    MA-->>RE: Upskilling path + alt candidates
  end

  CA->>AT: Accept offer
  AT->>MA: Create onboarding plan
  MA-->>LM: Push targeted learning tasks



```
SWTT dataflow and surfaces (flowchart)
```mermaid
flowchart TD
  A[Sources: HRIS ATS LMS Projects Surveys] --> B[Ingest and Clean]
  B --> C[Embeddings and Feature Store]
  C --> D[SWTT Engine: Skill Will Task Time]
  D --> E[Scores and Explanations]
  E --> F[APIs and Webhooks]
  F --> G[Recruiting Dashboard]
  F --> H[Manager Console]
  F --> I[Employee App]
  F --> J[BI Tools and Data Warehouse]

```

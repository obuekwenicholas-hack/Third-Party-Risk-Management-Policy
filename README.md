# Third-Party Risk Management Program – MedCore Health

## Project Overview

This project is a Third-Party Risk Management (TPRM) program built for **MedCore Health**, a fictional mid-size healthcare SaaS company subject to HIPAA requirements. MedCore Health processes sensitive patient data and relies on multiple third-party vendors to support cloud infrastructure, customer relationship management, internal communications, video conferencing, e-signatures, and payment processing.

The purpose of this project is to demonstrate how a GRC analyst can assess vendor risk, classify vendors by risk tier, evaluate security controls, document findings, create remediation plans, and establish an ongoing vendor monitoring process.

This project mirrors real-world vendor risk management activities commonly performed by Governance, Risk, and Compliance teams.

## Scenario

MedCore Health uses six third-party vendors for core business operations:

| Vendor          | Service Provided                 | Data Access   | Risk Tier |
| --------------- | -------------------------------- | ------------- | --------- |
| CloudHost Inc.  | Cloud Infrastructure             | PHI + PII     | Critical  |
| CRM Pro         | Customer Relationship Management | PII           | High      |
| CollabTools     | Internal Communications          | Internal Only | Medium    |
| VideoMeet       | Video Conferencing               | Minimal       | Low       |
| DocSign Co.     | E-Signatures                     | Contract Data | Medium    |
| PayProcess Ltd. | Payment Processing               | PCI Data      | High      |

Each vendor was assessed based on the type of data accessed, business criticality, compliance requirements, and potential operational impact to MedCore Health.

## Project Objectives

The main objectives of this project were to:

* Build a vendor inventory for all third-party service providers
* Classify vendors into Critical, High, Medium, and Low risk tiers
* Create a structured vendor risk questionnaire
* Assess vendors across key security and compliance domains
* Score vendor responses using a defined risk scoring model
* Identify control gaps and document remediation plans
* Establish a vendor reassessment schedule based on risk tier
* Write a formal Third-Party Risk Management policy

## Key Deliverables

This repository includes the following deliverables:

| Deliverable         | Description                                                                                                                      |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| Vendor Inventory    | Tracks vendor name, service provided, data classification, business criticality, certifications, contract dates, and risk rating |
| Risk Questionnaire  | Contains vendor security questions across access control, data security, incident response, business continuity, and compliance  |
| Risk Scoring Model  | Scores vendor responses and assigns overall risk ratings                                                                         |
| Risk Treatment Plan | Documents control gaps, risk response, remediation actions, owners, and target dates                                             |
| Review Schedule     | Defines how often vendors are reassessed based on risk tier                                                                      |
| TPRM Policy         | Formal policy covering vendor onboarding, due diligence, monitoring, incident notification, and offboarding                      |
| Screenshots         | Evidence of completed project tabs and policy documentation                                                                      |

## Vendor Risk Domains

The vendor questionnaire evaluates vendors across five major domains:

### 1. Access Control

This domain reviews whether vendors enforce secure access practices such as multi-factor authentication, least privilege, access reviews, and user provisioning controls.

Example questions:

* Is MFA enforced for all users?
* Are access rights reviewed on a regular basis?
* Is least privilege applied to user accounts?

### 2. Data Security

This domain evaluates how vendors protect sensitive data throughout its lifecycle.

Example questions:

* Is data encrypted at rest?
* Is data encrypted in transit using TLS?
* Does the vendor classify and protect sensitive data?

### 3. Incident Response

This domain assesses whether vendors can detect, respond to, and report security incidents.

Example questions:

* Does the vendor have a documented incident response plan?
* What is the vendor’s breach notification timeline?
* Has the vendor experienced a breach in the last three years?

### 4. Business Continuity

This domain reviews the vendor’s ability to continue operations during outages, disasters, or major disruptions.

Example questions:

* Does the vendor maintain a disaster recovery plan?
* Has the disaster recovery plan been tested in the last 12 months?
* What are the vendor’s RTO and RPO targets?

### 5. Compliance

This domain reviews whether vendors maintain relevant security and privacy certifications.

Example questions:

* Does the vendor have a SOC 2 Type II report?
* Is the vendor ISO 27001 certified?
* Does the vendor comply with HIPAA, PCI DSS, or other applicable requirements?

## Risk Scoring Methodology

Vendor responses were scored using the following model:

| Response                    | Score | Meaning                            |
| --------------------------- | ----: | ---------------------------------- |
| Yes, with evidence          |     0 | Control confirmed; no risk added   |
| Yes, no supporting evidence |     1 | Control claimed but not verified   |
| Partial                     |     2 | Control gap exists                 |
| No                          |     3 | Control is absent; risk is present |
| N/A                         |     0 | Not applicable to this vendor      |

Scores were totaled by domain and by vendor. The overall score determined the vendor’s final risk rating.

| Total Score | Risk Rating |
| ----------: | ----------- |
|        0–10 | Low         |
|       11–20 | Medium      |
|       21–30 | High        |
|         31+ | Critical    |

This scoring model helps prioritize vendors based on the level of risk they introduce to MedCore Health.

## Vendor Classification Criteria

Vendors were classified using the following criteria:

| Risk Tier | Classification Criteria                                                                                                                    |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Critical  | Vendor processes PHI, supports mission-critical operations, has privileged access, or could severely disrupt MedCore Health if unavailable |
| High      | Vendor processes PII, PCI, or sensitive business data and has a significant security or compliance impact                                  |
| Medium    | Vendor has access to internal or confidential data but does not support mission-critical operations                                        |
| Low       | Vendor has minimal data access and limited operational impact                                                                              |

This classification approach helps determine the depth of due diligence, approval requirements, and reassessment frequency for each vendor.

## Due Diligence Requirements

Before onboarding vendors, MedCore Health requires due diligence based on the vendor’s risk tier.

Critical and High vendors require a full assessment, including:

* Completed vendor security questionnaire
* SOC 2 Type II report or equivalent evidence
* HIPAA Business Associate Agreement, if applicable
* PCI DSS evidence, if payment data is processed
* Incident response documentation
* Business continuity and disaster recovery documentation
* Encryption and access control evidence
* Subprocessor review
* Contractual security and privacy terms

Medium vendors require an abbreviated questionnaire and targeted evidence review.

Low vendors may only require a basic self-attestation or limited review.

## Ongoing Monitoring

Vendors are reassessed based on their assigned risk tier:

| Risk Tier | Review Frequency                         | Assessment Type                        |
| --------- | ---------------------------------------- | -------------------------------------- |
| Critical  | Annually and after any security incident | Full questionnaire and evidence review |
| High      | Annually                                 | Full questionnaire                     |
| Medium    | Every 2 years                            | Abbreviated questionnaire              |
| Low       | Every 3 years                            | Self-attestation only                  |

Ongoing monitoring ensures vendor security controls remain effective over time and helps identify changes in vendor risk posture.

## Risk Treatment Plan

For each control gap identified during the assessment, a risk treatment plan was created. Each finding includes:

* Finding ID
* Vendor name
* Risk domain
* Finding description
* Risk response
* Recommended remediation action
* Risk owner
* Target remediation date
* Status

Risk responses include:

| Response | Meaning                                                                |
| -------- | ---------------------------------------------------------------------- |
| Accept   | Acknowledge and accept the risk                                        |
| Mitigate | Reduce the risk through remediation                                    |
| Transfer | Shift risk through insurance, contract terms, or vendor responsibility |
| Avoid    | Discontinue or avoid the vendor relationship                           |

## Incident Notification Requirements

Vendors must notify MedCore Health of any actual or suspected security incident that may impact MedCore Health data, systems, customers, or operations.

Vendor incident notifications should include:

* Date and time of discovery
* Description of the incident
* Data or systems impacted
* Whether MedCore Health data was affected
* Containment actions taken
* Root cause, if known
* Remediation plan
* Vendor incident response contact

For vendors processing PHI, notification expectations must align with HIPAA and any Business Associate Agreement requirements.

## Vendor Offboarding

When a vendor relationship ends, MedCore Health must safely terminate the relationship by:

* Removing user accounts and system access
* Disabling API keys and integrations
* Confirming return or secure deletion of MedCore Health data
* Obtaining written data destruction attestation, when applicable
* Reviewing open risks and contract obligations
* Ensuring business continuity plans are in place
* Closing vendor records in the inventory

This process helps prevent unauthorized access, data retention issues, and compliance gaps after a vendor relationship ends.

## Tools Used

* Google Sheets
* Google Docs
* Public vendor trust/security pages
* Cloud Security Alliance CAIQ Lite
* GitHub

## Skills Demonstrated

This project demonstrates the following GRC and cybersecurity skills:

* Third-party risk management
* Vendor risk assessment
* Vendor inventory management
* Risk tiering and classification
* Security questionnaire development
* Control gap analysis
* Risk scoring and prioritization
* Risk treatment planning
* Policy writing
* HIPAA-aware vendor governance
* Evidence collection and documentation
* Ongoing monitoring and reassessment planning

## Project Screenshots

Recommended screenshots to include in this repository:

* Vendor Inventory tab showing all six vendors
* Risk Questionnaire tab showing assessment questions and responses
* Risk Scoring tab with color-coded risk ratings
* Risk Treatment Plan tab with remediation actions
* Review Schedule tab showing reassessment cadence
* TPRM Policy document first page
* Example vendor trust page used for research

## What I Learned

Through this project, I gained hands-on experience building a complete vendor governance process from the ground up. I learned how to classify vendors based on data access and business criticality, assess vendor security controls, identify gaps, document remediation actions, and create a policy that supports the full vendor lifecycle.

This project strengthened my understanding of how GRC teams manage third-party risk in regulated environments, especially healthcare organizations that must protect PHI, PII, PCI data, and confidential business information.

## Resume Bullet Example

Assessed six third-party vendors across five security domains using a structured vendor risk questionnaire, classified vendors into four risk tiers, identified control gaps, and developed risk treatment plans to support HIPAA-aware vendor governance for a simulated healthcare SaaS environment.



## Disclaimer

This is a fictional portfolio project created for learning and demonstration purposes. MedCore Health and the vendor names used in this project are fictional. This project does not represent a real company assessment or actual vendor risk review.

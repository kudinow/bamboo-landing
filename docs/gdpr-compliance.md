# GDPR Compliance Policy

**Last Updated: May 1, 2026**

This document describes how "Sunction" Limited Liability Partnership ("Yumisa", "we", "us", or "our") complies with the General Data Protection Regulation (EU) 2016/679 ("GDPR"), the UK GDPR + Data Protection Act 2018, and the EU Artificial Intelligence Act (Regulation (EU) 2024/1689, "EU AI Act"), in relation to the Yumisa mobile application ("App").

This document complements our **Privacy Policy**. Where the two differ, the Privacy Policy controls; this document provides additional GDPR-specific information.

---

## 1. Data Controller

**Data Controller:** "Sunction" Limited Liability Partnership
**Address:** 133/1 Gagarin Avenue, Office 104, Bostandyk District, Almaty 050060, Republic of Kazakhstan
**Email:** support@bureau613.com

**Data Protection Officer (DPO).** "Sunction" Limited Liability Partnership has not formally designated a Data Protection Officer pursuant to Article 37 GDPR, as the company does not currently meet the mandatory criteria set out in Article 37(1) (public authority; large-scale regular and systematic monitoring; large-scale processing of special categories of data). We will reassess this status on an ongoing basis. In the meantime, the Yumisa Privacy Team serves as the primary point of contact for data-protection matters and may be contacted at **support@bureau613.com**.

## 2. Contact for EU and UK Data Subjects

EU and UK residents may exercise their rights under the GDPR and UK GDPR by contacting "Sunction" Limited Liability Partnership directly at **support@bureau613.com**. We respond to verified requests within the timeframes required by law (typically one month, with up to a two-month extension for complex requests, with prior notice). You may also lodge a complaint with your local supervisory authority — see §12 for contact details.

## 3. Lawful Bases for Processing

| Processing Activity | Lawful Basis (Art. 6) | Details |
|---------------------|----------------------|---------|
| Account creation & authentication | Contract (Art. 6(1)(b)) | Necessary to provide the Service |
| Food photo / text / audio analysis | Contract (Art. 6(1)(b)) + Explicit Consent (Art. 9(2)(a)) for special-category data | Core functionality of the App; explicit consent obtained at onboarding for health data |
| Subscription & payment processing | Contract (Art. 6(1)(b)) | Necessary to manage subscriptions |
| Push notifications (reminders) | Consent (Art. 6(1)(a)) | User can opt-in / out at any time |
| Marketing emails | Consent (Art. 6(1)(a)) | Granular opt-in (product updates separate from promotional offers); double opt-in for EU |
| Analytics (pseudonymous) | Legitimate Interest (Art. 6(1)(f)) | Improving App performance and UX; balancing test documented; opt-out available |
| AI model improvement | Consent (Art. 6(1)(a)) + Explicit Consent (Art. 9(2)(a)) | Using pseudonymised data only; opt-in / opt-out via Settings |
| Fraud prevention & security | Legitimate Interest (Art. 6(1)(f)) | Protecting users and the Service |
| Legal compliance | Legal Obligation (Art. 6(1)(c)) | Tax, fraud prevention, legal requests, breach notification |

### 3.1 Special Category Data (Art. 9)
The App processes **health-related data** (dietary intake, nutritional goals, body metrics, food photos that may reveal health conditions). Processing of special category data is based on:
- **Explicit consent** (Art. 9(2)(a)) — obtained during onboarding through a clear, separate consent screen
- Users can withdraw consent at any time by deleting their account or updating consent preferences in Settings → Privacy

We document explicit-consent capture (timestamp, IP, consent text version) for audit purposes.

## 4. Data Processing Agreements

We have Data Processing Agreements (DPAs) in place with all sub-processors. The current list of sub-processors:

| Sub-processor | Purpose | Location | DPA Status |
|---------------|---------|----------|------------|
| Amazon Web Services, Inc. (AWS) | Cloud hosting & storage | Frankfurt, Germany (AWS eu-central-1 region) | Signed |
| OpenAI, L.L.C. | Food recognition AI (image) | USA (EU-US Data Privacy Framework certified; SCCs signed) | Signed |
| Anthropic, PBC | Food recognition AI (text/voice) | USA (EU-US Data Privacy Framework certified; SCCs signed) | Signed |
| Adjust GmbH | Attribution, fraud detection, pseudonymous analytics | Berlin, Germany (EU) | Signed (Adjust Standard DPA, SCCs for non-EU data flows) |
| Adapty | Subscription management | USA (EU-US Data Privacy Framework certified; SCCs signed) | Signed |
| Apple / Google | Payment processing | USA | Platform terms |
| Intercom Inc. | Customer support | EU or US (with DPF / SCCs) | Signed |

The list is published and kept current at: **yumisa.app/sub-processors**

## 5. Data Subject Rights (Articles 15-22)

We support all GDPR data subject rights:

### 5.1 Right of Access (Art. 15)
Users can request a full copy of their personal data. Delivered within **1 month** in JSON or CSV format (extendable by 2 months for complex requests with notice).

### 5.2 Right to Rectification (Art. 16)
Users can update their profile data directly in the App (Settings → Profile) or by contacting support@bureau613.com.

### 5.3 Right to Erasure (Art. 17)
Users can delete their account in the App: **Settings → Account → Delete Account**. This triggers:
- Removal of personal data from active systems within 30 days
- Removal from backups within 60 days
- Retention only of: (a) anonymised / aggregated data not linkable to the user; (b) records required by law (tax, accounting); (c) records needed for legal claims

### 5.4 Right to Data Portability (Art. 20)
Users can export their data (food diary, nutritional history, profile) in a structured, machine-readable format (JSON / CSV) via the App or by request.

### 5.5 Right to Restriction (Art. 18)
Users can request restriction of processing while a complaint is being resolved.

### 5.6 Right to Object (Art. 21)
Users can object to processing based on legitimate interests (analytics, AI improvement). We will cease processing unless we demonstrate compelling legitimate grounds, and we will inform you of the outcome.

### 5.7 Automated Decision-Making and Profiling (Art. 22)
Yumisa uses automated processing (AI) to estimate the nutritional content of food. We do not believe this constitutes "automated decision-making producing legal or similarly significant effects" within the meaning of Art. 22, because the output is informational and you remain in control of all dietary decisions.

Nonetheless, you have the right to:
- Request a **human review** of any specific result
- Object to AI-based processing
- Receive a plain-language explanation of how our AI works and its limitations (typical accuracy ±15-25%, depends on photo quality, food complexity, ingredient visibility)

## 6. Data Protection by Design and Default (Art. 25)

- **Data minimisation:** We only collect data necessary for the Service. We do not collect precise location, contacts, photos beyond food, or browsing history.
- **Privacy by default:** Tracking, marketing, and AI-training are opt-in (or opt-out where required), not opt-out by default.
- **Pseudonymisation:** Food photos used for AI training have personal identifiers removed before being entered into the training pipeline.
- **Encryption:** All data encrypted in transit (TLS 1.2+) and at rest (AES-256).
- **Access controls:** Role-based, principle of least privilege, comprehensive audit logging.
- **Data retention limits:** Specific periods defined per data category (see Privacy Policy, Section 5).

## 7. Data Breach Notification (Art. 33-34)

In the event of a personal data breach:
- We will notify the relevant supervisory authority within **72 hours** of becoming aware of the breach (GDPR Art. 33)
- We will notify affected users without undue delay if the breach poses a high risk to their rights and freedoms (GDPR Art. 34)
- We will also comply with the FTC Health Breach Notification Rule (60-day notification) for US users
- We maintain an internal breach register documenting all incidents, root cause, mitigation, and follow-up

## 8. International Transfers (Art. 44-49)

For transfers outside the EU/EEA, we rely on:
- **EU-US Data Privacy Framework (DPF)** — for transfers to DPF-certified US recipients (validated by the EU Court of Justice in 2025; subject to ongoing legal review)
- **Standard Contractual Clauses (SCCs)** — EU Commission Decision 2021/914, with **supplementary measures** as recommended by EDPB Recommendation 01/2020 (encryption, pseudonymisation, contractual safeguards) following Schrems II
- **Adequacy decisions** — where applicable
- **UK transfers:** UK International Data Transfer Agreement (UK IDTA) or UK Addendum to EU SCCs
- **Brazil:** ANPD-approved Standard Contractual Clauses (mandatory from 23 August 2025)

We perform Transfer Impact Assessments (TIAs) for transfers to third countries without an adequacy decision and document supplementary measures.

## 9. Children's Data

Yumisa is intended for users 16 years of age or older worldwide.

We recognise that the digital age of consent under Art. 8 GDPR varies by Member State (UK 13; FR 15; ES 13; IT 14; SE/DK/EE/FI/LV/LT/MT/PL/PT 13-15; DE/NL 16). Our default minimum age of 16 satisfies the strictest national threshold.

In jurisdictions where the digital age of consent is below 16, users between the local digital age of consent and 16 may use Yumisa only with verifiable parental or guardian consent.

If we discover that a user below the applicable age has registered without proper consent, we delete their data promptly. See our separate **COPPA Policy** for US-specific children's privacy procedures.

## 10. Data Protection Impact Assessment (DPIA)

Given the processing of health data and AI-based analysis, we have conducted a DPIA as required by Art. 35 GDPR. The DPIA covers:
- Nature, scope, context, and purposes of processing
- Necessity and proportionality assessment
- Risks to rights and freedoms of data subjects
- Mitigation measures and residual risk

Key findings (high-level):

| Risk | Mitigation |
|------|------------|
| Health data exposure | Encryption (TLS 1.2+ in transit, AES-256 at rest); access controls; signed DPAs with all processors; no sharing for advertising |
| AI bias in food recognition | Regular model auditing, balanced training data, user feedback mechanism, transparency about accuracy (±15-25%) |
| Third-party data leakage | DPAs, regular security assessments, sub-processor approval workflow, data minimisation |
| Cross-border transfers | DPF where available; SCCs + supplementary measures (TIA documented); UK IDTA |
| AI training on user content | Pseudonymisation before training; opt-out available; consent logged |
| Special category data (health) | Explicit consent (Art. 9(2)(a)) captured at onboarding with version history |

The full DPIA is maintained internally and available to supervisory authorities upon request.

## 11. EU AI Act (Regulation (EU) 2024/1689)

Yumisa is an **AI system** within the meaning of the EU AI Act. We classify the food-recognition functionality as a **limited-risk AI system** (it provides nutritional estimates without producing automated decisions with legal or similarly significant effects).

We comply with applicable transparency obligations (Art. 50 EU AI Act), in force from 2 August 2026:
- We disclose to users that they are interacting with an AI system
- We explain in plain language the purpose, capabilities, and limitations of the system, including typical accuracy ranges
- We do not deploy AI techniques considered prohibited under Art. 5 EU AI Act
- We maintain technical documentation supporting our risk classification
- We monitor the EU AI Office's evolving guidance and reclassify if our use case materially changes

If we expand into clinical, diagnostic, or therapeutic functionality, we will reassess classification (potentially as a high-risk AI system) and implement Art. 9-15 EU AI Act obligations before deploying.

## 12. Record of Processing Activities (Art. 30)

A detailed Record of Processing Activities (ROPA) is maintained internally, structured per Art. 30(1) categories (controller / DPO / processing purposes / data subjects / data categories / recipients / transfers / retention / security measures), and is available to supervisory authorities upon request.

## 13. Contact and Complaints

- **Privacy inquiries:** support@bureau613.com
- **DPO:** Yumisa Privacy Team (no formal DPO designated; not required under Art. 37(1) GDPR) — support@bureau613.com
- **EU Representative:** support@bureau613.com
- **UK Representative:** support@bureau613.com
- **Supervisory Authority (EU):** Users in the EU may lodge complaints with their local Data Protection Authority. A list is available at: https://edpb.europa.eu/about-edpb/about-edpb/members_en
- **Supervisory Authority (UK):** Information Commissioner's Office (ICO), https://ico.org.uk

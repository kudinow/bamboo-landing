# COPPA Compliance Policy

**Last Updated: May 1, 2026**

This document describes how "Sunction" Limited Liability Partnership ("Yumisa", "we", "us", or "our") complies with the Children's Online Privacy Protection Act ("COPPA"), 15 U.S.C. §§ 6501-6506, and the FTC's Children's Online Privacy Protection Rule, 16 C.F.R. Part 312, as amended in January 2025 (effective June 23, 2025; full compliance by April 22, 2026), in relation to the Yumisa mobile application ("App").

---

## 1. Overview

COPPA is a United States federal law that protects the privacy of children under 13 years old. It requires operators of websites and online services (including mobile apps) directed at children — or that knowingly collect information from children under 13 — to comply with specific requirements regarding notice, parental consent, data minimization, security, and retention.

The 2025 update to the COPPA Rule expanded the definition of "personal information" to explicitly include **biometric identifiers** (such as facial geometry from photos and voiceprints), and introduced **separate verifiable parental consent** requirements for disclosing children's data to third parties for advertising or AI/ML training.

## 2. Age Restriction

**Yumisa is NOT directed at children under 16.**

The App:
- Is designed for users aged **16 and older** worldwide (this aligns with our global eligibility threshold — see Terms of Use, Section 1)
- Requires age verification during account registration
- Does not target children in its marketing, content, or visual design
- Does not use characters, activities, or visual elements primarily appealing to children under 13
- Does not feature ads or content specifically directed at children

Because we do not direct our service to children under 13 and require all users to be 16+, we do not knowingly collect personal information from children under 13.

## 3. Age Gate Implementation

During onboarding, the App implements an age gate:
- Users must enter their **date of birth** (not just age)
- If the user is under 16, account creation is blocked
- The message displayed: *"Sorry, you must be at least 16 years old to use Yumisa."*
- We **do not retain** the date of birth entered by underage users who are blocked, beyond what is needed to enforce the block (a hashed device-level flag prevents immediate retry)

**Anti-Circumvention.** If we later detect through behavioural signals or user reports that an account holder appears to be under 16, we will:
1. Suspend the account
2. Request age re-verification (via parental email or government-ID flow)
3. Terminate the account if age cannot be verified at 16+

## 4. No Knowing Collection from Children

We do not knowingly collect, use, or disclose personal information from children under 13 (or under 16, our global threshold). If we learn that we have inadvertently collected personal information from a child under our age threshold:

1. We will **immediately delete** the child's personal information from our active systems and from backups within 60 days
2. We will **terminate** the child's account
3. We will **notify** the child's parent or legal guardian if we have sufficient contact information
4. We will document the incident in our internal Children's Privacy Incident Log

## 5. Parental Rights and Verifiable Parental Consent

If you are a parent or legal guardian and believe your child has provided personal information to us, contact us at support@bureau613.com with:
- Your name and contact information
- Your child's name, account email or username
- Confirmation of your relationship to the child

We will:
- **Acknowledge your request within 5 business days**
- **Verify your identity** using one of the FTC-approved verifiable parental consent methods (e.g., signed consent form via email, government-issued ID + facial verification, knowledge-based authentication, or video conference with a trained representative)
- **Investigate within 10 business days** of identity verification
- **Delete** any information associated with the child's account
- Confirm completion in writing

You may also:
- **Review** the personal information we have collected from your child
- **Refuse** to permit further collection or use of your child's information
- **Receive** a copy of your child's data in a portable format

## 6. Third-Party SDKs

The following third-party services integrated in the App have COPPA-compliant configurations:

| Service | Purpose | COPPA Compliance |
|---------|---------|-----------------|
| Apple App Store | Distribution & payments | Apple's Developer Program License Agreement requires COPPA compliance; we declare the App as not made for kids |
| Google Play | Distribution & payments | Configured outside Google's Designed for Families program; we declare the App as not targeted at children |
| Adjust GmbH (Berlin, Germany) | Attribution, fraud detection, and pseudonymous analytics | SDK configured to disable behavioural tracking, advertising identifiers (IDFA / GAID), and persistent identifiers for users below our age threshold; signed Adjust Standard DPA with child-data safeguards |
| Adapty | Subscription management | Does not independently collect children's data; data limited to subscription metadata |
| AI providers (food recognition) | Image / text / audio analysis | Bound by data processing agreements; do not retain content beyond processing window |

We do not integrate any SDK that targets children's advertising networks (e.g., COPPA-compliant kids networks like SuperAwesome). We do not run targeted advertising in Yumisa.

## 7. App Store and Google Play Declarations

### 7.1 Apple App Store
In App Store Connect we declare:
- The App is **not** made for kids (Made for Kids: No)
- Age rating: **12+** (recommended: 12+ or 17+ depending on health/body content)
- Privacy Nutrition Label accurately reflects all data collection
- App Tracking Transparency: we request permission only where required and never for children's accounts

### 7.2 Google Play
In Google Play Console we declare:
- The App does **not** target children
- The App is **not** part of the Designed for Families program
- Content rating: **Teen** (recommended: Everyone or Everyone 10+)
- Data Safety section accurately reflects all data collection and sharing
- Health Apps Declaration: not a medical device, not for medical use

## 8. Information Security Program for Children's Data

Even though Yumisa is not directed at children under 16, we maintain a written information security program reasonably designed to protect any personal information of users that may inadvertently be collected from children, including:
- Encryption of data in transit (TLS 1.2+) and at rest (AES-256)
- Access controls and audit logs
- Regular security assessments
- Procedures for prompt deletion upon discovery

## 9. Data Retention

We do not knowingly retain personal information of users below our age threshold. Where we have collected such data inadvertently, we delete it as soon as reasonably necessary to fulfil the purpose for which it was collected (typically immediately upon discovery).

## 10. Safe Harbor

"Sunction" Limited Liability Partnership is **not currently** a member of an FTC-approved COPPA Safe Harbor program. We voluntarily comply with COPPA requirements through our internal Children's Privacy Program, which includes the measures described in this policy (age gating, data minimisation, security controls, deletion procedures, and parental rights support).

We will reassess membership in a Safe Harbor program (e.g., kidSAFE, PRIVO, iKeepSafe, ESRB Privacy Certified) if our product expands or if we begin to knowingly serve users below our age threshold.

## 11. Complaints and Regulator Inquiries

Parents and regulators with concerns may contact us through any channel listed in Section 12. Internally, we route children's-privacy complaints to our DPO and document each incident in our Children's Privacy Incident Log.

## 12. Updates

We will update this policy if our practices regarding children's data change, or to reflect changes in COPPA or related laws. Material changes will be reflected in the "Last Updated" date at the top.

## 13. Contact

For questions about our COPPA compliance:
- **Email:** support@bureau613.com
- **Postal address:** 133/1 Gagarin Avenue, Office 104, Bostandyk District, Almaty 050060, Republic of Kazakhstan

For FTC COPPA inquiries: https://www.ftc.gov/legal-library/browse/rules/childrens-online-privacy-protection-rule-coppa

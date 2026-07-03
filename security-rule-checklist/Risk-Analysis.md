# HIPAA Risk Analysis Template for Small Healthcare Practices

Reference: 45 CFR §164.308(a)(1)(ii)(A)

A risk analysis is not optional under HIPAA. It is a required administrative safeguard and the foundation of your entire security program. This template is designed for practices with 1-10 staff. It is intentionally practical, not bureaucratic. A completed version of this document is your primary evidence of compliance with the risk analysis requirement.

---

## Practice Information

| Field | Details |
|---|---|
| Practice Name | |
| Practice Type | (e.g. dental, therapy, med spa, specialty clinic) |
| Number of Staff | |
| Security Official | |
| Date of Analysis | |
| Next Review Date | |
| Completed By | |

---

## Step 1: Scope — Where Does ePHI Live?

List every system, device, and location where electronic Protected Health Information (ePHI) is stored, processed, or transmitted. Be specific. If it touches patient data, it belongs on this list.

| # | System / Device / Location | Type | Vendor / Owner | Notes |
|---|---|---|---|---|
| 1 | EHR System | Software | | e.g. Kareo, DrChrono, Jane App |
| 2 | Microsoft 365 Email | Cloud | Microsoft | Ensure BAA is in place |
| 3 | Staff Laptops | Device | | How many? Managed via Intune? |
| 4 | Staff Mobile Phones | Device | | Are these enrolled in MDM? |
| 5 | Practice Management Software | Software | | Billing, scheduling |
| 6 | Cloud Storage | Cloud | | OneDrive, SharePoint, Google Drive |
| 7 | Physical Files / Paper Records | Physical | | Are these scanned and destroyed or retained? |
| 8 | Telehealth Platform | Software | | Zoom for Healthcare, Doxy.me, etc. |
| 9 | | | | |
| 10 | | | | |

---

## Step 2: Identify Threats and Vulnerabilities

For each asset above, identify realistic threats and the vulnerabilities that could be exploited. Focus on what is actually plausible for a small practice, not theoretical nation-state attacks.

| # | Asset | Threat | Vulnerability | Likelihood (H/M/L) | Impact (H/M/L) |
|---|---|---|---|---|---|
| 1 | Staff Laptops | Theft or loss | No device encryption or remote wipe | | |
| 2 | M365 Email | Phishing attack | No MFA enforced | | |
| 3 | EHR System | Unauthorized access | Shared login credentials | | |
| 4 | Staff Mobile Phones | Unsecured personal device | No MDM enrollment | | |
| 5 | Cloud Storage | Accidental sharing | Overly permissive folder permissions | | |
| 6 | Physical Records | Unauthorized access | Unlocked filing cabinets | | |
| 7 | Telehealth Platform | Patient data interception | No end-to-end encryption | | |
| 8 | Network | Eavesdropping | Unencrypted Wi-Fi in waiting area | | |
| 9 | | | | | |
| 10 | | | | | |

**Likelihood Scale**
- H (High): Likely to occur without controls in place
- M (Medium): Could occur, some controls exist
- L (Low): Unlikely given existing environment

**Impact Scale**
- H (High): Significant patient harm, regulatory penalty, or operational disruption
- M (Medium): Moderate exposure, manageable with prompt response
- L (Low): Minimal impact, easily contained

---

## Step 3: Risk Rating

Combine likelihood and impact to assign an overall risk level to each threat.

| Likelihood | High Impact | Medium Impact | Low Impact |
|---|---|---|---|
| High | Critical | High | Medium |
| Medium | High | Medium | Low |
| Low | Medium | Low | Low |

Add your risk ratings to the table in Step 2 or create a separate consolidated risk register below:

| # | Asset | Threat | Likelihood | Impact | Risk Level | Priority |
|---|---|---|---|---|---|---|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |
| 5 | | | | | | |

---

## Step 4: Current Controls

Document what controls are already in place for each risk identified.

| # | Risk | Existing Control | Control Effective? (Y/N/Partial) | Gap Identified |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |

---

## Step 5: Risk Treatment Plan

For every gap identified in Step 4, document how you will address it, who is responsible, and by when.

| # | Risk | Gap | Remediation Action | Owner | Target Date | Status |
|---|---|---|---|---|---|---|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |
| 5 | | | | | | |

**Treatment Options**
- **Mitigate:** Implement a control to reduce likelihood or impact
- **Accept:** Document the decision to accept the risk (appropriate for low risks only)
- **Transfer:** Shift the risk to a third party (e.g. cyber insurance, vendor BAA)
- **Avoid:** Eliminate the activity or system that creates the risk

---

## Step 6: Business Associate Agreements (BAAs)

List every vendor that handles ePHI on your behalf. Each must have a signed BAA before they access patient data.

| # | Vendor | Service | BAA in Place? | Date Signed | Notes |
|---|---|---|---|---|---|
| 1 | Microsoft | M365 Business Premium | | | Accept via M365 admin portal |
| 2 | EHR Vendor | Electronic Health Records | | | |
| 3 | Billing Company | Medical Billing | | | |
| 4 | Telehealth Platform | Video Consultations | | | |
| 5 | Cloud Backup Provider | Data Backup | | | |
| 6 | | | | | |

---

## Step 7: Sign-Off and Review Schedule

| Field | Details |
|---|---|
| Analysis Completed By | |
| Title | |
| Date | |
| Next Scheduled Review | |
| Trigger for Unscheduled Review | New system, new staff member, security incident, or significant operational change |

---

## Notes and Observations

Use this section to capture anything that does not fit neatly into the tables above: informal observations during the review, staff feedback, vendor conversations, or open questions to follow up on.

---

*Built by TrustGrid Technology. Reference template only. Not legal advice. Completing this template is a starting point, not a guarantee of HIPAA compliance. Engage a qualified professional to review your completed analysis.*

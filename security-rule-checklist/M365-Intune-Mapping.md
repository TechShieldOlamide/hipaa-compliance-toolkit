# Microsoft 365 Business Premium and Intune HIPAA Control Mapping

**Reference:** 45 CFR Part 164 Subpart C (HIPAA Security Rule)
**Stack:** Microsoft 365 Business Premium, Microsoft Intune, Microsoft Entra ID
**Applies To:** Small healthcare practices (1-10 staff) running M365 as their primary workplace platform
**Review Frequency:** Annually or after any major M365 configuration change

---

## Purpose

This document maps Microsoft 365 Business Premium and Intune features to specific HIPAA Security Rule requirements. It is designed for small practices that have adopted M365 as their core platform and need to understand which controls M365 satisfies natively, which require configuration, and which require action outside of M365.

---

## How to Read This Document

| Column | Meaning |
|---|---|
| HIPAA Requirement | The specific safeguard from 45 CFR Part 164 |
| M365 / Intune Feature | The Microsoft tool or feature that addresses the requirement |
| Configuration Required | Whether the feature works out of the box or needs to be set up |
| Status | Your practice's current implementation status |
| Notes | Additional guidance or caveats |

**Status Options**
- ✅ Implemented
- 🔄 In Progress
- ❌ Not Implemented
- N/A Not Applicable

---

## Section 1: Administrative Safeguards

| HIPAA Requirement | Ref | M365 / Intune Feature | Configuration Required | Status | Notes |
|---|---|---|---|---|---|
| Risk Analysis | §164.308(a)(1)(ii)(A) | Microsoft Secure Score, Defender for Business vulnerability reports | Yes | | Use Secure Score as a starting point for identifying gaps. Does not replace a full risk analysis. |
| Information System Activity Review | §164.308(a)(1)(ii)(D) | Microsoft 365 Audit Log, Microsoft Purview | Yes | | Enable unified audit logging in the Microsoft 365 compliance portal. Retain logs for minimum 1 year. |
| Security Awareness Training | §164.308(a)(5) | Microsoft Attack Simulator, Viva Learning | Yes | | Attack Simulator sends phishing test emails to staff. Available in M365 Business Premium via Defender. |
| Security Reminders | §164.308(a)(5)(ii)(A) | Microsoft Teams, Outlook | No | | Use Teams announcements or email broadcasts for monthly security reminders. |
| Malware Protection | §164.308(a)(5)(ii)(B) | Microsoft Defender Antivirus, Defender for Business | Yes | | Defender is included in M365 Business Premium. Enable and configure via Intune security policies. |
| Business Associate Agreements | §164.308(b)(1) | Microsoft BAA | No | | Microsoft provides a BAA covering M365 services. Accept via the Microsoft 365 admin center under Settings > Org Settings > Security and Privacy. |

---

## Section 2: Physical Safeguards

| HIPAA Requirement | Ref | M365 / Intune Feature | Configuration Required | Status | Notes |
|---|---|---|---|---|---|
| Workstation Use Policy Enforcement | §164.310(b) | Intune Device Compliance Policies | Yes | | Configure compliance policies to enforce screen lock, encryption, and OS version requirements. |
| Workstation Security (Screen Lock) | §164.310(c) | Intune Configuration Profiles | Yes | | Set automatic screen lock timeout to 10 minutes or less via Intune configuration profile. |
| Device Disposal (Remote Wipe) | §164.310(d)(2)(i) | Intune Remote Wipe | Yes | | Enroll all devices in Intune to enable remote wipe. Test the wipe process on a non-critical device before you need it in a real situation. |
| Device Inventory | §164.310(d)(2)(iii) | Intune Device Inventory | Yes | | All enrolled devices appear in the Intune admin center under Devices. Export regularly for your records. |
| Media Re-use (Device Wipe Before Reuse) | §164.310(d)(2)(ii) | Intune Retire / Wipe | Yes | | Use Intune Retire action to remove company data before reassigning a device to a new staff member. |

---

## Section 3: Technical Safeguards

| HIPAA Requirement | Ref | M365 / Intune Feature | Configuration Required | Status | Notes |
|---|---|---|---|---|---|
| Unique User Identification | §164.312(a)(2)(i) | Microsoft Entra ID (Azure AD) | No | | Every user gets an individual M365 account. Shared accounts are not permitted and must never be created. |
| Emergency Access Procedure | §164.312(a)(2)(ii) | Entra ID Break Glass Account | Yes | | Create a dedicated emergency access account in Entra ID that is excluded from Conditional Access policies. Store credentials securely offline. |
| Automatic Logoff | §164.312(a)(2)(iii) | Intune Configuration Profiles, Entra ID Sign-in Frequency | Yes | | Configure screen lock timeout via Intune. Set sign-in frequency in Entra ID Conditional Access to limit session duration. |
| Encryption at Rest | §164.312(a)(2)(iv) | BitLocker (Windows), FileVault (Mac), Intune Encryption Policy | Yes | | Enforce BitLocker via Intune compliance policy for Windows devices. FileVault enforcement for Mac requires additional configuration in Intune. |
| Multi-Factor Authentication | §164.312(d) | Entra ID Conditional Access, Microsoft Authenticator | Yes | | Create a Conditional Access policy requiring MFA for all users on all apps. This is the single most important technical control in M365. Do not exclude any users. |
| Audit Controls (Audit Logging) | §164.312(b) | Microsoft 365 Unified Audit Log, Microsoft Purview | Yes | | Enable audit logging in the Microsoft Purview compliance portal. Set retention to 1 year minimum. Review logs monthly. |
| Integrity Controls | §164.312(c)(1) | SharePoint Version History, OneDrive Version History | Yes | | Enable versioning on all SharePoint libraries and OneDrive folders containing ePHI. This allows recovery of accidentally modified or deleted files. |
| Transmission Security (Encryption in Transit) | §164.312(e)(1) | Exchange Online TLS, SharePoint HTTPS | No | | M365 encrypts all data in transit by default using TLS. No additional configuration required for basic transmission security. |
| Transmission Encryption (Enhanced) | §164.312(e)(2)(ii) | Microsoft Purview Message Encryption, S/MIME | Yes | | For sending ePHI via email outside the practice, configure Microsoft Purview Message Encryption to automatically encrypt emails containing sensitive content. |
| Access Control (Role-Based) | §164.312(a)(1) | Entra ID Groups, M365 Role-Based Access Control | Yes | | Assign M365 licenses and app permissions based on job role. Use Entra ID security groups to manage access at scale. Review group membership every 6 months. |

---

## Section 4: Key Configuration Checklist

Use this as a quick reference to confirm your M365 tenant is configured for HIPAA compliance.

| # | Configuration Item | Where to Configure | Status |
|---|---|---|---|
| 1 | Accept Microsoft BAA | M365 Admin Center > Settings > Org Settings > Security and Privacy | ☐ |
| 2 | Enable Unified Audit Logging | Microsoft Purview Compliance Portal > Audit | ☐ |
| 3 | Enable MFA for all users via Conditional Access | Entra ID Admin Center > Security > Conditional Access | ☐ |
| 4 | Enforce BitLocker encryption via Intune | Intune Admin Center > Endpoint Security > Disk Encryption | ☐ |
| 5 | Configure automatic screen lock (10 min) via Intune | Intune Admin Center > Devices > Configuration Profiles | ☐ |
| 6 | Enroll all devices in Intune | Intune Admin Center > Devices > Enrollment | ☐ |
| 7 | Enable SharePoint and OneDrive versioning | SharePoint Admin Center > Settings | ☐ |
| 8 | Configure sign-in frequency via Conditional Access | Entra ID Admin Center > Security > Conditional Access | ☐ |
| 9 | Set up Microsoft Defender Antivirus via Intune | Intune Admin Center > Endpoint Security > Antivirus | ☐ |
| 10 | Create emergency access break glass account | Entra ID Admin Center > Users | ☐ |
| 11 | Configure Purview Message Encryption for outbound ePHI email | Microsoft Purview Compliance Portal > Information Protection | ☐ |
| 12 | Run Attack Simulator phishing test for all staff | Microsoft Defender Portal > Email and Collaboration > Attack Simulation Training | ☐ |

---

## Section 5: What M365 Does Not Cover

M365 Business Premium is a strong foundation but it does not cover everything. The following require action outside of M365:

| Gap | What You Need |
|---|---|
| EHR system security | Your EHR vendor must provide their own BAA and security documentation |
| Physical facility security | Door locks, visitor logs, and workstation cable locks are outside M365 scope |
| Staff HIPAA training records | M365 does not maintain training completion records. Use a separate LMS or spreadsheet. |
| Full risk analysis | Microsoft Secure Score is a useful input but does not replace a documented risk analysis |
| Telehealth platform | Your video platform must be HIPAA-compliant and have a signed BAA (e.g. Zoom for Healthcare, Doxy.me) |
| Third party backup for M365 | M365 has built-in redundancy but not a true backup. Use a third party tool with a BAA. |
| Cyber liability insurance | Not a technical control but strongly recommended for small practices |

---

## Sign-Off

| Field | Details |
|---|---|
| Completed By | |
| Role | |
| Date | |
| Next Review Date | |
| M365 Tenant Name | |
| Intune Tenant ID | |

---

*Built by TrustGrid Technology. Reference mapping only. Not legal advice. Microsoft product features and licensing are subject to change. Verify current feature availability in your M365 plan before relying on this document.*

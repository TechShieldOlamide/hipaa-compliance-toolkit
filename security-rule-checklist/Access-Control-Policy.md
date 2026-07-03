# Access Control Policy

**Policy Title:** Access Control Policy
**Reference:** 45 CFR §164.312(a)(1), §164.308(a)(4)
**Applies To:** All staff, contractors, and vendors with access to ePHI
**Review Frequency:** Annually or after any staffing or system change

---

## Purpose

This policy ensures that only authorized individuals can access electronic Protected Health Information (ePHI). Access is granted based on job role and the minimum necessary principle: staff only access what they need to do their job, nothing more.

---

## Scope

This policy applies to all systems that store, process, or transmit ePHI including the EHR system, Microsoft 365, practice management software, and any connected devices.

---

## Policy Rules

### 1. Unique User Accounts
- Every staff member must have their own individual login credentials
- Shared accounts are strictly prohibited
- Generic or group logins (e.g. "front desk@practice.com" used by multiple people) are not permitted

### 2. Role-Based Access
- Access to ePHI is granted based on job role only
- Clinical staff may access clinical records relevant to their patients
- Administrative staff may access scheduling and billing data only
- No staff member should have access beyond what their role requires

### 3. Multi-Factor Authentication (MFA)
- MFA is required for all accounts that access ePHI
- MFA must be enforced via Microsoft Entra ID (formerly Azure AD) Conditional Access for all M365 users
- No exceptions are permitted, including for practice owners or senior staff

### 4. Access Authorization
- All new access requests must be approved by the designated Security Official before provisioning
- Access changes due to role changes must be updated within 24 hours
- Access must be fully revoked on the same day a staff member leaves the practice

### 5. Password Requirements
- Minimum 12 characters
- Must include uppercase, lowercase, numbers, and a special character
- Passwords must not be reused within the last 10 cycles
- Passwords must not be shared with colleagues, written on paper, or stored in unsecured locations
- A password manager is recommended for all staff

### 6. Automatic Session Timeout
- All workstations and devices must be configured to lock automatically after 10 minutes of inactivity
- Staff must manually lock their screen when stepping away from a workstation

### 7. Remote Access
- Remote access to practice systems is permitted only through approved, secured connections
- Personal devices used for remote access must be enrolled in Intune mobile device management
- Public Wi-Fi must not be used to access ePHI without an active VPN connection

---

## Access Review

The Security Official must review all active user accounts and access permissions at least every 6 months and immediately following any staffing change. Accounts that are no longer needed must be disabled or deleted promptly.

---

## Violations

Any staff member found to have violated this policy is subject to disciplinary action as outlined in the Sanction Policy, up to and including termination and referral to regulatory authorities.

---

## Sign-Off

| Field | Details |
|---|---|
| Policy Owner | |
| Security Official | |
| Date Approved | |
| Next Review Date | |

---

*Built by TrustGrid Technology. Reference template only. Not legal advice.*

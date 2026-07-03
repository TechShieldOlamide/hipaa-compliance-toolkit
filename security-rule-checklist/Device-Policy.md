# Device and Media Policy

**Policy Title:** Device and Media Control Policy
**Reference:** 45 CFR §164.310(b), §164.310(c), §164.310(d)
**Applies To:** All staff, contractors, and vendors using devices that access ePHI
**Review Frequency:** Annually or after any device-related incident

---

## Purpose

This policy governs the use, management, and disposal of all devices and media that store, process, or transmit ePHI. Lost, stolen, or improperly disposed devices are one of the most common causes of HIPAA breaches in small practices. This policy reduces that risk.

---

## Scope

This policy applies to all devices including laptops, desktop computers, smartphones, tablets, USB drives, external hard drives, printers, and any other hardware that touches ePHI.

---

## Policy Rules

### 1. Approved Devices
- Only practice-approved devices may be used to access ePHI
- Personal devices may only be used if they are enrolled in Intune mobile device management and approved by the Security Official
- Unenrolled personal devices must never be used to access, store, or transmit ePHI

### 2. Device Enrollment
- All devices approved for ePHI access must be enrolled in Microsoft Intune before use
- Intune enrollment enables remote wipe, encryption enforcement, and compliance policy application
- The Security Official is responsible for maintaining an up to date device inventory

### 3. Device Encryption
- All devices must have full disk encryption enabled
- For Windows devices, BitLocker must be enabled and managed via Intune
- For Mac devices, FileVault must be enabled
- For mobile devices, encryption must be enforced via Intune compliance policy

### 4. Screen Lock and Automatic Timeout
- All devices must be configured to lock automatically after 10 minutes of inactivity
- Staff must lock their screen manually when stepping away from a device
- Biometric or PIN unlock is acceptable for mobile devices enrolled in Intune

### 5. Physical Security
- Laptops must never be left unattended in public spaces including cars, waiting rooms, or coffee shops
- Devices must be stored securely when not in use
- Cable locks are recommended for desktop workstations in shared spaces

### 6. USB and Removable Media
- The use of USB drives and external storage media for ePHI is strongly discouraged
- Where removable media is necessary, only encrypted, practice-approved devices may be used
- USB ports may be disabled on clinical workstations via Intune policy where operationally feasible

### 7. Printing
- Printed documents containing ePHI must not be left unattended
- Printed ePHI must be stored securely and disposed of via cross-cut shredding
- Printers used for ePHI must have access controls and audit logging enabled where the device supports it

### 8. Lost or Stolen Devices
- Any lost or stolen device must be reported to the Security Official immediately
- The Security Official must initiate a remote wipe via Intune within 2 hours of confirmation
- The incident must be logged and assessed for breach notification requirements per the Incident Response Policy

### 9. Device Disposal
- No device may be disposed of, donated, or sold without first confirming that all ePHI has been permanently removed
- Remote wipe via Intune must be completed before disposal
- Physical destruction of storage media is required where remote wipe is not possible
- Disposal must be documented in the device inventory

---

## Device Inventory

The Security Official must maintain a current inventory of all devices approved for ePHI access.

| # | Device Type | Make / Model | Serial Number | Assigned To | Enrollment Status | Encryption Status | Date Added | Notes |
|---|---|---|---|---|---|---|---|---|
| 1 | | | | | | | | |
| 2 | | | | | | | | |
| 3 | | | | | | | | |
| 4 | | | | | | | | |
| 5 | | | | | | | | |

---

## Bring Your Own Device (BYOD)

Small practices sometimes allow staff to use personal devices for work. If BYOD is permitted:

- The device must be enrolled in Intune before any ePHI access is granted
- Staff must acknowledge that the practice may remotely wipe the device if it is lost, stolen, or the staff member leaves
- A signed BYOD acknowledgement form must be retained on file
- BYOD is a risk and should be avoided where practice-owned devices can be provided instead

---

## Violations

Any staff member who uses an unapproved device to access ePHI, fails to report a lost or stolen device, or improperly disposes of a device is subject to disciplinary action as outlined in the Sanction Policy.

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

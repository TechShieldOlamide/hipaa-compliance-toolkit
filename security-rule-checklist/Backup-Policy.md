# Backup and Recovery Policy

**Policy Title:** Data Backup and Recovery Policy
**Reference:** 45 CFR §164.308(a)(7)(ii)(A), §164.308(a)(7)(ii)(B), §164.308(a)(7)(ii)(C)
**Applies To:** All systems that store or process ePHI
**Review Frequency:** Annually or after any data loss incident

---

## Purpose

This policy ensures that ePHI is backed up regularly, that backups are tested, and that the practice can restore access to patient data in the event of a system failure, ransomware attack, accidental deletion, or disaster. A backup that has never been tested is not a backup.

---

## Scope

This policy applies to all systems containing ePHI including the EHR system, Microsoft 365 (email, SharePoint, OneDrive), practice management software, and any local storage containing patient data.

---

## Backup Requirements

### 1. Frequency
- ePHI must be backed up at minimum once every 24 hours
- Real-time or continuous backup is preferred where the system supports it
- Backups must run automatically and not depend on manual action by staff

### 2. Backup Locations
- At least one backup copy must be stored in a separate location from the primary system
- Cloud-to-cloud backup is acceptable (e.g. M365 data backed up to a third party backup service)
- Local-only backups are not sufficient on their own

### 3. Encryption
- All backup copies must be encrypted at rest and in transit
- Encryption keys must be stored separately from the backup data itself

### 4. Retention
- Backup data must be retained for a minimum of 6 years in line with HIPAA retention requirements
- Retention schedules must be configured in the backup system and reviewed annually

---

## System-Specific Backup Configuration

| System | Backup Method | Frequency | Retention | Vendor / Tool | BAA in Place |
|---|---|---|---|---|---|
| EHR System | | | | | |
| M365 Email | | | | | |
| SharePoint / OneDrive | | | | | |
| Practice Management Software | | | | | |
| Local Workstations | | | | | |
| Other | | | | | |

**Note:** Microsoft 365 has built-in redundancy but does not provide a full backup solution by default. A third party M365 backup tool (e.g. Veeam, Acronis, Datto SaaS Protection) is strongly recommended and must have a signed BAA in place.

---

## Backup Testing

A backup that has never been tested cannot be trusted. The Security Official must schedule and document backup restoration tests as follows:

| Test Type | Frequency | Last Tested | Result | Notes |
|---|---|---|---|---|
| File-level restore test | Quarterly | | | Restore a sample of files to confirm integrity |
| Full system restore test | Annually | | | Confirm full recovery is possible |
| EHR data restore test | Annually | | | Confirm patient records are recoverable |

Testing results must be documented and retained. Failed tests must trigger immediate remediation.

---

## Disaster Recovery

In the event of a major system failure or data loss incident:

### Step 1: Declare the Incident
- The Security Official declares a recovery situation and notifies all affected staff
- Normal operations are suspended for affected systems until recovery is complete

### Step 2: Assess the Damage
- Identify which systems and data are affected
- Determine the cause (hardware failure, ransomware, accidental deletion, natural disaster)
- Estimate the recovery time objective (RTO) and recovery point objective (RPO)

### Step 3: Restore from Backup
- Initiate restoration from the most recent clean backup
- Prioritize systems in this order for a typical small practice:
  1. EHR system (patient care continuity)
  2. Practice management software (scheduling and billing)
  3. Microsoft 365 email and communication
  4. Other systems

### Step 4: Verify Integrity
- Confirm restored data is complete and accurate
- Check for any gaps between the last backup and the point of failure
- Document what data, if any, could not be recovered

### Step 5: Resume Operations
- Notify staff that systems are restored and verified
- Document the full incident and recovery process
- Review and update backup configuration to prevent recurrence

---

## Emergency Access to ePHI

If primary systems are unavailable, the practice must have a documented process for accessing critical ePHI during the outage. Options include:

- Contacting the EHR vendor for emergency access procedures
- Accessing the most recent printed or exported patient schedule
- Using a designated backup device with offline access to critical records where the EHR supports this

Document

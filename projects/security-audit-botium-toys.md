# Botium Toys:  Security Audit

## Scope, Goals, Risk Assessment
Scope of the audit is to review the entirety of the security protocols and policies at the fictional company, Botium Toys.  This includes all assets, networks, and systems.  The review is to determine the current controls and compliance practices in place.

The goal is to assess the current controls and compliance practices and see what meets best practices while giving suggestions to improve and meet anything below standard.

Assets:  Equipment for in-office and employees, products, systems, software, services, network, access, retention and storage of data, legacy systems.

Current Risk Score:  8/10 (Very High)

## Checklist
Note:  If a control is in place but inadequate, it will also be considered a 'no'.

### Controls

| Control | Yes | No | Notes |
|------|------|---------|---------|
| Least Privilege | | X | No current access controls to limit access to the least needed for a role, position or group. |
| Disaster Recovery Plans | | X | There are no disaster recovery plans in place or backup policies for critical systems. |
| Password Policies | | X | There is a policy in place but it is insufficient.  It does not meet the minimum standard of eight characters with a combination of uppercase letters, lowercase letters, a number, and a special character. |
| Separation of Duties | | X | There are no access controls to enforce separation of duties or prevent access to unneeded systems by role, position, or group. |
| Firewall | X | | The firewall is present and correctly configured to filter traffic based on security rules. |
| Intrusion Detection System (IDS) | | X | There is no IDS installed. |
| Backups | | X | There is no policy or procedure in place for backups to be created, stored, maintained, tested, or restored, not even for critical systems. |
| Antivirus Software | X | | There is antivirus software installed and it is monitored regularly by the IT department. |
| Manual Monitoring, Maintenance, & Intervention for Legacy Systems | | X | This occurs, but is insufficient. There is no documentation, schedule, or defined response or intervention. |
| Encryption | | X | There is no encryption enforced either at the data storage level or endpoint access level. |
| Password Management System | | X | There is no centralized system detailing password requirements, leading to complications in password resets, etc. |
| Locks (Offices, Storefront, Warehouses) | X | | The physical locks are current and sufficient for the buildings. |
| Closed-Circuit Television (CCTV) Surveillance | X | | The CCTV surveillance is current and sufficient. |
| Fire Detection / Prevention (Fire Alarm, Sprinkler System, Etc.) | X | | Fire detection systems and prevention systems are current and functional. |

### Compliance
### Payment Card Industry Data Security Standard (PCI DSS)

| Best Practice | Yes | No | Notes |
|------|------|---------|---------|
| Only authorized users have access to customers' credit card information | | X | All users have access to all stored data internally. |
| Credit card information is stored, accepted, processed, and transmitted internally, in a secure environment. | | X | No.  Everyone can access the data and it is not encrypted. |
| Implement data encryption procedures to better secure credit card transaction touchpoints and data. | | X | No.  Internal data storage is not encrypted leaving information unsecured. |
| Adopt secure password management policies. | | X | Insufficient.  There are policies in place, but they fail to meet the minimum industry standard of eight characters long, with a combination including at least one each of the following:  uppercase letters, lowercase letters, numbers, and a special character. |

### General Data Protection Regulation (GDPR)

| Best Practice | Yes | No | Notes |
|------|------|---------|---------|
| E.U. customers' data is kept private/secured. | | X | Insufficient.  There have been policies and procedures created and enforced by IT to document and maintain data, but the data is not encrypted leaving it vulnerable. |
| There is a plan in place to notify E.U. customers within 72 hours if their data is compromised/there is a breach. | X | | They have a specific procedure in place for the E.U. to be notified as well as to monitor and document data. |
| Ensure data is properly classified and inventoried. | | X | No.  The inventory is listed, but not classified or categorized. |
| Enforce privacy policies, procedures, and processes to properly document and maintain data. | X | | Yes.  There are specific procedures, policies, and processes enforced by IT to document and maintain data. |

### System and Organizations Controls (SOC Type 1, SOC Type 2)

| Best Practice | Yes | No | Notes |
|------|------|---------|---------|
| User access policies are established. | | X | No access policies are used to monitor access of confidential data or controls based on roles, position, or least privilege. |
| Sensitive Data (PII/SPII) is confidential/private. |  | X | No.  It can be accessed by all employees and is not encrypted. |
| Data integrity ensures the data is consistent, complete, accurate, and has been validated. | X | | The IT department has ensured availability and controls to assure integrity. |
| Data is available to individuals authorized to access it. | | X | While it is available to those authorized to view it, it is not secured and everyone has access to it.  There is no sufficient safeguard to ensure that only authorized individuals have access. |

## Recommendations
1. Update all password policies to modern standards of a minimum of eight characters with a combination of at least one of each of the following:  uppercase letter, lowercase letter, number, and special character.  Institute a centralized password management system.  Document all upgrades, updates, and changes.
2. Establish controls for role-based access and group policies that enforce least privilege and separation of duties.  Document all associated policies and procedures.
3. Create backups and document policies and procedures accordingly.  Schedule regular backups based on how critical the data is. Schedule reviews to test viability of all backups and restoration drills. 
4. Enforce encryption for data in storage using such programs as BitLocker or similar.  Ensure policies and procedures that also enforce classified information to be encrypted in transit as well.
5. Create a disaster response plan and ensure it covers multiple major scenarios such as natural disasters and system compromise.  Schedule at least semi-annual review and tabletop exercises to ensure readiness.
6. Document policies and procedures related to legacy system maintenance, intervention, and escalation.  Create an established policy and procedure for scheduling maintenance and documenting any changes.  Schedule and run drills to ensure readiness in case of need for intervention and escalation.
7. Create policies and procedures to ensure E.U. GDPR standards are met.  Document them.  Apply these globally to save investment of time and funds.
8. Be sure to review local laws and governance to customize beyond the GDPR as needed in all localities.

## Skills Demonstrated
- Security Auditing
- Risk Assessment
- Compliance Assessment
- Security Controls Evaluation
- Technical Documentation
- Security Recommendations

## Project Information
This project is based on the Botium Toys security audit scenario from the Google Cybersecurity Professional Certificate.  All analysis, documentation, formatting, notes, and recommendations were completed independently.

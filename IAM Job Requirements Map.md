
# IAM Skills Map

**Northwind Health | Third-Party App Review**

This map links IAM Analyst job requirements to the work completed in this case study.

| Job Requirement | Evidence in This Project |
|---|---|
| **Access Reviews and Audits** | [01. App Inventory & Current Consent Rules](Documents/01.%20App%20Inventory%20%26%20Current%20Consent%20Rules.md) · [03. Application Access Decisions](Documents/03.%20Application%20Access%20Decisions.md): Reviewed eight applications against their permissions, ownership, usage and business justification. |
| **Access Risk Assessment and Investigation** | [02. App Triage](Documents/02.%20App%20Triage.md): Prioritised three applications by risk and urgency, distinguishing suspected consent phishing from potential exposure and dormant access. |
| **Least Privilege and Access Remediation** | [03. Application Access Decisions](Documents/03.%20Application%20Access%20Decisions.md): Recommended retaining five applications, restricting ExportBot's organisation-wide mailbox access and removing two applications. |
| **Identity Incident Response** | [04. DocuSharePro Response](Documents/04.%20DocuSharePro%20Response.md): Defined an ordered response covering application access revocation, session revocation and investigation across 112 affected accounts. |
| **Identity Governance and Access Lifecycle Management** | [03. Application Access Decisions](Documents/03.%20Application%20Access%20Decisions.md) · [05. Proposed Consent Policy](Documents/05.%20Proposed%20Consent%20Policy.md): Identified gaps in application ownership, credential management, consent approval and ongoing access reviews. |
| **Access Control and Policy Design** | [05. Proposed Consent Policy](Documents/05.%20Proposed%20Consent%20Policy.md): Designed a risk-based consent policy distinguishing low-risk delegated permissions from permissions requiring administrator approval. |
| **Business Impact and Change Planning** | [03. Application Access Decisions](Documents/03.%20Application%20Access%20Decisions.md) · [05. Proposed Consent Policy](Documents/05.%20Proposed%20Consent%20Policy.md): Proposed overlapping credentials during ExportBot's secret rotation and preserved Marketing's access through formal approval. |
| **Security Documentation and Communication** | [Project README](README.md): Communicated access risks, recommended decisions and business implications while distinguishing suspected compromise from confirmed findings. |

<br>

## 🔍 Areas of Interest

- **Microsoft Entra ID:** Testing application consent policies, admin approval workflows and permission revocation in a lab.
- **PowerShell and Microsoft Graph:** Automating application access reviews and identifying excessive permissions, missing owners and ageing credentials.
- **Non-Human Identity Security:** Exploring application identities, credential lifecycle management and least-privilege access.

---

[Back to Project Overview](README.md)

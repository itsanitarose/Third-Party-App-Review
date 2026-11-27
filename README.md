# Third-Party App Review
**IAM skills tested:** reviewing what third-party apps are allowed to do with people’s work accounts, and designing an approval rule that stays secure without breaking the business.

<br>

## 🎫The Ticket
It's 23 November 2026, my **8th week** at Northwind Health.

My manager writes:

> "We've found that anyone at Northwind can connect any app to their work account with one click. I need to know which of the apps connected today worry you, what we do about them, and a rule for the future. Please be careful with Marketing: their email tool pays for itself."

<BR>

**Supporting information:** [App Inventory & Current Consent Rules](Documents/01.%20App%20Inventory%20%26%20Current%20Consent%20Rules.md)

<BR>

<table>
<tr>
<td>
  
**🛡️ Decision**

 **Priority:** [Priority]  
 **Key finding:** [Main finding]  
 **Recommended action:** [What should happen first and why]

</td>
</tr>
</table>
<BR><BR>

## What's the Risk?

Every application should follow an access lifecycle: requests, approvals, ongoing monitoring, regular reviews and timely revocation. The phrases "anyone", "any app" and "with one click" point to a gap in consent and approval. That's a governance gap that could allow excessive application permissions and expose sensitive patient data.

<BR>


## The Investigation

<BR>

I framed my investigation around four questions:

<BR>

1. Which applications present the greatest access risk, and why?
2. Which existing application permissions are justified, excessive or no longer needed?
3. How can we contain suspicious application access and limit potential exposure?
4. How can we govern future application consent without disrupting legitimate business operations?


<BR>

## What I Found

Of the eight applications reviewed, three require priority action.

| Priority | Application | Key Finding |
|---|---|---|
| P1 | DocuSharePro | Suspected OAuth consent phishing, with 112 approvals in four calendar days. With activity peaking over the weekend.
| P2 | ExportBot | Organisation-wide mailbox access, an unchanged secret and no current business owner identified. |
| P3 | PDF Tools Online | Broad file permissions retained despite 190 days of inactivity. |

<BR>

**MailMerge Plus** and **SignFast** appear legitimate, with permissions that align with their respective business functions.

[Full App Triage](Documents/02.%20App%20Triage.md)

<BR> 



## Case Study Outcome

- **Application access:** Keep five applications, restrict ExportBot and remove DocuSharePro and PDF Tools Online. [Access Decisions](Documents/03.%20Application%20Access%20Decisions.md)
- **Incident response:** Contain DocuSharePro, revoke sessions for all 112 affected users and investigate potential data exposure. [DocuSharePro Response](Documents/04.%20DocuSharePro%20Response.md)
- **Consent governance:** Introduce risk-based approvals, accountable ownership and consent alerts while preserving Marketing's business operations. [Proposed Consent Policy](Documents/05.%20Proposed%20Consent%20Policy.md)
  
<BR>




## Reflection & Next Steps

What interested me most about this case was the relationship between access, trust and authority. Northwind had given employees the authority to approve application access without establishing whether they were equipped to assess the consequences of those decisions.

The investigation showed me that risk is rarely defined by a single factor. ExportBot had greater potential for widespread damage, yet DocuSharePro showed stronger signs of an immediate threat: an unverified publisher, no business owner and approvals rising from 6 to 31 to 52 over three days. Meanwhile, HRLink had the largest user count but only basic profile permissions. Context changed the significance of the evidence and, ultimately, my decisions.

DocuSharePro also illustrates the distinction between authentication and authorisation. An identity system can work exactly as intended, verifying the right person through MFA, yet that person may unknowingly grant a malicious application access to sensitive data. **A successfully authenticated user can still make an unsafe authorisation decision. That is why the authority to grant access must itself be governed.**

I also had to consider the consequences of the security controls themselves. Revoking access, restricting permissions or rotating credentials can introduce operational risks if the underlying business dependencies are not understood. ExportBot's nightly reporting and Marketing's reliance on MailMerge Plus required me to balance risk reduction with business continuity.

This is why application access governance requires **judgment at every stage of the access lifecycle:** who can grant access, how much access is justified, who remains accountable for it and when it should be withdrawn.

### Next Step

I would introduce periodic application access reviews to reassess business justification, validate permission scope, confirm ownership and review credential security. Access that is no longer justified should be restricted or revoked.



<BR>


## Explore the Investigation



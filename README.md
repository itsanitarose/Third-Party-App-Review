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


<BR>


## Explore the Investigation



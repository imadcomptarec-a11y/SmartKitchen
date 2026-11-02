---
title: Privacy Policy – SmartKitchen
---

# Privacy Policy – SmartKitchen

_Last updated: November 2, 2026_

This Privacy Policy explains what information **SmartKitchen** (the "App", shown on Google sign-in screens as **"Mailing Agent"**) accesses, how it is used, how it is protected, and what rights you have. It applies to the App and to the related services we provide to restaurant operators.

## 1. Who we are

SmartKitchen is published and operated by **[COMPANY LEGAL NAME]**, [legal form], registered under SIRET **[SIRET NUMBER]**, with its registered office at **[POSTAL ADDRESS]**, France ("we", "us").

Contact for any privacy question or request: **imadcomptarec@gmail.com**

## 2. What the App does

SmartKitchen is a back-office tool for restaurant operators who sell on Uber Eats ("Operators"). It:

- retrieves the Operator's order reports from the **Uber Eats Reporting API**;
- records orders that were cancelled or disputed in the Operator's **own Google Sheets**;
- sends refund requests about those orders to Uber Eats support from the Operator's **own Gmail** mailbox, with supporting files from the Operator's **own Google Drive** when needed;
- reads Uber Eats support's replies in that mailbox to record which refunds were granted, and sends follow-up reminders when there is no answer;
- shows a dashboard of requests sent, refunds obtained and amounts recovered.

The App runs on a computer controlled by us or by the Operator. **There is no SmartKitchen cloud server** that receives or stores Operator data.

## 3. Information the App accesses

### 3.1 Uber Eats data
Through the Uber Eats Reporting API, for the stores the Operator authorises:
- store information: store name, store UUID, external store ID, city, country;
- order information: order ID and UUID, order date and time, order status and delivery status, order amount, cancellation information, workflow UUID;
- operational timings: acceptance, preparation, courier and delivery times.

These reports do **not** contain end-customers' names, addresses, phone numbers or payment details, and the App does not request such data.

### 3.2 Google user data
Only for Google accounts that an Operator explicitly connects through Google's sign-in screen, the App requests these permissions:

| Permission | Scope | Why the App needs it |
|---|---|---|
| Send email | `https://www.googleapis.com/auth/gmail.send` | To send refund requests and follow-up reminders to Uber Eats support from the Operator's mailbox, and to send the Operator a run summary. |
| Read email | `https://www.googleapis.com/auth/gmail.readonly` | To search the mailbox **only for Uber Eats support replies** to the requests the App sent, and read them to determine whether a refund was granted. The App does not read, index or analyse other emails. |
| Google Sheets | `https://www.googleapis.com/auth/spreadsheets` | To read and update the Operator's own spreadsheets listing orders, request status and refund results. |
| Google Drive (read-only) | `https://www.googleapis.com/auth/drive.readonly` | To find and download evidence files (such as photos) that the Operator stored in their own Drive folders, so they can be attached to a refund request. The App never modifies or deletes Drive files. |

### 3.3 Information you give us
When an Operator sets up the App, they may provide business information: restaurant and company names, store addresses, a business contact email address, and the commission rate agreed with us.

### 3.4 Information we do not collect
The App does not use cookies, trackers or analytics, and it does not collect device identifiers, location data, or end-customer personal data.

## 4. How we use information

We use the information above **only** to provide the features described in section 2 to the Operator who authorised it:
- to identify the orders eligible for a refund request;
- to write and send those requests and their follow-ups;
- to detect and record Uber Eats support's answers;
- to compute the amounts recovered and the commission due under our agreement with the Operator;
- to keep the service secure and working (for example, error logs).

We do **not** use any of this information for advertising, marketing, profiling, resale, or to train artificial-intelligence models.

### Automated classification of replies
To decide whether an Uber Eats support reply grants a refund, the App first applies its own keyword rules. If they are not conclusive, the text of **that reply only** may be sent to the **Anthropic API (Claude)**, which returns a "refunded / not refunded" assessment. Anthropic acts as our service provider. Under its commercial terms, it does not use API inputs to train its models. Classification results are always visible to the Operator in their spreadsheet and can be corrected.

## 5. Google API Services – Limited Use disclosure

SmartKitchen's use and transfer to any other app of information received from Google APIs will adhere to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the **Limited Use** requirements. Specifically:

1. Google user data is used only to provide or improve the user-facing features that are prominent in the App and described in this policy.
2. Google user data is not transferred to third parties, except (a) as necessary to provide those features (the Anthropic reply classification described in section 4), (b) to comply with applicable law, or (c) as part of a merger, acquisition or sale of assets, with notice to users.
3. Google user data is not used or transferred for serving advertisements, including personalised or interest-based advertising.
4. Google user data is not sold, and it is not used to determine creditworthiness or for lending purposes.
5. No human reads Google user data, unless (a) the user has given affirmative consent for specific messages, (b) it is necessary for security purposes such as investigating abuse, (c) it is necessary to comply with applicable law, or (d) the data is aggregated and anonymised and used for internal operations.

## 6. Legal bases (GDPR)

When personal data is processed (for example, an Operator's business email address or messages exchanged with Uber Eats support), we rely on:
- **performance of a contract** (Article 6(1)(b) GDPR), to provide the service agreed with the Operator;
- **legitimate interests** (Article 6(1)(f) GDPR), to keep the service secure, prevent abuse and improve reliability;
- **legal obligation** (Article 6(1)(c) GDPR), for accounting and tax records relating to our invoices.

For processing carried out on an Operator's behalf, the Operator remains responsible for its own business data, and we process it according to the Operator's instructions.

## 7. Where data is stored and how it is protected

- **Google access tokens** and App settings are stored locally on the computer running the App, in files readable only by that computer's user account. They are never uploaded to any SmartKitchen server.
- **Order and refund records** are stored in the Operator's own Google Sheets, under the Operator's Google account and its security settings.
- **Uber Eats report files** are downloaded over encrypted connections (HTTPS) to the computer running the App.
- **Uber Eats report notifications** reach the App through an encrypted tunnel (ngrok). Each notification is verified with a cryptographic signature (HMAC-SHA256) before it is processed.
- A **local cache** of reply classifications is kept to avoid processing the same email twice. For each Uber Eats support reply it stores the Gmail message identifier, the "refunded / not refunded" result, a confidence level, the refunded amount, and the short phrase from the reply that justified the result. It does not store the full email.
- All connections to Google, Uber Eats and Anthropic use HTTPS/TLS encryption.

No method of transmission or storage is completely secure. We will notify affected Operators, and the competent authority where required, of any personal data breach as required by law.

## 8. Sharing

We do not sell, rent or trade information. We share information only with the service providers needed to run the App, and only for that purpose:

| Recipient | Purpose |
|---|---|
| Google (Gmail, Sheets, Drive) | Storing the Operator's records, sending and reading refund emails, reading evidence files |
| Uber Eats | Retrieving order reports; receiving refund requests (Uber Eats support) |
| Anthropic | Classifying unclear Uber Eats support replies (section 4) |
| ngrok | Encrypted delivery of Uber Eats report notifications to the App |
| Telegram (optional) | Sending run summaries and remote commands to the Operator's authorised Telegram accounts, when this feature is enabled |

We may also disclose information when required by law or by a court order, or to protect our rights or the safety of users.

## 9. International transfers

Some of these providers (Google, Anthropic, ngrok, Telegram) may process data outside the European Economic Area, notably in the United States. Where this happens, the transfer relies on the European Commission's adequacy decision for the EU-US Data Privacy Framework where the provider is certified, or on the European Commission's Standard Contractual Clauses.

## 10. Retention

- **Order and refund records** stay in the Operator's Google Sheets for as long as the Operator keeps them there.
- **Downloaded Uber Eats reports** are kept on the App's computer for up to **24 months**, then deleted.
- **Google access tokens** are kept until the account is disconnected, access is revoked, or the service ends.
- **Business and invoicing records** are kept for the period required by French accounting law (10 years).
- When the service with an Operator ends, we delete that Operator's tokens, cached data and downloaded reports from the App's computer within **30 days**.

## 11. Your rights

Under the GDPR you have the right to **access**, **correct** and **delete** your personal data, to **restrict** or **object** to its processing, to **data portability**, and to give instructions about what happens to your data after your death. To exercise any of these rights, email **imadcomptarec@gmail.com**. We answer within one month.

**Revoking Google access:** you can remove the App's access to your Google account at any time at [myaccount.google.com/permissions](https://myaccount.google.com/permissions). The App can then no longer access that account. Revoking access does not delete what is already in your own spreadsheets.

**Complaint:** you can file a complaint with the French data protection authority, the **CNIL** (3 place de Fontenoy, TSA 80715, 75334 Paris Cedex 07, [www.cnil.fr](https://www.cnil.fr)).

## 12. Children

The App is a professional tool for businesses. It is not intended for anyone under 18, and we do not knowingly process children's data.

## 13. Changes to this policy

We may update this policy, for example when we add features or when the law changes. The "Last updated" date at the top shows the latest version. We will inform Operators of significant changes by email before they take effect.

## 14. Contact

**[COMPANY LEGAL NAME]**, [POSTAL ADDRESS], France
Email: **imadcomptarec@gmail.com**

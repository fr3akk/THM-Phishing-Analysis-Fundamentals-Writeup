# Task 4: Email Headers

## Objective

Understand the structure of an email header, identify its key fields, and learn how header information helps analysts investigate suspicious emails.

---

## Key Concepts

- Every email consists of two main components:
  - **Email Header** – Contains metadata about the email, including sender, recipient, routing information, and timestamps.
  - **Email Body** – Contains the actual message content.
- Email headers provide valuable forensic information that is not always visible in the normal inbox view.
- Viewing the raw message source reveals additional fields, such as the originating IP address and authentication details.

---

## Walkthrough

While the email body is what users normally see, the email header contains technical metadata that is crucial during phishing investigations.

The standard header fields include:

| Header Field | Description |
|--------------|-------------|
| **From** | Sender's email address |
| **To** | Recipient's email address |
| **Reply-To** | Address where replies will be sent |
| **Subject** | Subject of the email |
| **Date** | Date and time the email was sent |

To access the complete header information, open the email in Thunderbird and navigate to:

```
View → Message Source
```

or use the shortcut:

```
Ctrl + U
```

The raw message source exposes additional information that is not visible in the normal email view, including routing details, originating IP addresses, and other metadata useful for forensic analysis.

---

## Why Email Headers Matter

Email headers are one of the most valuable sources of evidence during phishing investigations. They can help analysts:

- Verify the actual sender.
- Trace the path an email followed.
- Identify the originating IP address.
- Detect spoofed emails.
- Analyze email authentication results (SPF, DKIM, DMARC).
- Correlate indicators with threat intelligence.

Rather than trusting the display name, analysts rely on header information to determine an email's true origin.

---

## Important Notes

> The inbox view only displays a limited set of header fields.

> The raw message source contains significantly more information useful for investigations.

> The originating IP address can often help identify where an email actually originated.

---

## My Notes

- One of the first things I should inspect during a phishing investigation is the raw email header.
- The **Received** fields help reconstruct the email's path.
- The **X-Originating-IP** field can reveal the sender's original IP address when available.
- The **Reply-To** field should always be compared against the **From** address, as attackers frequently abuse it.

---

## Takeaways

- Learned the difference between the email header and email body.
- Understood the purpose of common email header fields.
- Learned how to view the raw email source in Thunderbird.
- Recognized why email headers are essential during phishing investigations.

---

## Questions

### 1. What is the full subject line of `email1.eml`?
  > Help protect your budget by protecting your home

### 2. What IP address is listed as the `X-Originating-IP`?
  > 

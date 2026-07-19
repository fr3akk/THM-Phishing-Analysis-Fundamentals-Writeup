# Task 6: Types of Phishing

## Objective

Learn about the different types of phishing attacks, recognize common phishing techniques, and analyze phishing emails by inspecting their headers, sender information, and message content.

---

## Types of Phishing

### Spam
- Unsolicited bulk emails sent to a large number of recipients.
- Malicious spam is often referred to as **malspam** because it delivers phishing links or malware.

### Phishing
- A generic phishing attack that impersonates a trusted organization.
- The goal is to trick users into revealing sensitive information such as usernames, passwords, or financial details.

### Spear Phishing
- A highly targeted phishing attack aimed at a specific individual or organization.
- Often uses personalized information to appear legitimate and increase the likelihood of success.

### Whaling
- A specialized form of spear phishing that targets senior executives such as CEOs or CFOs.
- The objective is usually to steal sensitive business information or authorize fraudulent financial transactions.

### Smishing
- Phishing conducted through SMS or text messages.
- Commonly includes malicious links or fake delivery notifications.

### Vishing
- Voice-based phishing carried out over phone calls.
- Attackers impersonate trusted organizations to obtain confidential information.

---

## Anatomy of a Phishing Email

Phishing emails often share several common characteristics regardless of their objective.

### Spoofed Sender Address
The sender's email address is crafted to resemble a trusted organization while using a malicious domain.

### Urgent Language
Creates a sense of urgency to pressure the recipient into acting quickly without verifying the email.

### Brand Impersonation
Uses company logos, colors, and formatting to imitate legitimate organizations.

### Grammar and Spelling Errors
May contain spelling mistakes, awkward wording, or unusual phrasing, although modern phishing emails generated with AI are becoming more convincing.

### Generic Greetings
Uses greetings such as "Dear Customer" instead of addressing the recipient by name.

### Hidden or Shortened Links
Hyperlinks may display a legitimate-looking name while redirecting users to malicious websites.

### Malicious Attachments
Attachments are disguised as legitimate files but may actually contain malware or malicious scripts.

---

## Safe Analysis

When analyzing phishing emails:

- Never click suspicious links directly.
- Never open unknown attachments on your host system.
- Use isolated environments such as virtual machines or sandboxes.
- Defang URLs, domains, and email addresses before sharing them.

### Example

Original URL:

```text
http://www.suspiciousdomain.com
```

Defanged URL:

```text
hxxp://www[.]suspiciousdomain[.]com
```

---

# Questions

## Question 1

**Which reputable organization is being spoofed in this phishing attempt?**

**Answer:**

```
Home Depot
```

---

## Question 2

**What is the sender's email address?**

**Answer:**

```
Support@teckbe.com
```

---

## Question 3

**What is the defanged X-Originating-IP?**

Inspect the email headers and locate:

```text
103[.]234[.]236[.]83
```

---

## Question 4

**Which mail server generated the Authentication-Results header?**

Inspect the email source and locate:

```text
atlas102.free.mail.gq1.yahoo.com
```

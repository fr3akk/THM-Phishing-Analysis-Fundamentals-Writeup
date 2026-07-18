# Task 2: The Email Address

## Objective

Understand the structure of an email address and why it is one of the first indicators examined during a phishing investigation.

---

## Key Concepts

- Every email address consists of three main components:
  - **Username (Local Part)** – Identifies the recipient's mailbox.
  - **@ Symbol** – Separates the local part from the domain.
  - **Domain Name** – Specifies the mail server responsible for receiving the email.
- Ray Tomlinson introduced the **@** symbol for email addressing in the early days of ARPANET.
- Understanding the anatomy of an email address is essential for identifying spoofed or suspicious senders.

---

## Walkthrough

This task introduces the basic structure of an email address, which forms the foundation of phishing analysis. Before examining email headers or message content, analysts should first inspect the sender's email address for anything unusual.

An email address follows the format:

```
username@domain.com
```

Example:

```
david@tryhackme.com
```

Where:

| Component | Description |
|-----------|-------------|
| **Username** | Identifies the recipient's mailbox on the mail server. |
| **@** | Separator between the username and the domain. |
| **Domain** | Specifies the mail server responsible for handling the email. |

A helpful analogy is to think of an email address like a postal address:

- **Domain** → Street or apartment building
- **Username** → Specific house or apartment number

Together, these components tell the mail server exactly where the email should be delivered.

---

## Why It Matters in Phishing Analysis

Attackers frequently manipulate email addresses to impersonate trusted organizations or individuals. Common tactics include:

- Registering lookalike domains (e.g., `micr0soft.com`)
- Using typosquatting domains (e.g., `paypaI.com`, where the capital **I** replaces the lowercase **l**)
- Creating misleading usernames while using legitimate email services (e.g., `support.amazon@gmail.com`)
- Relying on the display name to appear trustworthy, while the actual email address reveals a different sender.

For this reason, analysts should always inspect the **full email address**, not just the display name.

---

## Important Notes

> The display name can be easily spoofed, but the underlying email address often provides valuable clues during an investigation.

> The domain name is especially important, as it can reveal impersonation attempts, newly registered domains, or typosquatting attacks.

---

## My Notes

- Always verify the sender's **actual email address**, not just the display name.
- Look for misspelled or lookalike domains.
- Check if the sender's domain matches the organization they claim to represent.
- The email address is one of the first artifacts examined during phishing investigations.

---

## Takeaways

- Learned the anatomy of an email address.
- Understood the purpose of the username, `@` symbol, and domain name.
- Recognized why email addresses are important indicators during phishing investigations.
- Identified common attacker techniques involving spoofed and lookalike email addresses.

---

## Questions

1. Identify the domain used in the following email address: `hatsalesman@tryhatme.com`
  > tryhatme.com

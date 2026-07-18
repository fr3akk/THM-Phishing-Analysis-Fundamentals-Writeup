# Task 3: Email Delivery

## Objective

Understand how emails are transmitted from the sender to the recipient and learn the roles of the protocols involved in email delivery.

---

## Key Concepts

- **SMTP (Simple Mail Transfer Protocol)** is responsible for sending emails.
- **POP3 (Post Office Protocol v3)** downloads emails to a single device and typically removes them from the mail server.
- **IMAP (Internet Message Access Protocol)** stores emails on the mail server and synchronizes them across multiple devices.
- **DNS (Domain Name System)** helps locate the recipient's mail server by resolving the domain's MX (Mail Exchange) records.

---

## Walkthrough

Email delivery relies on multiple protocols working together to ensure messages are sent and received correctly.

### SMTP

SMTP is used whenever an email is sent from an email client to a mail server and between mail servers during delivery.

**Key Characteristics**

- Sends outgoing emails
- Transfers emails between mail servers
- Does not retrieve emails

---

### POP3

POP3 downloads emails from the mail server to a single device.

**Characteristics**

- Emails are stored locally
- Messages are typically removed from the server after download
- Best suited for accessing email from one device

---

### IMAP

IMAP keeps emails stored on the mail server while synchronizing them across multiple devices.

**Characteristics**

- Emails remain on the server
- Supports multiple devices
- Changes made on one device are reflected on others

---

## Email Delivery Process

A simplified email delivery workflow:

1. The sender composes an email.
2. The email client sends the message using **SMTP**.
3. The sending mail server queries **DNS** for the recipient domain's **MX (Mail Exchange)** record.
4. DNS returns the destination mail server.
5. The email is delivered to the recipient's mail server.
6. The recipient retrieves the email using **POP3** or **IMAP**.

---

## Important Notes

> SMTP is used only for **sending** emails.

> POP3 is designed for downloading emails to a single device.

> IMAP is recommended when accessing emails from multiple devices.

> DNS plays a critical role by locating the recipient's mail server through MX records.

---

## My Notes

- SMTP = Send Mail
- POP3 = Download Mail
- IMAP = Sync Mail
- DNS resolves the recipient domain before delivery.
- Most modern email services (such as Gmail and Outlook) use IMAP by default.

---

## Takeaways

- Learned the purpose of SMTP, POP3, and IMAP.
- Understood how DNS helps route emails to the correct mail server.
- Learned the complete journey of an email from sender to recipient.
- Recognized why IMAP is preferred over POP3 in modern environments.

---

## Questions

### 1. Which protocol is responsible for sending an email from a client to a mail server?
  > SMTP

### 2. Which service is used to look up the recipient domain's mail server?
  > DNS

### 3. Bob wants to access his email from multiple devices, including his phone and laptop. Which protocol should he use?
  >IMAP

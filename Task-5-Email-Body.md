# Task 5: Email Body

## Objective

Understand how to analyze an email body, inspect its HTML source, and reconstruct email attachments by decoding Base64-encoded data.

---

## Key Concepts

### 1. Email Body Formats

Emails can be sent in two different formats:

#### Plain Text Email
- Contains only plain text.
- Does not support formatting, images, hyperlinks, or styling.
- Easier to analyze because there is no embedded HTML.

#### HTML Email
- Uses HTML to create visually formatted emails.
- Can include:
  - Images
  - Hyperlinks
  - Buttons
  - Logos
  - CSS styling
  - Hidden elements

HTML emails are commonly used in phishing attacks because they can disguise malicious links behind legitimate-looking text or buttons.

---

### 2. Viewing the HTML Source

Most email clients display the rendered version of an email rather than its underlying HTML.

Inspecting the HTML source allows investigators to identify:
- Hidden hyperlinks
- Embedded images
- HTML structure
- Tracking elements
- Suspicious URLs
- Other indicators of phishing or malicious activity

This helps analysts understand how the email is constructed and detect content that may not be immediately visible in the rendered view.

---

### 3. Reconstructing Attachments

Email attachments are typically encoded using **Base64** before being transmitted.

The email source contains several important MIME headers:

- **Content-Type:** Specifies the file type (e.g., `application/pdf`).
- **Content-Disposition:** Indicates that the file is an attachment and provides its filename.
- **Content-Transfer-Encoding:** Specifies how the attachment is encoded, most commonly `base64`.

The Base64 data can be decoded using tools such as **CyberChef** or a **Base64-to-PDF converter** to reconstruct the original attachment for forensic analysis.

---

# Questions & Answers

## Question 1

**What is the Content-Type of the attachment?**

**Answer:**

```text
application/pdf
```

---

## Question 2

**What is the name of the attachment?**

**Answer:**

```text
zmqpalgh.pdf
```

> **Note:** Verify the exact filename in `email2.txt` before submitting, as capitalization and spacing may matter.

---

## Question 3

**What is the hidden flag value?**

The hidden flag cannot be determined from the screenshots alone.

### Steps to Obtain the Flag

1. Open `email2.txt`.
2. Locate the Base64-encoded attachment data.
3. Copy the entire Base64 string.
4. Decode it using **CyberChef** or a **Base64-to-PDF converter**.
5. Open the recovered PDF.
6. Read the hidden flag inside the document.

> THM{BENIGN_PDF_ATTACHMENT}

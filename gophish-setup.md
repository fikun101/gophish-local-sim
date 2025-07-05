# GoPhish Setup Guide (Kali Linux)

This guide walks through the installation and configuration of **GoPhish** on a Kali Linux machine for use in a phishing simulation lab.

---

## 1. Download GoPhish
```bash
wget https://github.com/gophish/gophish/releases/download/v0.12.1/gophish-v0.12.1-linux-64bit.zip
unzip gophish-v0.12.1-linux-64bit.zip
cd gophish-v0.12.1-linux-64bit
```

---

## 2. Run GoPhish
```bash
sudo ./gophish
```

- GoPhish runs a web interface on port `3333` (admin panel)
- Sends phishing pages/emails from port `80` (landing pages)

Access the admin UI in browser:
```
https://localhost:3333
```
Default credentials:
- Username: `admin`
- Password: auto-generated (check terminal output)

---

## 3. Optional: Set Custom Admin Password
After logging in:
- Go to `Users` > Edit your user
- Change password and save

---

## 4. Configure Sending Profile (SMTP)
To simulate email sending:
- Use test SMTP server (like MailHog, or setup Postfix locally)
- Or use a disposable SMTP relay (if using for lab/testing only)

Go to:
```
Sending Profiles > + New Profile
```
Enter:
- Name: `Test SMTP`
- Interface Type: `SMTP`
- Host: `127.0.0.1:25` (or whatever your relay uses)
- Email: `phisher@lab.com`

---

## 5. Create a Landing Page
- Go to `Landing Pages` > + New Page
- Paste in your fake login HTML
- Check "Capture submitted data"
- (Optional) Enable redirection after login

---

## 6. Create an Email Template
- Go to `Email Templates` > + New Template
- Add subject, body text (with link to landing page)
- Use `{{.URL}}` as a dynamic link placeholder

---

## 7. Launch a Campaign
- Go to `Campaigns` > + New Campaign
- Add:
  - Name: `Phish Test`
  - Email Template: your template
  - Landing Page: your fake login
  - SMTP Profile: your SMTP settings
  - Group: list of recipients (e.g., test@vm.com)

Start the campaign and monitor results in real-time.

---

## Log Files
- GoPhish logs activity to `gophish.log`
- Use this for post-campaign analysis or validation

---

## Final Notes
- Run this lab in an isolated or virtual environment only
- Do not use real email accounts or send messages outside your test lab
- For testing email delivery, use tools like MailHog, fakeSMTP, or a test VM with Thunderbird/Outlook

---

### Next Step: Create the email template and landing page markdown files

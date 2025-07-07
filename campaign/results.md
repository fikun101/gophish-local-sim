# Campaign Results – GoPhish Simulation

This document summarizes the observed outcomes from the phishing campaign launched using GoPhish within a controlled environment.

---

## Campaign Details
- **Campaign Name:** TechNova Credential Harvest
- **Email Template:** Fake Security Alert – Password Reset Required
- **Landing Page:** TechNova Login (custom HTML)
- **Target Group:** 1 Gmail account used for testing
- **SMTP Used:** Gmail SMTP (`smtp.gmail.com`)

---

## Outcome Summary
- Email was successfully sent via Gmail SMTP
- Email was received in a separate Gmail inbox
- The recipient was able to click the phishing link
- The landing page (TechNova Login) loaded successfully
- Credentials submitted through the form were captured in the GoPhish dashboard
---

## Observations
- Initial testing with local SMTP relay failed to allow clickable URLs due to security restrictions.
- Gmail’s SMTP server was used to successfully deliver the phishing email.
- A second Gmail address (under the user’s control) was used to receive and interact with the phishing email.
- Clicking the link directed the user to the fake TechNova login page.
- Submitted credentials were successfully captured and logged in the GoPhish dashboard.

---

## Screenshots (See `/screenshots/` folder)
- `dashboard.png` – Overview of campaign statistics in GoPhish
- `email-gmail.png` – Phishing email as shown in Gmail inbox
- `submitted-creds.png` – Captured credential entry in GoPhish dashboard

---

## Log Review
- GoPhish `gophish.log` confirmed campaign launch and interaction events
- Gmail SMTP authentication and delivery succeeded with proper app password or “less secure apps” configuration

---

## Ethical Note
All testing was done using accounts owned and controlled by the tester. No third-party users were involved. This simulation was created purely for cybersecurity training and ethical demonstration purposes.

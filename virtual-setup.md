# Virtual Environment Setup

This document outlines the virtual lab environment used to conduct the phishing simulation and monitor email delivery and interactions.

---

## Host System
- **Host OS:** Kali Linux (running GoPhish)
- **Hypervisor:** VMware Workstation / VirtualBox

---

## Target Email Client (Victim VM)
- **VM OS:** Kali Linux (or Ubuntu Desktop)
- **Mail Client:** Thunderbird (configured with test Gmail account)
- **Network Mode:** NAT or Bridged (ensures external internet access)

---

## SMTP Configuration
- **Initial Method (Local Mail Server):**
  - Postfix configured locally
  - Result: Email delivered but Gmail blocked clickable links for security

- **Final Method (Gmail SMTP):**
  - GoPhish configured to use `smtp.gmail.com`
  - Email sent from a test Gmail account
  - Receiver: separate Gmail inbox controlled by tester

---

## Email Monitoring Setup
- **Thunderbird** configured with IMAP to receive test emails
- **Gmail Web UI** also used to verify email rendering and click-through capability

---

## Isolation & Control
- No real user accounts or external systems involved
- Both sender and recipient Gmail accounts were controlled by the tester
- Campaign interactions were limited to this test environment

---

## Notes
- Disabling browser security warnings may be necessary to test landing page rendering in some environments
- GoPhish server was hosted entirely inside Kali VM running locally

---



This setup enabled safe simulation of a phishing campaign with full control and no external risk.

# Phishing Simulation with GoPhish

## 🎯 Project Overview
This project demonstrates a controlled phishing simulation using [GoPhish](https://getgophish.com/), an open-source phishing framework. A fake login landing page was created and delivered to a test mailbox within a virtual environment to evaluate how phishing attacks can be conducted and monitored ethically.

## 🧰 Tools & Technologies
- **GoPhish**: Phishing campaign management and tracking
- **VirtualBox / VMware**: Lab environment
- **Postfix/Dovecot** *(optional)*: Mail relay & IMAP
- **Kali Linux**: Host and attack simulator
- **Wireshark**: Email traffic sniffing (optional)

## 🛠️ Project Components
- Custom **email template** and fake **landing page**
- **GoPhish server** hosted on Kali Linux
- A separate VM set up to receive phishing emails
- Capture of credentials and analysis of click-throughs

## 📸 Screenshots
See `/screenshots/` folder for:
- GoPhish campaign dashboard
- Fake login page
- Phishing email received in VM

## 📂 Folder Structure
```
gophish-phishing-lab/
├── README.md
├── gophish-setup.md
├── campaign/
│   ├── email-template.md
│   ├── landing-page.md
│   └── results.md
├── environment/
│   ├── virtual-setup.md
│   └── network-diagram.png
├── screenshots/
│   └── *.png
└── report/
    └── GoPhish_Project_Redacted.pdf
```

## 📄 Full Report
[📄 View the Redacted Project Report](report/GoPhish_Project_Redacted.pdf)

## ⚠️ Disclaimer
This project was conducted in a secure and legal virtual lab. No real users were targeted. Intended for educational and ethical testing only.

# Email Template – Phishing Simulation

This file describes the structure and content of the phishing email used in the GoPhish campaign.

---

## Template Name
Fake Security Alert – Password Reset Required

---

## Subject Line
**[Action Required] Unusual Login Attempt Detected – Reset Your Password**

---

## Email Body (HTML)
```html
<p>Dear User,</p>
<p>We've detected an unusual login attempt from a new device on your account. For your security, please reset your password immediately.</p>
<p><a href="{{.URL}}" style="background-color:#1a73e8;color:#fff;padding:10px 20px;text-decoration:none;">Reset Password</a></p>
<p>If you did not request this, please ignore this email.</p>
<p>Thanks,<br>IT Security Team</p>
```

---

## Dynamic URL
- The `{{.URL}}` tag is replaced by GoPhish with the real tracking URL tied to the landing page

---

## Notes
- The tone mimics a typical security warning email to trigger urgency
- Designed to encourage the user to click the link and visit the fake login page
- The message uses inline CSS to create a convincing "Reset Password" button

---

## Ethical Use
This email was sent only within a lab-controlled virtual environment for educational purposes. No real users or live systems were involved.

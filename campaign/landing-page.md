# Landing Page – TechNova Fake Login (Phishing Simulation)

This file documents the actual landing page used in the phishing campaign, designed to resemble a secure login page for a fictional brand, TechNova.

---

## Page Title
TechNova Login Portal

---

## Design Overview
The landing page used a modern, glassmorphism-inspired UI with:
- Gradient background
- Blurred card-style container
- Styled username/password inputs
- A responsive, clean design using the Inter font

---

## HTML Template Used
```html
<!DOCTYPE html><html lang="en"><head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1"/>
  <title>TechNova Login</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap');

    body {
      margin: 0;
      font-family: 'Inter', sans-serif;
      background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      color: #fff;
    }

    .login-container {
      background: rgba(255, 255, 255, 0.05);
      backdrop-filter: blur(12px);
      border-radius: 12px;
      padding: 40px 50px;
      box-shadow: 0 8px 32px rgba(0,0,0,0.4);
      width: 350px;
      text-align: center;
    }

    .login-container h1 {
      margin-bottom: 20px;
      font-weight: 600;
      font-size: 28px;
      letter-spacing: 1.2px;
      color: #00f0ff;
    }

    .input-group {
      margin-bottom: 25px;
      text-align: left;
    }

    label {
      display: block;
      font-size: 14px;
      margin-bottom: 6px;
      color: #a0cce8;
    }

    input[type="text"],
    input[type="password"] {
      width: 100%;
      padding: 12px 15px;
      border-radius: 8px;
      border: none;
      font-size: 16px;
      outline: none;
      background-color: rgba(255,255,255,0.15);
      color: #e1eaff;
      transition: background-color 0.3s ease;
    }

    input[type="text"]:focus,
    input[type="password"]:focus {
      background-color: rgba(255,255,255,0.3);
      box-shadow: 0 0 6px #00f0ff;
    }

    button {
      width: 100%;
      padding: 14px;
      border: none;
      border-radius: 8px;
      background: #00f0ff;
      color: #002f34;
      font-size: 18px;
      font-weight: 600;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }

    button:hover {
      background: #00c9d9;
    }

    .footer-text {
      margin-top: 20px;
      font-size: 13px;
      color: #7ab8c6;
    }
  </style>
</head>
<body>
  <div class="login-container">
    <h1>TechNova</h1>
    <form action="">
      <div class="input-group">
        <label for="username">Username</label>
        <input id="username" type="text" placeholder="Enter your username"/>
      </div>
      <div class="input-group">
        <label for="password">Password</label>
        <input id="password" type="password" placeholder="Enter your password" name="password"/>
      </div>
      <button type="submit">Log In</button>
    </form>
    <p class="footer-text">© 2025 TechNova Inc.</p>
  </div>
</body></html>
```

---

## GoPhish Configuration
- Data Capture: Enabled
- Redirect after submit: Disabled (user remains on page)

---

## Notes
- HTML and CSS were authored from scratch to simulate a believable corporate portal
- The site does not connect to any backend or real authentication
- GoPhish records the submitted data in the admin dashboard under campaign results

---

## Ethical Disclaimer
This page was used exclusively in a secure lab environment for ethical, educational testing. No real users, credentials, or organizations were involved.

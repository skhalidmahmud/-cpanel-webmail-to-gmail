# Connect cPanel Webmail to Gmail 📧 (Updated Step-by-Step Guide)

A complete guide to linking your custom cPanel domain email (e.g., info@yourdomain.com) with a standard Gmail account using POP3 and SMTP. This allows you to send and receive custom domain emails directly from your Gmail inbox.

## 🚀 Why do this?
- Manage all your emails in one familiar Gmail interface.
- No need to log into cPanel Webmail every time.
- Utilize Gmail's powerful search, spam filtering, and mobile app features.

## 📋 Prerequisites
- Access to your hosting cPanel.
- A standard Gmail account.
- A created custom email address in cPanel (e.g., info@thinkori.com).

---

## 🛠️ Step 1: Gather cPanel Email Details
First, you need the server configuration details from your cPanel.
1. Log in to your cPanel and go to Email Accounts.
2. Note down the following Secure SSL/TLS Settings:
   - Username: Your full email address (e.g., info@thinkori.com)
   - Password: The password for this email account
   - Incoming Server (POP3): mail.yourdomain.com (Port: 995)
   - Outgoing Server (SMTP): mail.yourdomain.com (Port: 465 or 587)

---

## 📥 Step 2: Set up Gmail to Receive Emails (POP3)
1. Log in to your Gmail account.
2. Click the Gear icon ⚙️ (Settings) in the top right and select "See all settings".
3. Go to the "Accounts and Import" tab.
4. Scroll to "Check mail from other accounts" and click "Add a mail account". (Note: If this option isn't directly visible, you can also use "Import mail and contacts").
5. Enter your full custom email address (e.g., info@thinkori.com) and click Next.
6. Select "Import emails from my other account (POP3)" and click Next.
7. Fill in the details:
   - Username: Your FULL custom email address (Do not just put 'info').
   - Password: Your email password.
   - POP Server: mail.yourdomain.com
   - Port: 995
   - Check: "Always use a secure connection (SSL)..."
   - Check: "Leave a copy of retrieved message on the server" (Crucial for backups).
   - Check: "Add label to all imported mail"
8. Click "Add Account" (or "Start import").

---

## 📤 Step 3: Set up Gmail to Send Emails (SMTP)
1. In the "Accounts and Import" tab, find "Send mail as:" and click "Add another email address".
2. Enter your Name (what recipients will see) and click Next Step.
3. Fill in the SMTP details.
   
   > 💡 PRO TIP (Troubleshooting): 
   > Try Option A first. If you get an error ("Error: you must provide SMTP information..."), use Option B.
   
   Option A (Default):
   - SMTP Server: mail.yourdomain.com
   - Port: 465
   - Username: Your FULL custom email address.
   - Password: Your email password.
   - Select: Secured connection using SSL.
   
   Option B (Troubleshooting/Fallback):
   - SMTP Server: mail.yourdomain.com (or your hosting's main server name if this fails)
   - Port: 587
   - Username: Your FULL custom email address.
   - Password: Your email password.
   - Select: Secured connection using TLS.
   
4. Click "Add Account".

---

## ✅ Step 4: Verify the Setup
1. If successful, you will see a success message saying "Congratulations, we successfully located your other server...". Close this popup window.
2. Go back to your main Gmail inbox and wait 1-2 minutes.
3. You will receive a verification email from the "Gmail Team".
4. Open the email and click on the long confirmation link.
5. A new tab will open; click "Confirm".

🎉 Congratulations! 
You can now select your custom email address from the "From" dropdown menu whenever you compose a new email in Gmail.

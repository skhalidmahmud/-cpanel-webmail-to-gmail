# Connect cPanel Webmail to Gmail 📧 (Comprehensive Guide)

A complete, step-by-step guide to linking your custom cPanel domain email (e.g., info@yourdomain.com) with a standard Gmail account using POP3 and SMTP. This guide also covers how to set up a Profile Picture (DP) for your custom domain email.

## 🚀 Why do this?
- Manage all your emails in one familiar Gmail interface.
- No need to log into cPanel Webmail every time.
- Utilize Gmail's powerful search, spam filtering, and mobile app features.
- Establish a professional identity with a custom profile picture.

## 📋 Prerequisites
- Access to your hosting cPanel.
- A standard Gmail account.
- A created custom email address in cPanel (e.g., info@thinkori.com).

---

## 🛠️ Step 1: Gather cPanel Email Details
First, obtain the server configuration details from your cPanel.
1. Log in to your cPanel and navigate to **Email Accounts**.
2. Locate your email address and click **Connect Devices** or **Set Up Mail Client**.
3. Note down the following from the **Secure SSL/TLS Settings**:
   - **Username:** Your full email address (e.g., info@thinkori.com)
   - **Password:** The password for this email account
   - **Incoming Server (POP3):** mail.yourdomain.com (Port: 995)
   - **Outgoing Server (SMTP):** mail.yourdomain.com (Port: 465 or 587)

---

## 📥 Step 2: Set up Gmail to Receive Emails (POP3)
1. Log in to your primary Gmail account.
2. Click the **Gear icon ⚙️** (Settings) in the top right and select **See all settings**.
3. Go to the **Accounts and Import** tab.
4. Scroll to the **Check mail from other accounts** section and click **Add a mail account**. (Note: If this option isn't directly visible, look for **Import mail and contacts**).
5. Enter your full custom email address (e.g., info@thinkori.com) and click **Next**.
6. Select **Import emails from my other account (POP3)** and click **Next**.
7. Fill in the details:
   - **Username:** Your FULL custom email address (e.g., info@thinkori.com).
   - **Password:** Your custom email password.
   - **POP Server:** mail.yourdomain.com
   - **Port:** 995
   - ✅ **Check:** *Always use a secure connection (SSL)...*
   - ✅ **Check:** *Leave a copy of retrieved message on the server* (Crucial for retaining backups on your hosting).
   - ✅ **Check:** *Add label to all imported mail* (Helps organize incoming emails).
8. Click **Add Account** (or **Start import**).

---

## 📤 Step 3: Set up Gmail to Send Emails (SMTP)
1. In the **Accounts and Import** tab, locate **Send mail as:** and click **Add another email address**.
2. Enter your **Name** (the sender name recipients will see) and keep **Treat as an alias** checked. Click **Next Step**.
3. Fill in the SMTP details.
   
   > 💡 **PRO TIP (Troubleshooting):** 
   > Try Option A first. If you encounter an error ("Error: you must provide SMTP information..."), proceed with Option B.
   
   **Option A (Default):**
   - **SMTP Server:** mail.yourdomain.com
   - **Port:** 465
   - **Username:** Your FULL custom email address.
   - **Password:** Your custom email password.
   - Select: **Secured connection using SSL.**
   
   **Option B (Fallback):**
   - **SMTP Server:** mail.yourdomain.com (or your hosting's main server hostname)
   - **Port:** 587
   - **Username:** Your FULL custom email address.
   - **Password:** Your custom email password.
   - Select: **Secured connection using TLS.**
   
4. Click **Add Account**.

---

## ✅ Step 4: Verify the Setup
1. Upon successful connection, a success message will appear. Close the popup window.
2. Return to your main Gmail inbox and wait 1-2 minutes.
3. You will receive a verification email from the "Gmail Team".
4. Open the email and click on the provided confirmation link.
5. A new tab will open; click **Confirm**.

*Note regarding Sent Emails: Emails sent via Gmail using this SMTP setup will be saved in your Gmail's "Sent" folder, not in the cPanel Webmail's "Sent" folder. This is standard SMTP behavior.*

---

## 🖼️ Step 5: Add a Profile Picture (DP) to Your Custom Domain Email
By default, cPanel webmail does not support profile pictures. However, you can display a DP to recipients (especially Gmail users) by linking your custom email to a Google Account.

1. Go to the [Google Account Creation Page](https://accounts.google.com/signup).
2. Enter your First and Last name.
3. When prompted for an email address, click on **Use my current email address instead**.
4. Enter your custom domain email (e.g., info@thinkori.com) and click **Next**.
5. Verify the email address by entering the code sent to your inbox (which will now arrive in your linked Gmail account).
6. Complete the setup process (password, date of birth, etc.).
7. Once the account is created, go to [myaccount.google.com](https://myaccount.google.com/) while logged into this new account.
8. Click on the profile icon (the initial of your name) at the top right, or click on **Personal info** on the left menu.
9. Click on the **Profile Picture** option and upload your desired logo or image.

Your custom email now has a professional profile picture that will be visible to recipients using Gmail and other supported platforms.

---
## 📄 License
This guide is released under the [MIT License](LICENSE).

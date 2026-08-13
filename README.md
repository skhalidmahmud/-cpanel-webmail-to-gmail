# Connect cPanel Webmail to Gmail 📧

A complete, step-by-step guide to linking your custom cPanel domain email (e.g., `info@yourdomain.com`) with a standard Gmail account using POP3 and SMTP. This allows you to send and receive custom domain emails directly from your Gmail inbox.

## 🚀 Why do this?
- Manage all your emails in one familiar Gmail interface.
- No need to log into cPanel Webmail (Roundcube/Horde) every time.
- Utilize Gmail's powerful search, spam filtering, and mobile app features.

## 📋 Prerequisites
- Access to your hosting **cPanel**.
- A standard **Gmail account**.
- A created custom email address in cPanel (e.g., `info@thinkori.com`).

---

## 🛠️ Step 1: Gather cPanel Email Details
First, you need the server configuration details from your cPanel.

1. Log in to your **cPanel** and go to **Email Accounts**.
2. Find your email address and click on **Connect Devices** or **Set Up Mail Client**.
3. Scroll down to **Secure SSL/TLS Settings** (Recommended) and note down the following:
   - **Username:** Your full email address (e.g., `info@thinkori.com`)
   - **Password:** The password for this email account
   - **Incoming Server (POP3):** `mail.yourdomain.com` (Port: **995**)
   - **Outgoing Server (SMTP):** `mail.yourdomain.com` (Port: **465**)

---

## 📥 Step 2: Set up Gmail to Receive Emails (POP3)
This step allows Gmail to fetch emails sent to your custom address.

1. Log in to your **Gmail account**.
2. Click the **Gear icon ⚙️** (Settings) in the top right corner and select **See all settings**.
3. Go to the **Accounts and Import** tab.
4. Scroll down to the **Check mail from other accounts** section and click **Add a mail account**.
5. A popup window will appear. Enter your custom email address and click **Next**.
6. Select **Import emails from my other account (POP3)** and click **Next**.
7. Fill in the details gathered from Step 1:
   - **Username:** Your full custom email address.
   - **Password:** Your custom email password.
   - **POP Server:** `mail.yourdomain.com`
   - **Port:** `995`
   - ✅ **Check:** *Always use a secure connection (SSL) when retrieving mail.*
   - ✅ **Check:** *Label incoming messages* (This helps easily identify business emails in your inbox).
8. Click **Add Account**.

---

## 📤 Step 3: Set up Gmail to Send Emails (SMTP)
After successfully adding the POP3 account, Gmail will ask if you also want to send emails from this address.

1. Select **Yes, I want to be able to send mail as...** and click **Next**.
   *(If the popup closed, you can find this in Settings > Accounts and Import > Send mail as > Add another email address).*
2. Enter your **Name** (this is what recipients will see) and keep **Treat as an alias** checked. Click **Next Step**.
3. Fill in the SMTP details:
   - **SMTP Server:** `mail.yourdomain.com`
   - **Port:** `465`
   - **Username:** Your full custom email address.
   - **Password:** Your custom email password.
   - ✅ Select **Secured connection using SSL**.
4. Click **Add Account**.

---

## ✅ Step 4: Verify the Setup
1. Gmail will now send a verification code to your custom email address.
2. Since you've just set up POP3 (Step 2), this verification email will arrive directly in your **Gmail inbox** within a minute or two.
3. Open the email, copy the verification code, paste it into the popup window, and click **Verify**.

🎉 **Congratulations!** 
You can now select your custom email address from the **"From"** dropdown menu whenever you compose a new email in Gmail.

---
## 📄 License
This guide is released under the [MIT License](LICENSE).
# 💡 WiFiBillBot – Smart Monthly Billing Automation using Python

WiFiBillBot is an automated billing system built in Python to simplify and streamline internet bill generation and delivery. Inspired by real-world use cases like JioFiber, ACT, and BSNL broadband billing systems, it reads customer details from Excel, generates professional PDF invoices, and sends them via email — based on whether the customer has paid or not.

---

## 🔧 Features

- 📊 Excel-based customer management
- 📄 Automatically generates monthly PDF invoices
- ✉️ Sends personalized emails for:
  - ✅ Paid users → "Thank you" + invoice
  - ❌ Unpaid users → "Polite reminder" + invoice
- 📬 Built-in email support via Gmail (SMTP)
- 🧠 Easy to expand with WhatsApp or UPI QR alerts

---

## 📂 Project Structure

```

wifi-billbot/
├── billbot.py           ← Python script to automate billing
├── clients.xlsx         ← Excel file with customer data
├── README.md            ← This file
├── Invoice\_Apsar\_Jun-2025.pdf   ← Auto-generated PDF per customer

````

---

## 📥 Setup Instructions

1. **Install required packages:**

```bash
pip install pandas fpdf yagmail openpyxl
````

2. **Enable Gmail App Passwords:**

   * Enable 2-Step Verification in Gmail
   * Create an [App Password](https://myaccount.google.com/apppasswords)
   * Use this in the script instead of your regular password

3. **Edit `billbot.py`:**

   * Replace `your_email@gmail.com` and `your_app_password` with your credentials

4. **Customize `clients.xlsx`:**

   * Columns: Name, Email, Plan, Price, Paid?

---

## ▶️ How to Run

```bash
python billbot.py
```

Each time it runs:

* ✅ Checks each row in the Excel
* 📤 Sends appropriate email
* 🧾 Saves invoice as PDF for records

---

## 🔄 Example Email Logic

| Condition  | Email Sent                         |
| ---------- | ---------------------------------- |
| Paid = Yes | "Thank you" + attached PDF invoice |
| Paid = No  | "Friendly reminder" + PDF invoice  |

---

## 💼 Real-World Applications

* Internet Service Providers (ISPs)
* Apartment associations with shared WiFi
* Freelancers charging monthly clients
* Local cable & broadband providers

---

## 🚀 Future Enhancements (Optional)

* 📲 WhatsApp integration using Twilio / WATI
* 🧾 Add UPI QR Code to PDF for instant payment
* 📆 Automate monthly runs via CRON or Task Scheduler
* 🌐 Web dashboard for report viewing and editing

---

## 👤 Author

**Apsar**
🚀 Passionate about automation, billing systems, and Python development.

---



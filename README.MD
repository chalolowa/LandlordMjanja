# Landlord254

A simple, mobile-first platform that helps landlords:

- Manage tenants

- Automate rent reminders (SMS/USSD)

- Track rent payments

- Handle payment verification

- Communicate with tenants

Using:

- Africa's Talking (SMS + USSD APIs)

- n8n (workflow automation engine)

<br>

---

<br>

Problems solved:

- Low tech adoption in real estate

- Manual rent collection

- Poor and mostly time-consuming payment verification

- Weak tenant communication

<br>

---

<br>

🧱 Core Features

    1️⃣ Landlord Dashboard (Web)

      - Add property

      - Add tenant

      - Set rent amount + due date

      - View payment status

      - View income summary
  

    2️⃣ Automated Rent Reminder System (n8n Flow Workflow):

    Trigger:

      - 3 days before due date

      - On due date

      - After due date

    Action:

      - Send SMS via Africa's Talking

    Example message:

        “Reminder: Rent of KES 25,000 due on 5th Feb. Please pay to Paybill XXXX.”



    3️⃣ USSD for Tenants (No App Required)

        Example:

            Dial:
            *XXX#

        Menu:

            - View Rent Balance

            - Confirm Payment

            - Contact Landlord



    4️⃣ Simple Accounting Module

        Auto-track:

          - Rent expected

          - Rent paid

          - Rent overdue

        Monthly income summary:

          - Monthly PDF summary

<br>

---

<br>

🧠 Architecture

    Frontend:

      - Next.js

      - Tailwind / Shadcn

    Backend:

      - FastAPI

    Database:

      - Neon PostgreSQL

      - Redis Cloud (for USSD)

    Automation:

      - n8n hosted separately

      - Webhook triggered from backend

    SMS and USSD:

      - Africa’s Talking API
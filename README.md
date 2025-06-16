# Simple-TASKa

**Simple-TASKa** is a lightweight preschool (TASKA) management system built using Pure PHP 8.3, MariaDB 11, and Bootstrap 5.3. It enables administrators, managers, teachers, and parents to collaborate efficiently to manage daily preschool activities, child records, billing, and logs.

## 📦 Tech Stack

- **Backend**: PHP 8.3 (Pure PHP, no framework)
- **Database**: MariaDB 11
- **Frontend**: Bootstrap 5.3
- **Email**: Basic PHP Mail or SMTP
- **Deployment**: Shared hosting, VPS or LAMP stack compatible

---

## 🧩 Features

### 🔐 Admin Panel
- Register new TASKA (Preschool) – dynamic name
- Add & update TASKA location and phone number
- Create and manage Managers
- Approve Parent and Baby registrations (with email notification)
- View and approve payments from parents

### 👨‍💼 Manager Panel
- Check-in / Check-out (attendance)
- Create and manage Teacher accounts
- Assign daily meal menu
- Create and manage school calendar (holidays/events)
- Approve Baby registrations
- Approve Log Book entries submitted by Teachers

### 👩‍🏫 Teacher Panel
- Check-in / Check-out
- Record Baby check-in/check-out (daily attendance)
- Fill and submit **Log Harian Kanak-Kanak** (Daily Child Log)
  - Health status
  - Meals
  - Milk intake
  - Diaper changes
  - Behaviour/incidents
  - Activities
  - Notes
- View assigned meal & school calendar

### 👨‍👩‍👧 Parent Portal
- Register and wait for approval (requires phone number [WhatsApp] & email)
- Register Babies under their account
- View **Daily Log Book** entries for their child
- View and pay Bills
- Email notifications on approval and billing

---

## 📂 Directory Structure (Coming Soon)

```bash
simple-taska/
├── README.md
├── public/
│   ├── index.php
│   ├── login.php
│   ├── logout.php
│   ├── assets/
│   │   ├── css/
│   │   │   └── style.css
│   │   ├── js/
│   │   │   └── app.js
│   │   └── images/
│   └── uploads/  # For baby photos, logbook images, etc.
├── src/
│   ├── controllers/
│   │   ├── AuthController.php
│   │   ├── AdminController.php
│   │   ├── ManagerController.php
│   │   ├── TeacherController.php
│   │   ├── ParentController.php
│   │   └── BabyController.php
│   ├── models/
│   │   ├── User.php
│   │   ├── Taska.php
│   │   ├── Baby.php
│   │   ├── LogBook.php
│   │   ├── Bill.php
│   │   └── Calendar.php
│   ├── views/
│   │   ├── admin/
│   │   │   ├── dashboard.php
│   │   │   └── manage_taska.php
│   │   ├── manager/
│   │   │   ├── dashboard.php
│   │   │   └── assign_calendar.php
│   │   ├── teacher/
│   │   │   ├── dashboard.php
│   │   │   └── fill_logbook.php
│   │   ├── parent/
│   │   │   ├── dashboard.php
│   │   │   └── view_logbook.php
│   │   ├── auth/
│   │   │   ├── login.php
│   │   │   └── register.php
│   │   └── shared/
│   │       ├── header.php
│   │       ├── footer.php
│   │       └── navbar.php
├── config/
│   ├── db.php
│   ├── mail.php
│   └── routes.php
├── database/
│   ├── schema.sql
│   └── seed.sql
├── utils/
│   ├── helpers.php
│   ├── auth.php
│   └── mailer.php
└── .env.sample

````

---

## 🚀 Getting Started

### Prerequisites

* PHP 8.3+
* MariaDB 11+
* Web server (Apache, NGINX)
* SMTP or PHP mail configured for email

### Setup Instructions

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/simple-taska.git
   cd simple-taska
   ```

2. Setup the database:

   * Import the SQL schema from `database/schema.sql`

3. Configure database:

   * Edit `/config/db.php` with your credentials

4. Set up your web server root to point to `/public`

5. Start building!

---

## 📧 Email Notifications

Uses PHP `mail()` or configurable SMTP for:

* Parent approval
* Baby registration approval
* Billing notifications

---

## 📖 License

This project is open-source and available under the MIT License.

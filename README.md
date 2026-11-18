# 🏥 Physiotherapy & Biomedical Management Platform

> A Unified Web Ecosystem for Clinical Rehabilitation and Biomedical Data Integration.

**Physiotherapy Management Platform** (also known as PhysioCare) is a comprehensive, multi-role web application designed to bridge the gap between physical therapy and biomedical engineering. It eliminates fragmented medical records by providing a centralized hub for patients, physiotherapists, and biomedical engineers to collaborate seamlessly.

This project was built as a **Senior Graduation Project** at the Lebanese International University.

---

## ✨ Key Features by Role

### 👤 1. Patient
* **Smart Booking:** Browse physiotherapist availability and book conflict-free time slots.
* **Transparent Recovery:** Access personal medical history, past injuries, and active treatment plans.
* **Home Training:** View assigned exercises and mark them as completed.
* **Billing & Feedback:** Manage invoices and rate therapy sessions.

### 🩺 2. Physiotherapist
* **Treatment Dashboard:** Build custom recovery plans while viewing the patient's full medical and diagnostic history.
* **Session Logging:** Record daily treatment notes, protocols, and upload session videos.
* **Biomedical Integration:** Direct access to specialized test results (e.g., EMG, ECG) shared by engineers.
* **Schedule Control:** Define and manage daily working hours, with automated expiration of past dates.

### 💻 3. Biomedical Engineer
* **Targeted Testing:** Administer and record specialized biomechanical tests.
* **Data Uploads:** Securely attach CSV datasets and medical imagery to patient profiles.
* **Inter-Specialty Collaboration:** Form system links with specific therapists to share insights instantly.

### 🛡️ 4. Administrator
* **User Management:** Approve, verify, and securely manage accounts across all system roles.
* **Partnership Setup:** Formally link Physiotherapists and Engineers to allow data sharing.
* **System Oversight:** Monitor clinic bookings, schedules, and overall platform health.

---

## 🛠️ Technology Stack

This project uses a modified **MERN-style** architecture, swapping MongoDB for MySQL to enforce strict relational data integrity for healthcare records.

* **Frontend:** React.js, HTML5, CSS3
* **Backend:** Node.js, Express.js
* **Database:** MySQL
* **Key Libraries & Tools:**
  * `bcrypt`: Secure password hashing and salting.
  * `multer`: Handling multipart/form-data for session videos and biomedical CSV uploads.
  * `node-cron` / MySQL Events: Automated database maintenance (e.g., expiring old availability slots).

---

## 🚀 Installation & Setup

Follow these steps to set up the project locally on your machine.

### Prerequisites
* [Node.js](https://nodejs.org/) installed
* [XAMPP](https://www.apachefriends.org/index.html) or any local MySQL server installed
* Git installed

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/physiotherapy-platform.git
cd physiotherapy-platform
```

### 2. Database Setup
1. Open XAMPP and start the **MySQL** module.
2. Open **phpMyAdmin** (usually `http://localhost/phpmyadmin`).
3. Create a new database named `physiotherapy_db`.
4. Import the provided `physiotherapy_db.sql` file into this new database to set up the 25 required tables (users, patients, appointments, treatment_plans, etc.).

### 3. Backend Setup
```bash
cd backend
npm install
```
Create a `.env` file in the `backend` folder and add your database credentials and secret keys:
```env
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=
DB_NAME=physiotherapy_db
JWT_SECRET=your_super_secret_jwt_key
PORT=5000
```
Start the backend server:
```bash
npm run dev
```

### 4. Frontend Setup
Open a new terminal window:
```bash
cd frontend
npm install
npm start
```
The application should now be running on `http://localhost:3000`.

---

## 🗺️ Database Mapping Overview
The database consists of **25 relational tables**. Key tables include:
* `users` & `patients` (Authentication & Demographics)
* `appointement` & `availability` (Scheduling Engine)
* `biomedical` & `biomedical_files` (Engineering Data)
* `treatment_plan`, `sessions`, & `training` (Clinical Execution)

---

## 🔮 Future Roadmap
- [ ] **Wearable Integration:** Sync live smartwatch data (heart rate, mobility).
- [ ] **AI Assistance:** Machine learning algorithms to suggest optimal treatment plans based on past biomedical data.
- [ ] **Telehealth:** Built-in video conferencing for remote, at-home therapy sessions.

---

## 👨‍💻 Developer
**Mohammad Abdallah**  
*Computer Science Department | Lebanese International University*
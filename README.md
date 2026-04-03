## RemuGen - A Digital Solution for University-Remuneration Billing

A comprehensive, web-based automated solution designed for academic institutions to streamline and modernize the calculation, management, and processing of faculty remunerations. This system replaces laborious manual billing processes with an efficient, transparent, and error-resistant digital workflow.

## 💡 Problem & Initial Idea

### The Problem

Historically, managing faculty remuneration at institutions like Khulna University involved several critical bottlenecks:

* **Manual Calculations:** Calculating payments for diverse academic tasks—such as question setting, script evaluation, and sessional assessments—was labor-intensive and prone to human error.
* **Operational Inefficiency:** The lack of automation led to significant delays in payment processing and hindered the overall administrative workflow.
* **Transparency Gaps:** Without a centralized digital record, tracking the status of billing requests and ensuring consistent application of rates was challenging for both faculty and the accounts department.

### The Solution

The **Remuneration Billing System** was developed as a modern web-based platform to bridge this digital gap. It simplifies the entire lifecycle of a remuneration bill by:

* Digitizing the submission and approval process.

* Utilizing a rule-based engine to automate complex financial calculations based on institutional policies.

* Providing a transparent, role-based interface where teachers can monitor their claims and accountants can verify data with high precision.

## ✨ Key Features

- **Automated Billing:** Automatically calculates payments based on teaching hours, research contributions, and administrative duties.

- **Invoice Generation:** Generates clear, well-formatted, and detailed PDF invoices for each teacher.

- **Approval Workflow:** Includes a structured review process where accountants can verify data, provide feedback, and approve payments.

- **Real-time Notifications:** Sends automated email notifications to faculty members once their remuneration is approved.

- **Role-Based Access Control (RBAC):** Distinct functional modules for Administrators, Teachers, and Accountants.

### 🛠 Tech Stack

- **Framework:** Laravel (PHP) – Utilizing MVC architecture for scalability and security.  
- **Database:** MySQL – Relational database for efficient management of records.  
- **Frontend:** Bootstrap & JavaScript (jQuery/AJAX) – Ensuring a responsive and interactive user interface.  


## 📊 System Design

The system was developed following the Waterfall Model of the Software Development Life Cycle (SDLC).

- **Database Normalization:** The schema is designed to minimize redundancy and ensure data integrity across entities.

- **Architecture:** Model-View-Controller (MVC) for clean separation of logic and presentation.



## 🧪 Testing

To ensure the reliability of financial data, the system underwent a rigorous testing phase:

- **Unit Testing:** Individual components, particularly calculation logic and database triggers, were tested in isolation.

- **Integration Testing:** Verified that modules like User Authentication, Bill Submission, and Notification Services worked seamlessly together.

- **User Acceptance Testing (UAT):** The system was evaluated against real-world scenarios to ensure an intuitive interface for faculty and accounting staff.

- **Boundary Value Analysis:** Focused on "Rate" and "Amount" fields to prevent mathematical overflows or incorrect billing cycles.


## ⚙️ Installation and Setup

Follow these steps to get a local copy of the project up and running.

### Prerequisites

* PHP (version 7 or higher)
* Composer
* A database system (MySQL, PostgreSQL, etc.)
* Node.js & npm (for front-end assets)

### 1. Clone the repository

```bash
git clone https://github.com/rajesh-mondal/RemuGen.git
cd RemuGen
```

### 2. Install Dependencies
Install the backend dependencies using Composer:
```bash
composer install
```

### 3. Environment Configuration
1. Copy the example environment file:
```bash
cp .env.example .env
```

2. Generate a unique application key:
```bash
php artisan key:generate
```

3. Generate a unique application key:
Edit the `.env` file and update your database credentials, JWT secret (if required), and any other necessary configuration:
```bash
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=remugen
DB_USERNAME=root
DB_PASSWORD=
```

### 4. Database Setup
Run the migrations to create the necessary tables 
```bash
php artisan migrate
```

### 4. Running the Application
Start the Laravel development server: 
```bash
php artisan serve
```
The application will typically be available at `http://127.0.0.1:8000`.

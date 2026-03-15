# Theme Park Management System

A full-stack web application designed to manage theme park operations, demonstrating database architecture, role-based access control, and dynamic data rendering. The application follows an MVC architecture.

## Technology Stack
- **Backend:** Node.js, Express.js
- **Frontend:** EJS (Embedded JavaScript templating), HTML, CSS
- **Database:** MySQL
- **Architecture:** Model-View-Controller (MVC)

## Core Features
- **Role-Based Access Control (RBAC):** Distinct dashboards and permissions for Admins, Park Managers, Location Managers, and Maintenance Staff.
- **Ride & Maintenance Management:** Track ride statuses, log operational runs, and submit/resolve maintenance tickets.
- **Inventory & Vendor Operations:** Manage park inventory, process restocks, and handle vendor checkouts.
- **Ticketing & Memberships:** Process customer ticket purchases and manage recurring member profiles.
- **Reporting Analytics:** Generate attendance, ride popularity, and closure impact reports.

## Project Structure

- **`app.js`**: Initializes the Express server, configures session management, and sets up middleware.
- **`db.js`**: Handles the database connection pool.
- **`routes/`**: Contains backend logic and API endpoints (e.g., `auth.js`, `rides.js`, `inventory.js`).
- **`views/`**: Contains the frontend templates rendered by EJS.
- **`middleware/`**: Custom middleware functions to enforce authentication and access control.
- **`sql/`**: Contains database initialization scripts, including schema definitions, stored procedures, triggers, and dummy data generation.

---

## Local Installation & Setup

To run this application locally, you will need **Node.js** and **MySQL** installed on your machine.

### 1. Database Initialization
1. Open MySQL Workbench (or your preferred MySQL client) and connect to your local MySQL server.
2. Create a new schema named `park_database`.
3. Locate the SQL dump file provided in the repository (e.g., `sql/park_database.sql` or `submission_dump.sql`).
4. Execute the SQL script to build the schema, insert stored procedures, and populate the database with sample data.

### 2. Environment Configuration
Create a `.env` file in the root directory of the project to store your local database credentials and session secrets. 

Add the following variables, updating the values to match your local MySQL setup:

DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_local_mysql_password
DB_NAME=park_database
DB_PORT=3306
SESSION_SECRET=your_secret_key


### 3. Run the Web Application
1. Open a terminal in the root directory of the cloned repository.
2. Install the required Node.js dependencies:
   npm install

3. Start the Express server:
   node app.js

4. Open your web browser and navigate to: **http://localhost:3000**

---

## Application Testing: Logins & Roles

The database is populated with sample employee accounts to test the Role-Based Access Control (RBAC) features.

**Default Password for ALL accounts:** `Clubhouse123`

### Key Management Roles

| Role | Email |
| :--- | :--- |
| **Admin** | `walt@park.com` |
| **Park Manager** | `minnie@park.com` |
| **Location Manager** (Main Entrance) | `mickey@park.com` |
| **Staff** (Main Entrance) | `daisy@park.com` |

### Maintenance Staff Roles

| Role | Email |
| :--- | :--- |
| Maintenance 1 | `goofy@park.com` |
| Maintenance 2 | `bob@park.com` |
| Maintenance 3 | `felix@park.com` |
| Maintenance 4 | `manny@park.com` |
| Maintenance 5 | `doc@park.com` |

> **Note:** You may also log in as any other employee found in the "Park Employees" list within the database using their email and the default password.

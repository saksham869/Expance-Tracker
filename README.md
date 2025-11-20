# Fullstack Expense Tracker

A **full-stack expense tracking web application** built using **Spring Boot**, **React.js**, and **MySQL**, designed to help users efficiently manage day-to-day finances.  
Supports **multi-role functionality** for users and admins.

---

## **Description**

- Developed a full-stack expense tracking application using **Spring Boot** (backend), **React.js** (frontend), and **MySQL** (database).  
- Facilitates seamless management of personal finances including income, expenses, and budgets.  
- Implements **multi-role user authentication**, enabling secure access for both regular users and administrators with sign-in, sign-up, password reset, and email verification features.  
- Developed **intuitive dashboards** for users to manage transactions, track upcoming/recurring payments, and view monthly summaries and statistics.  
- Admins can manage **categories, users, and transactions**, including search, filtering, and pagination.  

**Future Enhancements:**
- Integration of **Generative AI (RAG / GPT)** for intelligent insights and transaction analysis.  
- Fully **Dockerized deployment** for backend, frontend, and database.  

---

## **Features**

### User Features
- Sign-up, login, logout
- Password reset and email verification
- Profile management and profile picture upload/delete
- Create, edit, delete, and save recurring transactions
- Categorize transactions (Income / Expense)
- View monthly summaries, statistics, and budgets

### Admin Features
- Manage users, categories, and transactions
- Enable/disable users
- Search, filter, and paginate data
- Admin dashboard with statistics

---

## **How to Run**

### Step 1: Fork and Clone the Repository

```bash
git clone https://github.com/<your-username>/Expance-Tracker.git
cd Fullstack-Expense-Tracker-main
Step 2: Configure Environment Variables
Backend (backend/.env or application.properties):
properties
spring.datasource.url=jdbc:mysql://localhost:3306/YOUR_DATABASE_NAME
spring.datasource.username=YOUR_USERNAME
spring.datasource.password=YOUR_PASSWORD

spring.mail.username=YOUR_EMAIL
spring.mail.password=YOUR_EMAIL_PASSWORD
Frontend (frontend/.env):

REACT_APP_API_URL=http://localhost:8080
Step 3: Run Backend

cd backend
./mvnw spring-boot:run
Backend will automatically create required tables.

Add initial categories manually for Income and Expense.

To create an admin account, insert a user in users table with role ADMIN.

Step 4: Run Frontend

cd frontend
npm install
npm start
Open http://localhost:3000 to access the application.


Future Enhancements
AI Integration: Generative AI (RAG / GPT) for data insights

Docker Deployment: One-command deployment for backend, frontend, and MySQL

Expense forecasting, semantic search, and collaborative dashboards

# Fullstack Expense Tracker - Developer Documentation

## **Project Overview**
The **Fullstack Expense Tracker** is a full-featured financial management application, designed to help users track income and expenses while gaining actionable insights into their financial habits.

- **Frontend:** ReactJS
- **Backend:** Spring Boot (Java + Maven)
- **Database:** MySQL
- **Authentication:** Multi-role (Users & Admins) with secure email verification and password reset
- **Current Enhancements:** Generative AI (RAG / GPT) integration, Dockerization

This documentation is targeted at **developers, contributors, and future maintainers**, providing insights into the architecture, features, and roadmap.

---

## **Current Architecture & Workflow**

### **1. Backend (Spring Boot)**
- RESTful APIs for **users, transactions, and categories**
- Security via **Spring Security & JWT**
- Multi-role authentication (User/Admin)
- Services:
    - **UserService:** CRUD operations, role management, profile management
    - **TransactionService:** Manage income/expense, recurring transactions, saved templates
    - **CategoryService:** Admin-only category management

**Flow:**
Frontend (React) → HTTP Requests → Spring Boot Controllers → Services → MySQL Database

markdown
Copy code

### **2. Frontend (ReactJS)**
- Responsive UI for **dashboards, transaction management, and summaries**
- Components:
    - Auth (login/signup, email verification)
    - Dashboard (monthly summaries, charts)
    - Transactions (create/edit/delete, saved transactions)
    - Admin panels (user, category, transaction management)
- Communicates with backend via **REST APIs**

### **3. Database (MySQL)**
- Tables:
    - `users` – Stores user info, roles, and authentication data
    - `transactions` – Tracks all financial transactions
    - `categories` – Income/Expense categories
- Relationships:
    - One-to-many: `User → Transactions`
    - One-to-many: `Category → Transactions`

---

## **Current Features (Working)**
- **User Features**
    - Registration & login with email verification
    - Profile management and profile picture upload/delete
    - Transaction management (create, edit, delete)
    - Saved/recurring transactions
    - View monthly summaries, statistics, and charts

- **Admin Features**
    - Enable/disable users
    - Manage categories and transactions
    - Search, filter, and pagination for large datasets

---

## **Future Features / Roadmap**
### **1. AI Integration**
- **Generative AI / RAG:** Provide natural language insights using GPT-4 / GPT-3.5
- Semantic search of transactions using vector databases (Weaviate / Pinecone)
- Example queries:
    - “How much did I spend on groceries last month?”
    - “Highlight unusual spending patterns”
    - “Summarize weekly expenses and income”

### **2. Full Dockerization**
- Containerize:
    - Backend (Spring Boot)
    - Frontend (ReactJS)
    - Database (MySQL)
- Single-command deployment using `docker compose up --build`
- Ensures consistent environments across development, staging, and production

### **3. Advanced Analytics**
- AI-driven budgeting and predictive financial insights
- Recommendations for expense reduction
- Trend visualization for future spending

### **4. Improved UX/UI**
- Interactive dashboards and charts
- Notifications for recurring transactions
- Real-time summaries

---

## **Contribution Guidelines**
- Fork the repository
- Create a feature branch: `git checkout -b feature/<feature-name>`
- Commit your changes: `git commit -m "Add <feature>"`
- Push and create a Pull Request

**Recommended Contributions:**
- Implementing AI-driven features (RAG, GPT integration)
- Dockerization improvements for deployment
- Enhancing dashboards and analytics
- Optimizing backend APIs and database queries

---

## **Technical Notes**
- Spring Boot APIs are **stateless** and secured with JWT
- Frontend communicates over **REST** endpoints
- `.env` files are used for sensitive credentials and should **never** be committed
- Docker Compose orchestrates the **multi-container setup**

---

## **Visual Workflow Diagram**
+-------------------+ +-------------------+ +----------------+
| React Frontend | ---> | Spring Boot APIs | ---> | MySQL DB |
| (Dashboard/UI) | | (Services/Logic) | | (Users/Transactions/Categories) |
+-------------------+ +-------------------+ +----------------+
| ^
| |
| +---------------------------+
| | Generative AI / RAG Layer |
| | (GPT-4 / Semantic Search)|
+-------->| Provides Insights & Analysis|
+---------------------------+

----

## **Contact**
- GitHub: [https://github.com/saksham869/Expance-Tracker](https://github.com/saksham869/Expance-Tracker)
- Maintainer: Satyam Mishra

-------------------------------------------------------------------------------------------


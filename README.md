# Customer Churn & Retention Analytics

A web-based data analytics application that analyzes customer behavior and churn patterns to identify high-risk customer segments and generate business-focused retention insights.

## 🔗 Project Links

**Live Demo:** https://customer-churn-retention-analytics.vercel.app/

**GitHub Repository:** https://github.com/Prathiba-hub/customer-churn-retention-analytics

---

## 📌 About the Project

Customer churn is an important business problem where customers stop using a company's products or services.

The goal of this project is to analyze customer data and understand **who is churning, which customer groups are at higher risk, and what factors are associated with customer churn**.

The project uses data analytics and visualization techniques to transform raw customer data into meaningful business insights.

This project focuses on **data analysis and business intelligence rather than machine learning**.

---

## 🎯 Objectives

* Analyze customer churn patterns
* Understand customer behavior
* Identify high-risk customer segments
* Analyze customer retention trends
* Compare churn across different customer groups
* Visualize important business metrics
* Generate actionable retention recommendations

---

## 🛠️ Technology Stack

### Frontend

* React.js
* Vite
* Tailwind CSS
* JavaScript / TypeScript

### Data & Analytics

* Python
* Pandas
* NumPy
* SQL
* Matplotlib
* Seaborn

### Database

* Supabase

### Development & Deployment

* VS Code
* Git
* GitHub
* Vercel

---

## ✨ Key Features

### 📊 Customer Analytics

Analyze customer information and identify patterns in customer behavior.

### 📉 Churn Analysis

Analyze the overall churn rate and understand how churn varies across different customer groups.

### 👥 Customer Segmentation

Compare customer groups based on factors such as:

* Customer tenure
* Contract type
* Payment method
* Demographics
* Service usage

### 🔎 High-Risk Customer Identification

Identify customer segments that show higher churn rates and may require retention strategies.

### 📈 Interactive Visualizations

Present analytical results through interactive charts and dashboards.

### 💡 Business Recommendations

Convert analytical findings into practical recommendations that businesses can use to improve customer retention.

---

## 📊 Key Analysis Areas

The project analyzes several aspects of customer behavior:

* Customer demographics
* Customer tenure
* Contract type
* Payment method
* Service usage
* Churn status
* Retention patterns
* Customer segments
* High-risk groups
* Revenue-related patterns

---

## ❓ Business Questions

The project helps answer questions such as:

1. What percentage of customers are churning?
2. Which customer segments have the highest churn?
3. Does customer tenure affect churn?
4. Which contract types have better retention?
5. Which payment methods are associated with higher churn?
6. Which customers should businesses prioritize for retention campaigns?
7. What factors are commonly observed among churned customers?

---

## 📈 Dashboard & Application

The application provides an interactive interface for exploring customer analytics and business insights.

### Main capabilities

* Customer overview
* Churn analysis
* Customer segmentation
* Trend analysis
* Interactive visualizations
* Business insights
* Retention recommendations


## 🔄 Data Analytics Workflow

```text
Raw Customer Data
       ↓
Data Cleaning
       ↓
Data Exploration
       ↓
SQL Analysis
       ↓
Customer Segmentation
       ↓
Churn Analysis
       ↓
Data Visualization
       ↓
Business Insights
       ↓
Retention Recommendations
```

---

## 🗄️ Database

The project uses **Supabase** for storing and retrieving application data.

The application connects to Supabase using environment variables.

Environment variables required:

```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

> ⚠️ Never upload your `.env` file or expose secret credentials in GitHub.

---

## 🚀 Run the Project Locally

### 1. Clone the repository

```bash
git clone https://github.com/Prathiba-hub/customer-churn-retention-analytics.git
```

### 2. Navigate to the project

```bash
cd customer-churn-retention-analytics
```

### 3. Install dependencies

```bash
npm install
```

### 4. Create the environment file

Create a `.env` file in the project root:

```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

### 5. Start the development server

```bash
npm run dev
```

The application will be available at the local Vite development URL.

---

## 🌐 Deployment

The application is deployed using **Vercel**.

The GitHub repository is connected to Vercel, allowing the application to be automatically redeployed when changes are pushed to the repository.

**Live Demo:** Add your Vercel URL here

---

## 📁 Project Structure

```text
customer-churn-retention-analytics/
│
├── public/
│
├── src/
│   ├── components/
│   ├── pages/
│   ├── assets/
│   └── ...
│
├── index.html
├── package.json
├── package-lock.json
├── vite.config.ts
├── tailwind.config.js
├── tsconfig.json
├── .gitignore
└── README.md
```

---

## 💼 Business Value

This project demonstrates how customer data can be transformed into actionable business information.

Businesses can use this type of analysis to:

* Identify customers at higher risk of churn
* Prioritize retention campaigns
* Understand customer behavior
* Improve customer experience
* Reduce customer loss
* Make data-driven decisions

---

## 🎓 Skills Demonstrated

* Data Analytics
* Exploratory Data Analysis
* Customer Churn Analysis
* Customer Segmentation
* Business Intelligence
* SQL
* Python
* Pandas
* NumPy
* Data Visualization
* React.js
* Tailwind CSS
* Supabase
* Git
* GitHub
* Vercel
* Business Insight Generation

---

## 👩‍💻 Author

**Prathiba Devendiran**

B.Sc. Computer Science with Artificial Intelligence

GitHub: https://github.com/Prathiba-hub

---

## 📄 License

This project was developed for educational, portfolio, and demonstration purposes.

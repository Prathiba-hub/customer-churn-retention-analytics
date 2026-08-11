# Customer Churn &amp; Retention Analytics Platform

A full-featured analytics platform that ingests customer data via CSV upload, cleans and validates it, stores it in PostgreSQL, and computes churn rates, customer segments, revenue analysis, and data-driven retention recommendations — all displayed through an interactive dashboard.

## Features

- **CSV Upload &amp; Data Cleaning** — Drag-and-drop upload with automatic missing-value imputation (median for numerics, mode for categoricals), duplicate removal, invalid row detection, and a Data Quality Score
- **Interactive Dashboard** — 7 KPI cards and 6 charts (churn trends, churn by plan/contract/segment, revenue by segment, satisfaction vs churn) with multi-select filters for date range, plan, contract type, city, gender, and churn status
- **Customer Explorer** — Searchable, sortable, filterable, paginated customer table with a detail drawer showing per-customer behavior stats and a computed churn risk score
- **Churn Analysis** — Churn breakdowns by plan, contract, tenure bucket, satisfaction level, support ticket volume, purchase frequency, and age group, plus auto-generated findings derived from the actual data
- **Customer Segmentation** — Automatic segmentation into High Value Loyal, High Value At Risk, New Customers, Low Engagement, and Support Heavy, each with count, revenue, churn rate, and average spend
- **Revenue Analysis** — Total revenue, revenue by plan/city/segment, top customers, revenue trend, and a highlighted Revenue at Risk figure
- **Retention Recommendations** — Prioritized, data-driven recommendations with expected revenue impact
- **Reports** — Full report preview with one-click download

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React 18 + TypeScript + Vite |
| Styling | Tailwind CSS |
| Charts | Recharts |
| Icons | Lucide React |
| Routing | React Router |
| Database | Supabase (PostgreSQL) with Row Level Security |
| CSV Parsing | PapaParse |

## Getting Started

### Prerequisites

- Node.js 18+
- A Supabase project (free tier works fine)

### Installation

1. Clone the repo
   ```bash
   git clone https://github.com/YOUR_USERNAME/customer-churn-analytics.git
   cd customer-churn-analytics
   ```

2. Install dependencies
   ```bash
   npm install
   ```

3. Create a `.env` file in the project root with your Supabase credentials
   ```env
   VITE_SUPABASE_URL=your_supabase_project_url
   VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
   ```

4. Run the database migration — go to your Supabase project's SQL Editor and run the SQL in `supabase/migrations/20260808143749_create_churn_analytics_tables.sql`. This creates the `datasets` and `customers` tables with Row Level Security policies.

5. Start the dev server
   ```bash
   npm run dev
   ```

6. Open `http://localhost:5173` in your browser.

### Using the App

1. Start on the Home page and click **Get Started**
2. On the Upload page, click **Download Sample CSV** to get a template, then upload it (or upload your own CSV)
3. Review the Data Quality Report
4. Navigate through the sidebar to explore the Dashboard, Customers, Churn Analysis, Segments, Revenue, Recommendations, and Reports

### CSV Column Format

Your CSV should include some or all of these columns (the app maps common variations automatically):

| Canonical Field | Acceptable Header Variations |
|-----------------|------------------------------|
| customer_id | Customer ID, customerid, cust_id |
| age | Age |
| gender | Gender |
| city | City, Location |
| subscription_plan | Plan, Subscription Plan, plan_type |
| contract_type | Contract, Contract Type, contract |
| monthly_charges | Monthly Charges, Monthly, monthly_revenue |
| total_spend | Total Spend, Total Revenue, total_revenue |
| tenure_months | Tenure, Tenure Months, tenure |
| login_frequency | Login Frequency, Logins, login_freq |
| purchase_frequency | Purchase Frequency, Purchases |
| support_tickets | Support Tickets, Tickets, support_calls |
| satisfaction_score | Satisfaction Score, Satisfaction, csat |
| churned | Churn, Churned, churn_status |

## Build

```bash
npm run build      # production build
npm run typecheck  # type checking only
npm run lint       # eslint
```

## Project Structure

```
src/
├── components/          # Layout shell, reusable UI components
├── lib/
│   ├── analytics.ts     # Analytics engine (KPIs, churn, segments, recommendations)
│   ├── columns.ts       # CSV header → canonical field mapping
│   ├── data-context.tsx # Global state + Supabase data provider
│   ├── supabase.ts      # Supabase client
│   └── upload.ts        # CSV parsing, cleaning, imputation, quality scoring
├── pages/               # 9 route pages (Home, Upload, Dashboard, etc.)
├── types.ts             # Shared TypeScript types
└── App.tsx              # Router + route definitions
supabase/
└── migrations/          # SQL migration (tables + RLS policies)
```


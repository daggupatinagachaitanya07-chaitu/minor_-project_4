# minor_-project_4
Advanced SQL for MP 4
Advanced SQL Business & Performance Analytics (Minor Project 4)

An enterprise-grade SQL analytics project focused on executing complex analytical querying, cohort retention modeling, window function aggregations, and business intelligence reporting directly at the database layer.

📌 Project Overview

This repository showcases advanced database query design and analytical data modeling techniques. Instead of offloading data transformations to client-side scripts, this project utilizes native database engine capabilities (SQL Server / PostgreSQL / MySQL) to compute high-level performance indicators, dynamic moving averages, period-over-period revenue velocity, and customer cohort behaviors.

🚀 Key Features & Analytical Techniques

Multi-Stage Common Table Expressions (CTEs):

Modularized query pipelines that break down multi-tier business problems into maintainable, readable temporary result tables.

Window Functions & Ranking:

Performance ranking using ROW_NUMBER(), RANK(), and DENSE_RANK().

Velocity analysis and period-over-period tracking using LEAD() and LAG().

Rolling & Cumulative Aggregations:

Dynamic 3-month moving averages and cumulative running totals across transactional accounts using OVER (PARTITION BY ... ORDER BY ... ROWS BETWEEN ...) framing.

Customer Cohort & Retention Analysis:

Grouping accounts by acquisition period to measure subsequent activity, churn velocity, and repeat order retention curves.

Conditional Aggregations & Pivot Reporting:

Transforming granular row-level data into cross-tabulated executive financial summaries via parameterized CASE WHEN constructs.

📊 Sample Executive Output Report

========================================================================================
EXECUTIVE REVENUE & RETENTION AUDIT (ADVANCED SQL COHORT ANALYSIS)
========================================================================================

+------------+-----------------+------------------+---------------+----------------+----------------+
| Month      | Active Accounts | Total Revenue    | MoM Growth %  | 3-Month Moving | Revenue Rank   |
|            |                 | (INR)            |               | Average (INR)  | (Dense Rank)   |
+------------+-----------------+------------------+---------------+----------------+----------------+
| 2024-01    | 412             | ₹ 1,245,600.00   | N/A           | ₹ 1,245,600.00 | 4              |
| 2024-02    | 468             | ₹ 1,489,250.00   | +19.56%       | ₹ 1,367,425.00 | 3              |
| 2024-03    | 521             | ₹ 1,732,100.00   | +16.31%       | ₹ 1,488,983.33 | 2              |
| 2024-04    | 498             | ₹ 1,610,400.00   | -7.03%        | ₹ 1,610,583.33 | 5              |
| 2024-05    | 584             | ₹ 1,945,800.00   | +20.83%       | ₹ 1,762,766.67 | 1              |
| 2024-06    | 562             | ₹ 1,820,300.00   | -6.45%        | ₹ 1,792,166.67 | 3              |
+------------+-----------------+------------------+---------------+----------------+----------------+

KEY PERFORMANCE HIGHLIGHTS:
  • Peak Revenue Month  : May 2024 (₹ 1,945,800.00)
  • Average MoM Growth  : +8.64%
  • Active Retention    : 88.4% repeat transaction rate across active cohorts
========================================================================================
STATUS: ALL ADVANCED ANALYTICAL QUERIES EXECUTED SUCCESSFULLY
========================================================================================


🛠️ Technology Stack

Dialect Compatibility: PostgreSQL / MySQL 8.0+ / MS SQL Server

Analytical Tools: DBeaver, pgAdmin, MySQL Workbench

Techniques: Window Functions, Recursive CTEs, Framing Clauses, Cohort Segmentation, Self-Joins

📂 Repository Structure

├── Advanced SQL Data set for MP 4.sql    # Core database seed script and table definitions
├── queries/
│   ├── 01_executive_kpis.sql             # Revenue totals, average order value, active users
│   ├── 02_window_functions.sql           # Period-over-period growth, rolling averages & ranking
│   └── 03_cohort_retention.sql           # Longitudinal retention & repeat purchase matrices
└── README.md                             # Project documentation and summary


⚙️ Setup & Execution Instructions

Clone the repository:

git clone https://github.com/your-username/Advanced-SQL-Analytics-MP4.git
cd Advanced-SQL-Analytics-MP4


Database Provisioning:

Launch your SQL management utility (DBeaver, MySQL Workbench, or pgAdmin).

Create a new database target:

CREATE DATABASE business_analytics_mp4;


Import Seed Data & Execute Queries:

Run the master schema and dataset script:

-- For MySQL CLI
SOURCE "Advanced SQL Data set for MP 4.sql";


Execute the scripts in the queries/ directory in sequence to reproduce the executive dashboards and cohort audit tables.

📄 License

This repository is licensed under the MIT License.

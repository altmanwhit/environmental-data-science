# Phase 1: Azure SQL & Database Engineering

**Duration:** Months 1–3 | **Status:** 🔄 In Progress

---

## What I'm Building

A production-ready Azure SQL database to store and serve ESG (Environmental, Social, Governance) data for environmental consulting projects. This is a real project at my firm — this repo documents the learning and methodology behind it using synthetic data.

---

## Learning Objectives

- [ ] Design normalized relational schemas for complex environmental/ESG data
- [ ] Deploy and configure Azure SQL Database (vs. Managed Instance vs. Synapse — know the differences)
- [ ] Write advanced SQL: window functions, CTEs, stored procedures
- [ ] Build ETL pipelines with Azure Data Factory
- [ ] Connect Python (pandas + SQLAlchemy) to Azure SQL
- [ ] Implement row-level security and basic data governance
- [ ] Optimize queries with proper indexing strategies

---

## Projects in This Phase

### 1. ESG Schema Design
> `notebooks/01_esg_schema_design.ipynb`

Designing the entity-relationship model for an ESG database covering:
- Environmental metrics (emissions, water use, waste, spills)
- Regulatory compliance tracking
- Site-level vs. company-level data hierarchy
- Temporal versioning for regulatory reporting cycles

### 2. Azure SQL Deployment Walkthrough
> `notebooks/02_azure_sql_setup.ipynb`

Step-by-step deployment of an Azure SQL instance, including:
- Service tier selection and cost considerations
- Firewall and network configuration
- Connecting from Python with SQLAlchemy
- Basic security configuration

### 3. Advanced Query Library
> `scripts/esg_queries.sql`

A library of reusable SQL queries for common ESG reporting needs:
- Rolling averages for emissions trends
- Year-over-year comparisons
- Multi-site aggregations with window functions
- Data quality checks

### 4. Python-to-Azure ETL Pipeline
> `notebooks/03_python_azure_etl.ipynb`

Building a pandas → Azure SQL pipeline that:
- Reads raw ESG data from CSV/Excel inputs
- Validates and transforms data
- Loads to Azure SQL with error handling and logging

---

## Courses Completed

| Course | Platform | Completed |
|--------|----------|-----------|
| Introduction to SQL | DataCamp | ⬜ |
| Intermediate SQL | DataCamp | ⬜ |
| Database Design | DataCamp | ⬜ |
| Azure Data Fundamentals (DP-900) | Coursera/Microsoft | ⬜ |
| Microsoft Learn: Azure SQL Fundamentals | Microsoft Learn | ⬜ |

---

## Key Lessons Learned

*Updated as I go — this is where the real learning gets documented.*

---

## Resources

- [Microsoft Azure SQL Documentation](https://docs.microsoft.com/en-us/azure/azure-sql/)
- [SQLAlchemy + Azure SQL connection guide](https://docs.sqlalchemy.org/en/14/dialects/mssql.html)
- [Azure Data Factory documentation](https://docs.microsoft.com/en-us/azure/data-factory/)

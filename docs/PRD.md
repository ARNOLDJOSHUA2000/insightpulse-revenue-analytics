

\# InsightPulse — Product Requirements Document



\*\*Document Version:\*\* 0.1  

\*\*Status:\*\* Draft  

\*\*Project:\*\* InsightPulse — Revenue Analytics Web Application  

\*\*Dataset:\*\* Olist Brazilian E-Commerce Public Dataset



\---



\## 1. Product Vision



Build an interactive revenue analytics application that helps e-commerce stakeholders understand sales performance, identify trends and make evidence-based business decisions.



\## 2. Problem Statement



E-commerce businesses generate substantial transactional data, but raw data alone does not provide clear business insights.



InsightPulse will transform historical transaction data into meaningful KPIs, visualisations and analytical findings.



\## 3. Target Users



| User | Primary Need |

|---|---|

| Business Owner | Understand overall business performance |

| Sales Manager | Identify sales trends and category performance |

| Marketing Manager | Understand customer purchasing patterns |

| Operations Manager | Explore order and delivery performance |

| Data Analyst | Investigate trends and generate insights |



\## 4. Product Objectives



1\. Provide a reliable overview of e-commerce sales performance.

2\. Enable users to explore historical sales trends.

3\. Identify high-performing and underperforming categories.

4\. Analyse customer purchasing behaviour.

5\. Support business decisions through evidence-based insights.



\## 5. MVP Scope



\### Must Have



\- Revenue overview dashboard.

\- Total delivered orders.

\- Merchandise sales.

\- Average Order Value (AOV).

\- Monthly sales trends.

\- Product and category analysis.

\- Date and geographic filters.

\- Data quality validation.



\### Should Have



\- Repeat customer analysis.

\- Geographic sales comparisons.

\- Period-over-period growth.

\- Exportable analytical reports.



\### Could Have



\- Advanced customer segmentation.

\- Automated analytical summaries.

\- Additional interactive visualisations.



\### Out of Scope for MVP



\- Real-time sales monitoring.

\- Live inventory management.

\- AI-generated recommendations.

\- Profit margin calculations without reliable cost data.

\- Competitor analysis.



\## 6. Functional Requirements



| ID | Requirement |

|---|---|

| FR-01 | Display key revenue and order KPIs |

| FR-02 | Display monthly sales trends |

| FR-03 | Allow date-based filtering |

| FR-04 | Analyse product category performance |

| FR-05 | Compare geographic sales performance |

| FR-06 | Analyse repeat customer behaviour |

| FR-07 | Validate analytical results against SQL calculations |



\## 7. Non-Functional Requirements



\- Accuracy: KPI calculations must follow documented definitions.

\- Reliability: Invalid or missing data must be handled appropriately.

\- Performance: Dashboard interactions should remain responsive.

\- Security: Database credentials must not be exposed.

\- Maintainability: Application logic should be modular.

\- Testability: Core calculations must have automated tests.

\- Usability: Visualisations should be understandable to business users.



\## 8. Data Requirements



The project will use relevant Olist dataset tables, including:



\- Orders

\- Order Items

\- Customers

\- Products

\- Sellers

\- Payments

\- Reviews

\- Category Translation



Each table's grain, primary keys, relationships and data quality issues must be documented before analytical joins are implemented.



\## 9. Data Limitations and Assumptions



\- The dataset contains historical transactions, not live business activity.

\- Monetary values are represented in Brazilian Real (R$).

\- Merchandise sales are based on item prices and exclude freight.

\- Complete business cost data is unavailable; profit margin cannot be reliably calculated.

\- Repeat customer analysis must use customer\_unique\_id.

\- One-to-many joins must be controlled to prevent duplicated sales.

\- KPI definitions and eligible order populations must be documented.



\## 10. Product Success Criteria



\- KPI calculations reconcile with independently executed SQL queries.

\- Core analytical transformations pass automated tests.

\- Users can filter and explore the main dashboard.

\- Data quality issues are identified and documented.

\- The application is successfully deployed with project documentation.



\## 11. Risks



| Risk | Mitigation |

|---|---|

| Missing or inconsistent data | Data quality checks |

| Incorrect KPI definitions | Central KPI Dictionary |

| Duplicate sales from joins | Validate table grain and join cardinality |

| Slow dashboard performance | Optimise SQL and data loading |

| Credential exposure | Environment variables and .gitignore |



\## 12. Development Roadmap



1\. Product planning and repository setup.

2\. Dataset exploration and data profiling.

3\. PostgreSQL database design and ingestion.

4\. SQL analytics and KPI development.

5\. Python application development.

6\. Testing, CI/CD and deployment.



\---



\*\*Document Note:\*\* This PRD is an initial draft. Requirements may be refined after dataset profiling and technical validation.








\# InsightPulse — Revenue Analytics Web Application



\## 1. Project Overview



InsightPulse is a data analytics web application designed to help e-commerce businesses understand revenue performance, identify sales trends, evaluate product categories and make data-driven business decisions.



The application uses the Olist Brazilian E-Commerce dataset to demonstrate an end-to-end analytics workflow.



\## 2. Business Problem



E-commerce businesses generate large volumes of transactional data but often struggle to convert that data into meaningful business insights.



InsightPulse aims to address this by providing:

\- Revenue performance monitoring.

\- Sales trend analysis.

\- Product and category performance analysis.

\- Customer purchasing behaviour analysis.

\- Geographic sales insights.

\- Business-focused analytical recommendations.



\## 3. Technology Stack



| Area | Technology |

|---|---|

| Programming | Python |

| Database | PostgreSQL |

| Data Analysis | Pandas, NumPy |

| Query Language | SQL |

| Visualization | Plotly |

| Web Application | Streamlit |

| Testing | Pytest |

| Code Quality | Ruff |

| Version Control | Git, GitHub |

| CI/CD | GitHub Actions |



\## 4. Dataset



\*\*Source:\*\* Olist Brazilian E-Commerce Public Dataset.



The project will analyse historical Brazilian e-commerce transactions.



All monetary values will be represented in Brazilian Real (R$).



\## 5. Planned Architecture



Olist Dataset → Python Data Ingestion → PostgreSQL → SQL Analytics → Python Analysis → Streamlit Dashboard → Business Insights



\## 6. Key Business Metrics



\- Merchandise Sales

\- Total Delivered Orders

\- Average Order Value (AOV)

\- Sales Growth

\- Category Sales

\- Units Sold

\- Repeat Customer Rate



Metric definitions and calculation rules will be documented in the KPI Dictionary.



\## 7. Project Structure



```text

InsightPulse/

├── app/

├── src/

│   └── insightpulse/

├── data/

│   ├── raw/

│   └── processed/

├── sql/

├── tests/

├── docs/

├── .github/

│   └── workflows/

├── .env.example

├── .gitignore

└── README.md

```



\## 8. Development Status



Currently in the product planning and repository setup phase.



Planned development stages:



1\. Product requirements and KPI definitions.

2\. Dataset exploration and data quality assessment.

3\. PostgreSQL database design and ingestion.

4\. SQL transformations and analytics.

5\. Streamlit application development.

6\. Testing, CI/CD and deployment.



\## 9. Project Goals



\- Build a production-oriented analytics application.

\- Demonstrate practical SQL and Python skills.

\- Apply data engineering and analytical best practices.

\- Deliver actionable business insights.

\- Publish a documented, tested and deployed portfolio project.



\## 10. Disclaimer



This is a portfolio project using a historical public dataset. Its analytical outputs should not be interpreted as real-time business performance or audited financial statements.






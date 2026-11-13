

\# InsightPulse — KPI Dictionary



\*\*Version:\*\* 0.1  

\*\*Status:\*\* Draft — pending dataset validation  

\*\*Currency:\*\* Brazilian Real (R$)



\---



\## 1. Merchandise Sales



\*\*Definition:\*\* Total value of eligible merchandise sold, excluding freight charges.



\*\*Calculation:\*\*



SUM(order\_items.price)



\*\*Source:\*\* Order Items and Orders.



\*\*Population:\*\* Items belonging to delivered orders, using the purchase-date reporting period.



\*\*Business purpose:\*\* Understand merchandise sales performance.



\*\*Important:\*\* This is not accounting revenue or profit.



\---



\## 2. Total Delivered Orders



\*\*Definition:\*\* Number of distinct orders successfully delivered.



\*\*Calculation:\*\*



COUNT(DISTINCT order\_id)



\*\*Source:\*\* Orders.



\*\*Filter:\*\* order\_status = 'delivered'.



\*\*Business purpose:\*\* Measure completed order volume.



\---



\## 3. Average Order Value (AOV)



\*\*Definition:\*\* Average merchandise value per delivered order.



\*\*Calculation:\*\*



Merchandise Sales / Total Delivered Orders



\*\*Source:\*\* Orders and Order Items.



\*\*Business purpose:\*\* Understand average transaction value.



\*\*Rule:\*\* Numerator and denominator must use the same eligible order population and reporting period.



\---



\## 4. Sales Growth



\*\*Definition:\*\* Percentage change in merchandise sales compared with the previous equivalent period.



\*\*Calculation:\*\*



((Current Period Sales - Previous Period Sales)

&#x20;/ Previous Period Sales) \* 100



\*\*Business purpose:\*\* Identify increases or decreases in sales.



\*\*Rule:\*\* If previous-period sales are zero, display growth as undefined rather than dividing by zero.



\---



\## 5. Units Sold



\*\*Definition:\*\* Number of eligible order-item records associated with delivered orders.



\*\*Calculation:\*\*



COUNT(order\_item\_id)



\*\*Source:\*\* Order Items and Orders.



\*\*Business purpose:\*\* Understand product demand and sales volume.



\---



\## 6. Category Sales



\*\*Definition:\*\* Merchandise sales grouped by product category.



\*\*Calculation:\*\*



SUM(order\_items.price)



Grouped by translated product category.



\*\*Source:\*\* Order Items, Products and Category Translation.



\*\*Business purpose:\*\* Identify high-performing and underperforming categories.



\*\*Rule:\*\* Validate joins to prevent duplicated order-item records.



\---



\## 7. Repeat Customer Rate



\*\*Definition:\*\* Percentage of distinct customers who placed at least two delivered orders during the full observation window.



\*\*Calculation:\*\*



(Number of unique customers with 2+ delivered orders

&#x20;/ Number of unique customers with 1+ delivered orders) \* 100



\*\*Customer identifier:\*\* customer\_unique\_id.



\*\*Source:\*\* Orders and Customers.



\*\*Business purpose:\*\* Understand repeat purchasing behaviour.



\*\*Rule:\*\* Use customer\_unique\_id rather than customer\_id to identify the same underlying customer across orders.



\---



\## 8. Geographic Sales



\*\*Definition:\*\* Merchandise sales grouped by customer location.



\*\*Calculation:\*\*



SUM(order\_items.price)



Grouped by customer state or city.



\*\*Source:\*\* Orders, Order Items and Customers.



\*\*Business purpose:\*\* Identify geographic sales concentration.



\---



\## 9. General KPI Rules



1\. Monetary values must remain in Brazilian Real (R$).

2\. Merchandise sales exclude freight.

3\. Delivered-order KPIs must use a consistent order population.

4\. Distinct order counts must use order\_id.

5\. Repeat customer analysis must use customer\_unique\_id.

6\. One-to-many joins must be checked for duplication.

7\. Every KPI must be validated against an independent SQL calculation.

8\. Missing or invalid values must be documented.

9\. Profit and profit margin must not be reported without reliable cost data.



\---



\## 10. Validation Status



All definitions are initial proposals.



Final calculations will be confirmed after:

\- Dataset profiling.

\- Primary and foreign key validation.

\- Order-status analysis.

\- Join-cardinality checks.

\- SQL reconciliation.




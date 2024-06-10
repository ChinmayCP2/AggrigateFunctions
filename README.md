# AggrigateFunctions and Sequence clause in SQL
Example of using sub query along with aggrigate function
```sql
select a.customer_id,a.item, c.country, a.countOfItems from (select distinct customer_id, item, count(item) as countOfItems
from Orders
group by customer_id, item) as a join Customers c on a.customer_id = c.customer_id;
Uisng multiple colums for group by
```
```sql
select distinct customer_id, item, count(item) as countOfItems
from Orders
group by customer_id, item;
```
Also basic Example

```sql
select age, Count(customer_id) as Count 
from Customers 
group by age;
```
customer count based on age
and

```sql
SELECT OrderID, SUM(Quantity) AS [Total Quantity]
FROM OrderDetails
GROUP BY OrderID; ```

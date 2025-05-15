# pizzahut-sql-project

# Pizzahut SQL Project

An SQL analysis project on pizza sales, featuring:

- ERD and schema design
- Data views for business insights
- Optimized queries using indexes and subqueries
- Visual dashboards

## Files

- `schema.sql`: Table creation statements
- `views.sql`: Useful analysis views
- `indexes_and_queries.sql`: Indexes and optimized queries
- `images/`: Screenshots of ERD and dashboards

## Sample Queries

```sql
-- View to get monthly sales
SELECT * FROM monthly_sales;

-- Subquery to find top 5 best-selling pizza types
SELECT name FROM pizza_types
WHERE id IN (
  SELECT pizza_type_id FROM pizzas
  GROUP BY pizza_type_id
  ORDER BY SUM(quantity) DESC
  LIMIT 5
);

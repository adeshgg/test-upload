# Joins

Any 2 columns with the same type can be joined,
Ideal join primary key of 1 table with foreign key of other

Joins are there to filter the rows, by default if returns all the columns from both the tables
You can specify the columns to need in the select statement



**Syntax**

```sql
Select * from Left_table_name join Right_table_name ON Left_table.primary_key = Right_table.foreign_key
```

**Types of Joins**

Inner join: only get the over lap (intersection between the 2 tables)
Left join: Do give the intersection rows, but even if any row from the 1st table doesn't have a match include it with null values
Right join: intersection rows + all the other rows from the right table (all the right joins can be transformed in left joins)
Full Outer join: intersection + all the other rows from left table + all the other rows from the right table
Union Join: Join the value of 2 columns of the same type and gives there union (return a single column)
Cross Join: Each value of the first table's given column is attached with the second table's column (cross product)

```sql
select column_name from left_table union select column_name from right_table;
```

```sql
select left_table.column, right_table.column from left_table cross join right_table;
```


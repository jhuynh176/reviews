- [What are some ways that SQL is used in data science?](#what-are-some-ways-that-sql-is-used-in-data-science)
- [Are all databases relational?](#are-all-databases-relational)
- [Does every SQL statement follow this structure?](#does-every-sql-statement-follow-this-structure)
- [What happens if we try to create a table with an existing name?](#what-happens-if-we-try-to-create-a-table-with-an-existing-name)
- [What order are rows selected from a table?](#what-order-are-rows-selected-from-a-table)
- [Can we add a column at a specific position to a table?](#can-we-add-a-column-at-a-specific-position-to-a-table)
- [How is ALTER different from UPDATE?](#how-is-alter-different-from-update)
- [What if we only want to delete a specific number of rows?](#what-if-we-only-want-to-delete-a-specific-number-of-rows)
- [What are some reasons to apply constraints to a table?](#what-are-some-reasons-to-apply-constraints-to-a-table)
- [What types of data can SQLite databases store?](#what-types-of-data-can-sqlite-databases-store)
- [Can we alias multiple columns in a single query?](#can-we-alias-multiple-columns-in-a-single-query)
- [Can we apply DISTINCT to a SELECT query with multiple columns?](#can-we-apply-distinct-to-a-select-query-with-multiple-columns)
- [Can we compare values of two columns in a WHERE clause?](#can-we-compare-values-of-two-columns-in-a-where-clause)
- [Can we apply the LIKE operator to values other than TEXT?](#can-we-apply-the-like-operator-to-values-other-than-text)
- [How do we search for patterns containing the actual characters “%” or “_”?](#how-do-we-search-for-patterns-containing-the-actual-characters--or-_)
- [When storing missing data, should I store them as NULL?](#when-storing-missing-data-should-i-store-them-as-null)
- [When applying the BETWEEN operator on TEXT values, how are values compared?](#when-applying-the-between-operator-on-text-values-how-are-values-compared)
- [Is the `AND` used in `BETWEEN` the same as the `AND` operator between conditions?](#is-the-and-used-in-between-the-same-as-the-and-operator-between-conditions)
- [Can we write conditions using both AND and OR?](#can-we-write-conditions-using-both-and-and-or)
- [Can we apply ORDER BY with multiple columns?](#can-we-apply-order-by-with-multiple-columns)
- [What if we set a LIMIT value that is greater than the total number of rows?](#what-if-we-set-a-limit-value-that-is-greater-than-the-total-number-of-rows)
- [When using a CASE statement, do the values for THEN have to be a single type?](#when-using-a-case-statement-do-the-values-for-then-have-to-be-a-single-type)
- [What is a function?](#what-is-a-function)
- [Does `COUNT()` include duplicate values of a column?](#does-count-include-duplicate-values-of-a-column)
- [When do we use `COUNT()` or `SUM()`?](#when-do-we-use-count-or-sum)
- [How can we get the average of unique values of a column?](#how-can-we-get-the-average-of-unique-values-of-a-column)
- [If multiple rows have the minimum or maximum value, which one is returned when using MAX/MIN?](#if-multiple-rows-have-the-minimum-or-maximum-value-which-one-is-returned-when-using-maxmin)
- [Does the `ROUND()` function round up?](#does-the-round-function-round-up)
- [When using GROUP BY, do we always have to group by a selected column?](#when-using-group-by-do-we-always-have-to-group-by-a-selected-column)
- [Do column references have to follow the order the columns are listed in the SELECT?](#do-column-references-have-to-follow-the-order-the-columns-are-listed-in-the-select)
- [Can a WHERE clause be applied with a HAVING statement in the same query?](#can-a-where-clause-be-applied-with-a-having-statement-in-the-same-query)
- [Are there guidelines to splitting a table as provided in the example?](#are-there-guidelines-to-splitting-a-table-as-provided-in-the-example)
- [Given a value that is not a unique identifier, can we determine a unique identifier?](#given-a-value-that-is-not-a-unique-identifier-can-we-determine-a-unique-identifier)
- [When doing an INNER JOIN, are columns matched on NULL values?](#when-doing-an-inner-join-are-columns-matched-on-null-values)
- [Does the order of tables in a JOIN matter?](#does-the-order-of-tables-in-a-join-matter)
- [When should I use INNER JOIN instead of LEFT JOIN?](#when-should-i-use-inner-join-instead-of-left-join)
- [Is it possible for a table to have more than one unique identifier column?](#is-it-possible-for-a-table-to-have-more-than-one-unique-identifier-column)
- [Can you CROSS JOIN on more than two tables?](#can-you-cross-join-on-more-than-two-tables)
- [What happens if tables we perform UNION on have duplicate rows?](#what-happens-if-tables-we-perform-union-on-have-duplicate-rows)
- [Can we use WITH for more than one nested query in SQL?](#can-we-use-with-for-more-than-one-nested-query-in-sql)

# What are some ways that SQL is used in data science?
In the field of data science, there is a process, called the Data Science process, which provides a structured approach to performing experiments with data. In this data science process, some important steps include obtaining data, cleaning and organizing data, and exploring the data. Using tools like SQL, scientists are able to perform these important steps.

When obtaining data, scientists can use SQL to store them in tables and databases.

Once they have obtained the data, they can clean and organize the data utilizing built-in functions and clauses, to do things such as grouping them according to some qualities or conditions. They can also separate the data into different tables based on what kind of information they represent.

After these steps, they will be able to explore the data by utilizing many of the built-in SQL functions, which include functions such as AVG() which returns the average value of a column.

With its many built-in functions and ease-of-use, SQL is a very useful tool to have for data science.

# Are all databases relational?
No, not all databases are relational databases. Databases can be non-relational, and this type of database is referred to as NoSQL databases.

NoSQL databases are structured differently from the relational database structure. With relational, we structure tables by the type of relations, but NoSQL keeps all the information in one place, in the form of key-values or documents.

# Does every SQL statement follow this structure?
In general, SQL statements will usually follow a similar structure as the given example SQL statement, but depending on what you are trying to do, they can also look very different.

The following are some examples of different kinds of SQL statements you might use, which will be covered throughout this lesson.

This statement selects all rows from a table.

```
SELECT * FROM table;
```

This statement will create a new table.

```
CREATE TABLE students (
  column_1 data_type,
  column_2 data_type
);
```

This statement will update a row in a table.

```
UPDATE table
SET column_1 = new_value
WHERE id = 3;
```

# What happens if we try to create a table with an existing name?
When you try to create a table with an already existing table name, you will receive an `error message`, and no table will be modified or created.

Because SQLite (used in the exercises) is case insensitive for most syntax including names, this will apply to any casing of the table name. For instance, given the celebs table from this exercise, if you tried to run the following, it will throw an error, because the table name already exists.

# What order are rows selected from a table?
In most SQL databases, by default, the rows will be selected in the order that they appear in the table, from top to bottom. For instance, if you have a statement like
SELECT * FROM table this will select all rows from the table from the first row that appears down to the bottom row.

# Can we add a column at a specific position to a table?
`No`, unfortunately, you cannot specify what position to add a column to a table.

`By default, a new column will always be added at the end of the table`. For most intents and purposes, this should not affect much, since you can always select the columns in any order, for instance, like

SELECT col3, col1, col2
If column order is very important, then an alternative is to create a new table and add the columns in the specific order they should appear.

# How is ALTER different from UPDATE?
Although similar in the sense that both statements will modify a table, these statements are quite different.

The `ALTER` statement is used to modify `columns`. With ALTER, you can `add columns`, `remove` them, or even `modify` them.

The `UPDATE` statement is used to modify `rows`. However, UPDATE can only `update` a row, and `cannot remove` or `add rows`.

# What if we only want to delete a specific number of rows?
To delete only a specific number of rows, you can utilize the LIMIT statement. The value provided for LIMIT will be how many rows to affect.

For example, this statement will only delete the first 5 rows that match the condition,

```
DELETE FROM table
WHERE condition
LIMIT 5;
```

# What are some reasons to apply constraints to a table?
Applying constraints to a table can be useful, and provide some important benefits such as reliability and consistency of your data. The following are a few reasons you might consider for applying constraints to a table.

One reason for adding constraints is to prevent invalid data in the table. This is very important, because invalid data can cause issues and unexpected results from calculations. We do not have to worry about new data being added that might otherwise violate our constraints and cause bigger issues.

Similar to the previous point, constraints can let us prevent missing data, which is usually filled as NULL within the table. Instead of having missing values set to NULL, we can set constraints so that the missing values are given some default value instead, like 0. This can make some calculations easier to do.

Another important reason to add a constraint is for uniqueness, usually in the form of values like the id, or identifier column. By using a constraint like the PRIMARY KEY, we can ensure that every row has their own unique id value.

# What types of data can SQLite databases store?
SQLite databases can store several different types of data. Some of the most common data types, which we will encounter in this course, are INTEGER, TEXT and REAL.

The INTEGER type is for a signed whole number, such as -25, 0, 100, …

The TEXT type is similar to strings in other programming languages, and stores a sequence of characters like ‘123 parkway street’.

The REAL type includes floating point values, like 1.5, 3.141, 103.3333, …

It is worth noting that the values of each data type can take the state of NULL (covered in exercise 8) which denotes a lack of value.

# Can we alias multiple columns in a single query?
Yes, you can alias multiple columns at a time in the same query.

It is advisable to always include quotes around the new alias. Quotes are required when the alias contains spaces, punctuation marks, special characters or reserved keywords. It is simply more convenient to always include quotes around the new alias.

```
SELECT course_id AS "Course ID", exercise_id AS "Exercise ID"
FROM bugs;
```

# Can we apply DISTINCT to a SELECT query with multiple columns?
Let’s assume that in the Codecademy database there is a table bugs which stores information about opened bug reports. It might have columns like course_id, exercise_id, reported_by, reported_date, report_url, etc. For the purpose of this example, let’s say that this is our table:

| `id` | `course_id` | `exercise_id` | `reported_by` |
| :--- | :---------- | :------------ | :------------ |
| 1    | 5           | 4             | Tod           |
| 2    | 5           | 4             | Alex          |
| 3    | 5           | 3             | Roy           |
| 4    | 5           | 4             | Roy           |
| 5    | 7           | 4             | Alex          |
| 6    | 7           | 8             | Tod           |
| 7    | 14          | 2             | Alex          |
| 8    | 14          | 4             | Tod           |
| 9    | 14          | 6             | Tod           |
| 10   | 14          | 2             | Roy           |

Community Manager would like to know the names of the users who have reported bugs in order to send them a special Thank You note. We can use a SELECT query with DISTINCT keyword to pick unique values from the reported_by column:

```
> SELECT DISTINCT reported_by FROM bugs;

reported_by
Alex
Tod
Roy
```

Awesome! Exactly what we were expecting!

Our coworker would like to know in which exercises bugs have been reported. This gets trickier because now we have to query two columns: course_id and exercise_id. Let’s try to use the same approach as before:

```
> SELECT DISTINCT course_id, exercise_id FROM bugs;

course_id	exercise_id
14			2
5			4
14			4
14			6
5			3
7			4
7			8
```

Is this the result we were hoping for? Yes. It is true that there are duplicated values in the course_id and exercise_id, but every row is unique (there are no two rows with the same value in course_id and exercise_id).


# Can we compare values of two columns in a WHERE clause?
Yes, within a `WHERE` clause you can compare the values of two columns.

When comparing two columns in a `WHERE` clause, for each row in the database, it will check the value of each column and compare them.

```
/* 
This will return all rows where the value in the 
x column is greater than the y column value. 
*/

SELECT x, y
FROM coordinates
WHERE x > y;
```

# Can we apply the LIKE operator to values other than TEXT?
Yes, you can apply the `LIKE` operator to numerical values as well.

Whenever you use `LIKE` however, you must always wrap the pattern within a pair of quotations, whether for matching a number or a string.

```
/* 
This will select movies where the id number
starts with 2 and is followed by any two numbers.
*/
SELECT * 
FROM movies
WHERE id LIKE '2__';
```

# How do we search for patterns containing the actual characters “%” or “_”?
When searching for a pattern containing the specific characters `%`or `_`, we can utilize the escape character `\`, similarly to its use in Python.

If we want to search for these specific characters, we can simply add the escape character immediately before them.

```
/* 
In this pattern, we use an escape character before '%'.
This will only match "%" and not be used like the
wildcard character.

This query will match any titles that end with
' 100%'.
*/

SELECT *
FROM books
WHERE title LIKE '% 100\%';
```

# When storing missing data, should I store them as NULL?
It can depend entirely on how you need the data to be stored and utilized.

Let’s say that you have a table of employee information, which included their address. Say that we wanted to check all rows of this table and find where any addresses are missing. If we stored the addresses as TEXT values, we might choose to store all the missing values as either '' or as NULL.

If we stored the missing address values as an empty string '' then these values are not NULL. Empty strings are seen as a string of length 0. So, if we ran a query using

WHERE address IS NULL

it would not give us the rows with missing address values. We would have to check using

WHERE address = ''

With a table containing many different data types, it may be helpful and more convenient to store any missing values in general as just NULL so that we can utilize the IS NULL and IS NOT NULL operators.

# When applying the BETWEEN operator on TEXT values, how are values compared?
In most programming languages, including SQLite and Python, TEXT or string values are compared based on their lexicographical ordering, and when using the BETWEEN operator for a range of TEXT values in SQL, the values will be sorted in this way.

Lexicographical ordering is basically the ordering you would find words in a dictionary. If we had two words, they would be compared starting from their first letter, second letter, and so on, until we find a non-matching letter. The word which has the letter that comes first in the alphabet would ultimately be sorted to come first in this lexicographical ordering.

If two words have different lengths, but match up to the last letter of the shorter word, the shorter word will appear first in the ordering.

```
A = "Alien"
B = "Aliens"
C = "Alike"

/* 
   Because A and B share the same sequence of characters 
   up to the last character of A, which is shorter, A < B. 

   Also, because "k" comes after "e" in the alphabet, C will 
   come last in the ordering of these 3 words.

   A < B < C
*/
```

# Is the `AND` used in `BETWEEN` the same as the `AND` operator between conditions?
No, although they may be assumed to be the same thing, the AND used with a BETWEEN, like

BETWEEN 1990 AND 1999

is not quite the same AND used when combining multiple conditions. When used in a BETWEEN statement, we are not combining two separate conditions, but providing a range of values to obtain the values within that range.

However, we can easily rewrite a BETWEEN to one with two conditions, like these queries which would be identical.

```
SELECT *
FROM movies
WHERE year BETWEEN 1990 AND 1999;

SELECT * 
FROM movies
WHERE year >= 1990
AND year <= 1999;
```

# Can we write conditions using both AND and OR?
Yes, queries can combine multiple conditions using AND and OR without a real limit to how many conditions you can combine. However, the more conditions you combine, the more specific the results will be and the more complex it can get.

```
/* 
This will select movies with id values 
from 10 to 20 inclusive, OR with id 
values from 50 to 60 inclusive.
*/
SELECT *
FROM movies
WHERE
(id > 10 AND id < 20)
OR
(id > 50 AND id < 60);
```

# Can we apply ORDER BY with multiple columns?
Yes, following the ORDER BY, you can list more than one column for which to order the data by.

When ordering by more than one column, it will first order the data on the first column, then, keeping the previous column order, it will order on the next column, and so on.

You can also specify ascending or descending order for each listed column.

```
/* 
This will order on the year, then order the 
names in reverse alphabetical 
order, preserving the order
of the year column.
*/

SELECT year, name
FROM movies
ORDER BY year ASC, name DESC;
```

# What if we set a LIMIT value that is greater than the total number of rows?
If the number set in the LIMIT clause surpasses the number of rows available to select, then it will just exclude the remaining amount of rows in the result set.

You might think of LIMIT as an upper bound for the number of rows to return, but not as a strict number of rows that must be returned.

```
/* 
Say the table `name` has only 90 rows. 
Then, since 100 is greater than the number of rows, 
it will just return what rows are there. 
*/

SELECT *
FROM names
LIMIT 100;
```

# When using a CASE statement, do the values for THEN have to be a single type?
No, for CASE statements, the THEN values do not have to return only a single type of value. In fact, you can have each THEN in a single CASE statement return different value types such as TEXT, REAL, and INTEGER.

```
SELECT 
  CASE
    WHEN condition1 THEN "text"
    WHEN condition2 THEN 100
    WHEN condition3 THEN 3.14
  END AS 'example'
FROM table;
```

# What is a function?
A very general description of a function would be: A set of tasks or procedures that can take in a value, and return another value based on that input.

Functions in programming are similar to ones that you may have seen in math. For example,

`f(x, y) = x^2 + y^2`

If we use this function with two input values, it would return the sum of the squares of both values.

Similarly, in SQL, aggregate functions can take in a column name of a table, and will return some numerical value based on the column values. For example,

`SELECT COUNT(col) FROM table;`

This will return a single number, which is the number of rows that have non-empty values in the column col.

Some functions we will learn about later can even take values directly, instead of just column names, like

`ROUND(10.4, 0)`

and will return a value based on the input. The above would result in 10.0.

# Does `COUNT()` include duplicate values of a column?
Yes, when using the `COUNT()` function on a column in SQL, it will include duplicate values by default. It essentially counts all rows for which there is a value in the column.

If you wanted to count only the unique values in a column, then you can utilize the DISTINCT clause within the `COUNT()` function.

```
/* This will return 22, the number of distinct category values. */
SELECT COUNT(DISTINCT category)
FROM fake_apps;
```

# When do we use `COUNT()` or `SUM()`?
Although they might appear to perform a similar task, the `COUNT()` and `SUM()` functions have very different uses.

`COUNT()` is used to take a name of a column, and counts the number of non-empty values in that column. `COUNT()` does not take into account the actual values stored, and only cares if they have a non-empty value. Each row is essentially counted as 1 towards the total count.

On the other hand, `SUM()` takes a column name, and returns the sum of all values in the column, meaning that it must take into account the actual values stored.

In general, use `COUNT()` when you want to count how many rows contain a non-empty value for a specified column. Use `SUM()` when you want to get the total sum of all values in a column.

# How can we get the average of unique values of a column?
To run the AVG() function on a column such that it only averages the unique values in the column, we could use the DISTINCT clause right before the column name.

```
/* Returns 2.02365 */
SELECT AVG(price)
FROM fake_apps;

/* Returns 4.15833.. */
SELECT AVG(DISTINCT price)
FROM fake_apps;
```

# If multiple rows have the minimum or maximum value, which one is returned when using MAX/MIN?
Typically, when you have more than one row that contains the minimum or maximum value in a column, the topmost row containing that value will be returned in the result.

For example, if the table contained multiple rows with the minimum price of 0.0, then the result of a query with MIN(price) will choose the topmost row from the table that had this price value.

```
/* 
This should return the siliconphase app, because
it was the topmost row that had the minimum price 
value of the column. 
*/
SELECT id, name, MIN(price)
FROM fake_apps;
```

# Does the `ROUND()` function round up?
When using the `ROUND()` function, you can provide a second argument, which is the precision, or number of decimal places to round the number on.

In SQLite, rounding is done by rounding up if the next decimal value is 5, and rounds down if the value is less than 5.

```
/* This will result in 4.0 */
SELECT ROUND(3.5, 0);

/* This will result in 6.4 */
SELECT ROUND(6.42, 1);

/* This will result in 6.0 */
SELECT ROUND(6.42, 0);
```

# When using GROUP BY, do we always have to group by a selected column?
No, you can `GROUP BY` a column that was not included in the `SELECT` statement.

For example, this query does not list the price column in the `SELECT`, but it does group the data by that column.

```
SELECT name, downloads
FROM fake_apps
GROUP BY price;
```

However, usually we do include the grouped by column in the `SELECT` for the sake of clarity, so that it’s easier to see what rows belong to which group.

# Do column references have to follow the order the columns are listed in the SELECT?
No, once you list the columns after the `SELECT`, they can be referenced by the order they appeared, starting from 1 for the first listed column.

You are not limited to referencing them in the exact order they were listed, like

`GROUP BY 1, 2, 3`

You can freely use the references in any order, like you would normally without using references.

`GROUP BY 3, 1, 2`

However, when using references, it is important to always keep in mind what numbers referenced which column, as it can become confusing as you list more columns in the `SELECT`. It is a convenient shortcut, but not necessarily always the best choice.

# Can a WHERE clause be applied with a HAVING statement in the same query?
Yes, you can absolutely apply a WHERE clause in a query that also utilizes a HAVING statement.

When you apply a WHERE clause in the same query, it must always be before any GROUP BY, which in turn must be before any HAVING.

As a result, the data is essentially filtered on the WHERE condition first. Then, from this filtered data, it is grouped by specified columns and then further filtered based on the HAVING condition.

```
/* 
This will first filter the movies with a box_office > 500000.
Then, it will group those results by genre, and finally restrict
the query to genres that have more than 5 movies.
*/

SELECT genre, ROUND(AVG(score))
FROM movies
WHERE box_office > 500000 
GROUP BY genre
HAVING COUNT(*) > 5;
```

# Are there guidelines to splitting a table as provided in the example?
Yes, although there might not necessarily be a one-fits-all solution to every possible database structure, there are some guidelines that can help you when you need to split a table into multiple tables.

A concept that most programmers use to refer to restructuring a database in this manner is `“Database Normalization”`. A very brief explanation of this concept is that it aims to accomplish that databases tables are structured so that they **`avoid data redundancy`** and keep the data `accurate` and `consistent`. **`“Data redundancy”`** is when we have a lot of repeated, or redundant, data.

In the example given in this exercise, it explains how we might split a table into multiple tables, which is essentially doing normalization. Initially, the table has many columns, and as a result, some of the values will most likely be repeated many times, which introduces data redundancy.

Say for example, we added 1 million rows to this table. Some values like `customer_address` might end up being stored many thousands of times, when we really only need to store it once per customer.

To avoid this issue, we would split the table so that the information is stored more concisely. If we need the customer information, we can obtain it from the customers table, by their customer_id. And, if we need the information for a subscription, all of its information is stored in the subscriptions table. We only need the `customer_id` and `subscription_id` in the orders table, and we can obtain their information from their respective tables.

# Given a value that is not a unique identifier, can we determine a unique identifier?
No, if you are given a value other than a unique identifier column, like order_id, subscription_id, or customer_id, we cannot determine a unique identifier for the value.

What this means is, say we’re given a customer name of “John Smith”. There is no guarantee that there is only one “John Smith” within the customers table. There could one, or even a dozen entries with this name.

Given a customer_id, we can always determine their customer_name. But, the other way would not apply, because if we were given a customer_name, we could not determine their customer_id. Given the name “John Smith”, there might be 10 customer_id's with that name.

As a result, it is either very difficult and usually not possible to determine id values given a non-unique column value, which are columns other than the id columns.

# When doing an INNER JOIN, are columns matched on NULL values?
No, when you have NULL values in a column, these are never matched to other NULL values. This is because NULL signifies the absence of any value, and cannot be compared as they will never equal anything. `Doing say NULL = NULL results in False`.

Let’s take for example the animation given in the exercise, which shows how INNER JOIN works. Let’s say that an additional row was added to each table, with NULL in the C2 column, such that they become

Left table:
```
C1, C2
A, B
Q, W
X, Y
T, NULL
```

Right table:
```
C2, C3
B, C
E, R
Y, Z
NULL, V
```

If we inner joined these tables the same way, we would end up with the same result, because NULL values are not matched.
```
C1, C2, C3
A, B, C
X, Y, Z
```

# Does the order of tables in a JOIN matter?
Generally, no, the order of the tables in the JOIN will not affect the overall results of the query.

As long as you specify what columns to select, the results should appear essentially the same, just that the rows will be ordered according to the appearance in the first table.

However, if you do not specify specific columns, then the order of columns will be different depending on the order of the tables. Without specifying columns in your SELECT, by using just SELECT *, the result query will order the columns by the first table’s columns followed by the second table’s columns.

For example, say we had two tables:
`orders, with the columns order_id, customer_id`
and
`customers, with the columns customer_id, address`.

If we run the following query,
```
SELECT *
FROM orders
JOIN customers
ON orders.customer_id = customers.customer_id;
```

the columns in this query’s results will be ordered from left to right as:
order_id, customer_id, customer_id, address

Conversely, if we ran this query,
```
SELECT *
FROM customers
JOIN orders
ON orders.customer_id = customers.customer_id;
```

it will return the columns in the following order from left to right:
`customer_id, address, order_id, customer_id`

If the order of your columns matters in the result query, then it will be important to keep this in mind.

# When should I use INNER JOIN instead of LEFT JOIN?
Depending on how we want to select the combined data, it can determine whether to use an `INNER JOIN` or a `LEFT JOIN`.

Generally, we use `INNER JOIN` when we want to select only rows that match an ON condition. If no rows match the `ON` condition, then it will not return any results. This can be somewhat stricter than using a `LEFT JOIN`.

We use a `LEFT JOIN` when we want every row from the first table, regardless of whether there is a matching row from the second table. This is similar to saying,
“Return all the data from the first table no matter what. If there are any matches with the second table, provide that information as well, but if not, just fill the missing data with NULL values.”

In a way, `LEFT JOIN` is less strict than `INNER JOIN`. Furthermore, the results of a `LEFT JOIN` will actually include all results that an `INNER JOIN` would have provided for the same given condition.

# Is it possible for a table to have more than one unique identifier column?
Yes, it is possible for a table to have more than one column which can uniquely identify a row of data. A column that can uniquely identify a record of data is known as a "Candidate Key". Tables can have multiple "Candidate Key"s, each of which could potentially be the "Primary Key", but there must only be one "Primary Key" per table. Usually, the column chosen as the "Primary Key" follows the naming convention like customer_id or product_id.

For example, say that we had a table of employee records, with the columns employee_id and phone_number. Every employee has a unique employee_id value, and a unique phone_number value. Both of these columns can be unique identifiers for a row, so they are "Candidate keys", but the "Primary Key" would most likely be set to employee_id.

# Can you CROSS JOIN on more than two tables?
Yes, you can CROSS JOIN as many tables as you want.

Let’s build upon the example from the exercise, which had the tables shirts and pants, and add a third table for socks.

We can perform the CROSS JOIN for all three tables, like so
```
SELECT shirts.shirt_color,
pants.pants_color,
socks.sock_color
FROM shirts
CROSS JOIN pants
CROSS JOIN socks;
```

If the tables had 3 shirts, 2 pants, and 6 socks, then the result of this CROSS JOIN will give

3 x 2 x 6 = 36 combinations, or 36 total rows.

One thing to note is that when you use CROSS JOIN without a WHERE clause, like the example above, we get every single combination of the table rows.

As a result, this can quickly grow larger as you CROSS JOIN more tables because the growth is multiplicative.

# What happens if tables we perform UNION on have duplicate rows?
When you combine tables with UNION, duplicate rows will be excluded.

To explain why this is the case, recall a Venn Diagram, which shows the relations between sets. If we perform UNION on two sets of data (tables), say A and B, then the data returned in the result will essentially be
`A + B - (A intersect B)`

In the first part,
`A + B`
will add together all the rows of both tables, including duplicates.

The second part,
`- (A intersect B)`
will remove every duplicate, which is where A and B intersected.

If, however, you wanted to include duplicates, certain versions of SQL provides the UNION ALL operator.

# Can we use WITH for more than one nested query in SQL?
Yes, you can use WITH for more than one nested query. You can do so by listing each query using commas after the WITH.

```
WITH
query1 AS (SELECT column1 FROM table1 WHERE condition1),
query2 AS (SELECT column2 FROM table2 WHERE condition2)
…
```

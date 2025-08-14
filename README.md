# Lab Assignment 25

The purpose of this lab assignment is to familiarize yourself with SQL databases and the SQL programming language.

### Before you begin

Before your start working on this lab assignment. Install the following extensions into VS Code.

- SQLite
- SQLite Viewer

The **SQLite** extension will allow you to run query commands from the `src/commands.sql` file and the **SQLite Viewer** extension will visualize what's in your `src/database.db`. 

## SQL Database

An SQL database, also known as a relational database, is a system that stores and organizes data into structured tables composed of rows and columns, similar to a spreadsheet.

These databases use Structured Query Language (SQL) as the standard programming language to manage, query, and manipulate the data, enabling operations like creating tables, inserting, reading, and deleting data.

The following commands can be executed in your `src/commands.sql` file. Simply high light the query, right-click, and select "Run Query".

### Create a table

Any command sent to the database is known as a **query**. To create a table in SQL, run a query using the format shown below.

```sql
CREATE TABLE table_name ( column_name1 DATA_TYPE, column_name2 DATA_TYPE, ... );
```

What if you're unsure if the table has already been created? Run the query below to avoid any errors.

```sql
CREATE TABLE IF NOT EXISTS table_name (column_name1 DATA_TYPE, column_name2 DATA_TYPE, ... );
```

### Insert into a table

To insert a new row of information or entry, run the query below.

```sql
INSERT INTO table_name ( column_name1, column_name2, ... ) VALUES ( "example", 123, ... );
```

### Read from a table

To read from a table, you can either read the entire table using the command below.

```sql
SELECT * FROM table_name;
```

Or you can read from a specific entry or row.

```sql
SELECT * FROM table_name WHERE column_nameX = "some value";
```

### Delete from a table

To delete from a row or entry from a table you can use the command below.

```sql
DELETE FROM table_name WHERE column_nameX = "some value";
```

What if you want to delete all rows or entries? In that case, use this command instead.

```sql
DELETE FROM table_name;
```

## Your Assignment

Your assignment is to create the **amazon** and **clinic** tables shown below and insert the entires shown as well.

### amazon

| id | name | email | prime_member |
| --- | --- | --- | --- |
| 112 | "Bob Bobbert" | "bob@gmail.com" | 1 |
| 117 | "Carl Carlton" | "carl@yahoo.com" | 0 |
| 127 | "Jane Janeson" | "jane@aol.com" | 1 |
| 186 | "Dan Danbert" | "dan@hotmail.com" | 0 |

**Complete the following tasks:**

- Print out only users who are prime members.

- Bob has closed his Amazon account, so please remove him after completing the table.

### clinic

| id | firstName | lastName | weight | age |
| --- | --- | --- | --- | --- |
| 4231 | "Bob" |  "Bobbert" | 180.5 | 20 |
| 1578 | "Carl" | "Carlton" | 201.3 | 24 |
| 2697 | "Jane" | "Janeson" | 130.6 | 21 |
| 7852 | "Dan" | "Danbert" | 160.7 | 30 |

**Complete the following tasks:**

- Print out all patient information.

- Jane has moved to another clinic, so please remove her after completing the table.
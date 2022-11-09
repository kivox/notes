---
{"dg-publish":true,"permalink":"/computer-science/databases/revision/","dgHomeLink":true,"dgPassFrontmatter":false}
---


- # 1.3.2 Databases - Revision
	- What is a Database?
		- A database is an organized collection of data stored and accessed electronically.
		- Relational Database
			- A relationship in databases allow you to reuse data and link multiple records together.
			- An example of a relation use is when a user uses a login system, once the user logs in they might have relations to projects they hold access to, and then what other members that project holds. This is a relationship consisting of 3 tables, Users, Members, and Projects.
		- Flat File
			- A flat file database is a database stored in a file called a flat file.
			- Records follow a uniform format, and there are no structures for indexing or recognizing relationships between records.
			- The file is simple. A flat file is usually a plain text file, or in some cases like SQLite they're a binary file. 
			- What makes flat file databases differ from normal relational databases is the fact that, they only have one table.
		- Primary Key
			- A primary key is the column or columns that contain values that uniquely identify each row in a table.
			- A database table must have a primary key to insert, update, or delete data from a database table.
		- Foreign key
			- A foreign key is a set of attributes in a table that refers to the primary key of another table. The foreign key links these two tables.
		- Secondary key
			- A secondary key is an additional key, or alternate key, which can be used in addition to the primary key to locate specific data.
		- Entity relationship modelling
			- Entity Relationship Model is a high-level conceptual data model diagram.
			- ER model helps to draw out an environment based on data requirements to produce a well-designed database.
			- The ER Model represents entities and the relationships between them.
	- Methods of Capturing, Selecting, Managing and Exchanging Data
		- [SQL Keywords](https://www.w3schools.com/sql/sql_ref_keywords.asp)
			- CREATE
				- Creates a database, index, view, table, or procedure
			- SELECT
				- Selects data from a database, an example of getting all fields from a user record would be 
					- `SELECT * FROM tbl_users WHERE ID = 1 LIMIT 1;` 
			- ALTER
				- Adds, deletes, or modifies columns in a table, or changes the data type of a column in a table
			- UPDATE
				- Updates existing rows in a table
			- DROP
				- Deletes a column, constraint, database, index, table, or view
			- DELETE
				- Deletes rows from a table
			- FROM
				- Specifies which table to select or delete data from
			- WHERE
				- Filters a result set to include only records that fulfill a specified condition
			- JOINS
				- Joins tables, combines the tables together to query them simultaneously
			- LIMIT
				- Specifies the number of records to return in the result set
			- ORDER BY
				- Sorts the result set in ascending or descending order
	- Normalization
		- Database normalization is the process of structuring a relational database in accordance with a series of so-called normal forms in order to reduce data redundancy and improve data integrity.
	- Normal Forms
		- Normal forms are the rules that normalization is based on, these rules make it so that it eliminates data redundancy within databases.
		- 1NF
			- A table is in first normal form if it contains no repeating attributes or groups of attributes. All attributes must be atomic – a single attribute cannot consist of two data items such as first-name and surname. This would make it difficult or impossible to sort on surname.
				-   Each cell should contain a single value
				-   Each record needs to be unique
		- 2NF
			- A table is in second normal form (2NF) if it is in first normal form and contains no partial dependencies.
				- Be in 1NF
				- Single Column Primary Key that does not functionally dependant on any subset of candidate key relation
		- 3NF
			- A table is in third normal form if it is in second normal form and contains no non-key dependencies. All attributes depend on the key
				- Be in 2NF
				- Has no transitive functional dependencies
	- Referential Integrity
		- Referential integrity is a property of data stating that all its references are valid. In the context of relational databases, it requires that if a value of one attribute (column) of a relation (table) references a value of another attribute (either in the same or a different relation), then the referenced value must exist.
		- In simpler terms, making sure all relations in a database are valid, you can't create a project attached to a user if the user doesn't exist.
		- From markscheme
			- Ensuring that changes are consistent across a database
			- If a record is removed all references to it are removed
			- A foreign key value must have a corresponding Primary key value in another table.
			- In this case, a user being removed will result in their reviews being removed / a restaurant being removed will result in its reviews being removed.
	- Transaction Processing
		- Transaction processing is information processing that is divided into individual, indivisible operations called transactions.
		- Each transaction must succeed or fail as a complete unit; it can never be only partially complete.
	- ACID
		- ACID stands for atomicity, consistency, isolation, and durability
			- Atomicity
				- In a transaction involving two or more discrete pieces of information, either all the pieces are committed or none are.
			- Consistency
				- A transaction either creates a new and valid state of data, or, if any failure occurs, returns all data to its state before the transaction was started.
			- Isolation
				- A transaction in process and not yet committed must remain isolated from any other transaction.
			- Durability
				- Committed data is saved by the system such that, even in the event of a failure and system restart, the data is available in its correct state.
		- Following ACID is always accomplished by the use of transactions.
		- ACID ensure the highest possible data reliability and integrity.
		- ACID ensures that your data never falls into an inconsistent state because of an operation that only partially completes.
	- Record Locking
		- Record locking is the technique of preventing simultaneous access to data in a database, to prevent inconsistent results.
		- The classic example is demonstrated by two bank clerks attempting to update the same bank account for two different transactions.
			- Clerks 1 and 2 both retrieve (i.e., copy) the account's record.
			- Clerk 1 applies and saves a transaction.
			- Clerk 2 applies a different transaction to his saved copy, and saves the result, based on the original record and his changes, overwriting the transaction entered by clerk 1.
			- The record no longer reflects the first transaction, as if it had never taken place.
			- A simple way to prevent this is to lock the file whenever a record is being modified by any user, so that no other user can save data.
				- This prevents records from being overwritten incorrectly, but allows only one record to be processed at a time, locking out other users who need to edit records at the same time.
	- Redundancy
		- Data redundancy often refers to having the same data stored multiple times. This is useful in case of corruption and dataloss, but in terms of databases it makes them worse at what they do, you would have to update all occurances of data, to update that piece of data. It takes up more storage, it works against the rules of the normal forms.
		- It is advised to avoid data redundancy within relational databases, however, Data Redundancy has another meaning aswell, keeping a backup of data incase of an unlikely occurance such as dataloss.

Create a Database
```sql
CREATE TABLE Users (
	ID        int,
	Firstname varchar(32),
	Lastname  varchar(32),
);
```

Create a record inside database
```sql
INSERT INTO Users (ID, Firstname, Lastname) VALUES (1, "Petar", "Markov")
```

Update record in database
```sql
UPDATE Users SET Firstname = “Peter” WHERE User = 1;
```

Add a data field into database
```sql
ALTER TABLE Users ADD Grade varchar(1);
```

Delete user from database
```sql
DELETE FROM Users WHERE ID = 1;
```

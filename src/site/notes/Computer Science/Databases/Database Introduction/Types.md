---
{"dg-publish":true,"permalink":"/computer-science/databases/database-introduction/types/","dgHomeLink":true,"dgPassFrontmatter":false}
---

# Database Types
- ## Types:
	- ### SQL
		- Microsoft Access DB
		- MySQL
		- MariaDB (MySQL Enchanced)
		- PostgreSQL
		- CockroachDB
		- A lot more...

	- ### NoSQL (Databases that don't rely on SQL)
		- MongoDB
		- CouchDB
		- ArangoDB
		- A lot more...

- ## Types of NoSQL
	- ##### Key-Value Stores
		- This is based on a hashmap system, each document has a unique identifier, so you can select this identifier to pull the dataobject from storage.
	- ##### Document Stores
		- A document database is schema free, you don’t have to define a schema beforehand and adhere to it. It allows us to store complex data in document formats (JSON, XML etc.).
	- ##### Column Family Data stores
		- Wide column data stores take a hybrid approach mixing the declarative characteristics game of relational databases with the key-value pair based and totally variables schema of key-value stores. Wide Column databases stores data tables as sections of columns of data rather than as rows of data.
	- ##### Graph Databases
		- Graph Databases specific purpose is the storage of [graph-oriented](https://en.wikipedia.org/wiki/Graph_(data_structure) "What are Graph oriented Data Structures ?") data structures. A graph database is any storage system that provides index-free adjacency. This means that every node contains a direct pointer to its adjacent element and no index lookups are necessary. As the number of nodes increases, the cost of a hop remains the same.
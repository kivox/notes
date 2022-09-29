---
{"dg-publish":true,"permalink":"/computer-science/databases/database-introduction/validation/","dgHomeLink":true,"dgPassFrontmatter":false}
---

# Validation

- ## Types of Validation:
	- #### Primary Key
		- A primary key is **the column or columns that contain values that uniquely identify each row in a table**. A database table must have a primary key to insert, select, update, or delete data from a database table. Validation would be used to make sure the primary key is always unique.
		- ##### Checks:
			- "Is primary key unique?"
			- "Is primary key of right datatype?"
	- ##### Datatypes
		- Making sure the data inputted matches the datatype of the field
	- ##### Range check (validation rule)
		- Mainly used for age, could be used for things such as 
	- ##### Format number
		- An integer field may require input to use only characters 0 through 9.
	- ##### Field size
		- Is not longer than the allocated size to the field.
	- ##### Input mask 
		- Checks if it matches the input mask specified for a field.
	- ##### Presence check / Required Field
		- Checks that data in a field is present, e.g., customers may be required to have an email address before submitting or altering any existing information. This can also be applied on newly created rows.
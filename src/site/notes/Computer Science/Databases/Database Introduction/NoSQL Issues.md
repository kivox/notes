---
{"dg-publish":true,"permalink":"/computer-science/databases/database-introduction/no-sql-issues/","dgHomeLink":true,"dgPassFrontmatter":false}
---

# Issues with NoSQL

Now to get to the real worry at hand, why are NoSQL databases almost never a good choice, most of them don't offer relations the same way SQL offers them, these relations allow you to fetch data a lot faster. Instead of relying on multiple queries you can just use one with SQL. Some NoSQL databases have overcome this by having their own version of a query language but these databases are still often only used for storing of configuration files and data that does not require relations.

## Relations
In almost every system that requires a database, relations are needed to avoid repetition and to optimise performance aswell as ease of use.
# Report on Database Normalization

## Introduction
Normalization is a process used to organize data in a database efficiently. This involves creating tables and establishing relationships between them based on specific rules to protect data and make the database more flexible by eliminating redundancy and inconsistent dependencies.

## Why Normalize?
### Redundancy and Maintenance
Redundant data wastes disk space. For example, if a customer's address is stored in multiple places, changing that address means updating all instances. By storing the address only in the Customers table, you simplify updates and maintenance.

### Inconsistent Dependencies
An inconsistent dependency occurs when data is stored in a way that doesn’t logically align with its usage. For example, storing an employee’s salary in the Customers table creates an inconsistent dependency since salary data is related to employees, not customers. This makes the data difficult to access and manage correctly.

## Normal Forms
Normalization involves  a set of rules called "normal forms." The most common are the first three normal forms.

### First Normal Form (1NF)
- **Objective:** Eliminate repeating groups in individual tables.
- **Method:** Create a separate table for each set of related data, and identify each set with a primary key.
### Second Normal Form (2NF)
- **Objective:** Ensure that every non-primary key attribute is fully functionally dependent on the primary key.
- **Method:** Create separate tables for sets of values that apply to multiple records and relate these tables with foreign keys.
### Third Normal Form (3NF)
- **Objective:** Eliminate fields that do not depend on the primary key.
- **Method:** Ensure that no non-primary key field depends on another non-primary key field.


## Other Normal Forms
Beyond the third normal form, there are additional levels like the Boyce-Codd Normal Form (BCNF) and the fifth normal form, but these are rarely applied in practice. Ignoring these rules might not result in an ideal design but usually doesn't affect the database's functionality.

## Conclusion
Normalization is essential for efficient and logical database design. By following the first three normal forms, you can significantly reduce redundancy and inconsistent dependencies, making your database more robust and easier to maintain. However, balancing normalization with practical considerations is crucial to ensure optimal performance and usability.

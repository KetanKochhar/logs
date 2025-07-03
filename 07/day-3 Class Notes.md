##  DBMS Notes 

### What is a Database?
A **database** is an organized collection of data that can be easily accessed, managed, and updated.

### Why Do We Need a Database?
- Efficient data storage and retrieval
- Avoid data redundancy
- Maintain data integrity and consistency
- Multi-user environment support
- Security and backup options

### Types of Databases
- **Relational Database (RDBMS):** Stores data in tables (e.g., MySQL, Oracle, SQL Server)
- **NoSQL Database:** Non-relational, suitable for large-scale data (e.g., MongoDB)
- **Hierarchical Database:** Data is structured in a tree-like format
- **Network Database:** More flexible than hierarchical, allows many-to-many relationships
- **Object-oriented Database:** Stores data in the form of objects (as used in OOP)

### Applications Used to Manage Databases
- **Oracle**
- **MySQL**
- **SQL Server**
- **MongoDB**
- **SQLite**

### E-R Model (Entity-Relationship Model)
A **high-level data model** used to define the data elements and relationships for a database system.

#### Key Components:
- **Entity:** Real-world object (e.g., Student, Teacher)
- **Attributes:** Properties of an entity (e.g., Student → Name, ID)
- **Relationship:** Association between entities (e.g., Student *enrolls* in Course)

### Types of Tables
- **Base Tables:** Actual tables where data is stored
- **View Tables:** Virtual tables created from base tables

---

## 🛠️ Lab Session – Oracle APEX (SQL Practice)

### Task: Account Creation
- Created an account on the Oracle APEX website
- Faced issues with IP blocking due to multiple registrations from the same college network

### SQL Commands Practiced
- **Create Table:**
  ```sql
  CREATE TABLE table_name (
    column1 DATATYPE(SIZE),
    column2 DATATYPE(SIZE)
  );
- ```
- **Delete Table:**
```SQL
 DELETE FROM table_name;
```
- **To remove table completly**
```SQL
 DROP TABLE table_name;
```


___

## EHF Lecture – Introduction to Hacking

### What is Hacking?

The process of finding vulnerabilities in a system and exploiting them to gain unauthorized access.

### Types of Hackers

1. **White Hat Hackers:** Ethical hackers who help organizations improve security
2. **Black Hat Hackers:** Malicious hackers who break into systems for personal gain
3. **Grey Hat Hackers:** Blend of both; may break into systems without permission but not with bad intentions
4. **Script Kiddies:** Inexperienced hackers using tools/scripts created by others
5. **Hacktivists:** Hack for political or social causes
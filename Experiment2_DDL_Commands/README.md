# Experiment 2: DDL Commands

## AIM
To study and implement DDL commands and different types of constraints.

## THEORY

### 1. CREATE
Used to create a new relation (table).

**Syntax:**
```sql
CREATE TABLE (
  field_1 data_type(size),
  field_2 data_type(size),
  ...
);
```
### 2. ALTER
Used to add, modify, drop, or rename fields in an existing relation.
(a) ADD
```sql
ALTER TABLE std ADD (Address CHAR(10));
```
(b) MODIFY
```sql
ALTER TABLE relation_name MODIFY (field_1 new_data_type(size));
```
(c) DROP
```sql
ALTER TABLE relation_name DROP COLUMN field_name;
```
(d) RENAME
```sql
ALTER TABLE relation_name RENAME COLUMN old_field_name TO new_field_name;
```
### 3. DROP TABLE
Used to permanently delete the structure and data of a table.
```sql
DROP TABLE relation_name;
```
### 4. RENAME
Used to rename an existing database object.
```sql
RENAME TABLE old_relation_name TO new_relation_name;
```
### CONSTRAINTS
Constraints are used to specify rules for the data in a table. If there is any violation between the constraint and the data action, the action is aborted by the constraint. It can be specified when the table is created (using CREATE TABLE) or after it is created (using ALTER TABLE).
### 1. NOT NULL
When a column is defined as NOT NULL, it becomes mandatory to enter a value in that column.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) NOT NULL
);
```
### 2. UNIQUE
Ensures that values in a column are unique.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) UNIQUE
);
```
### 3. CHECK
Specifies a condition that each row must satisfy.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) CHECK (logical_expression)
);
```
### 4. PRIMARY KEY
Used to uniquely identify each record in a table.
Properties:
Must contain unique values.
Cannot be null.
Should contain minimal fields.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) PRIMARY KEY
);
```
### 5. FOREIGN KEY
Used to reference the primary key of another table.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size),
  FOREIGN KEY (column_name) REFERENCES other_table(column)
);
```
### 6. DEFAULT
Used to insert a default value into a column if no value is specified.

Syntax:
```sql
CREATE TABLE Table_Name (
  col_name1 data_type,
  col_name2 data_type,
  col_name3 data_type DEFAULT 'default_value'
);
```

**Question 1**

<img width="1151" height="702" alt="Screenshot 2025-10-06 at 1 27 14 PM" src="https://github.com/user-attachments/assets/5089cccc-557f-4fdf-a260-fbc29b7df2e0" />

**Output:**

<img width="1150" height="268" alt="Screenshot 2025-10-06 at 1 29 55 PM" src="https://github.com/user-attachments/assets/021dd63b-7b52-4100-9dc7-3666dfa4ba08" />


**Question 2**

<img width="1146" height="698" alt="Screenshot 2025-10-06 at 1 27 24 PM" src="https://github.com/user-attachments/assets/7c912594-f03f-430a-ac0d-f2506450314b" />

**Output:**

<img width="1149" height="246" alt="Screenshot 2025-10-06 at 1 32 17 PM" src="https://github.com/user-attachments/assets/bfd4536b-6020-4fc1-a5b7-60f3488e9c18" />

**Question 3**

<img width="1149" height="780" alt="Screenshot 2025-10-06 at 1 27 34 PM" src="https://github.com/user-attachments/assets/1b035609-eb42-4245-96d2-356f7a356035" />

**Output:**

<img width="1152" height="271" alt="Screenshot 2025-10-06 at 1 33 44 PM" src="https://github.com/user-attachments/assets/7a0fb0ed-6381-4881-9f6a-e89c7766d190" />

**Question 4**

<img width="1148" height="693" alt="Screenshot 2025-10-06 at 1 27 42 PM" src="https://github.com/user-attachments/assets/b755fe58-b4f2-4621-bd1a-7e55fb55714c" />

**Output:**

<img width="1150" height="242" alt="Screenshot 2025-10-06 at 1 37 07 PM" src="https://github.com/user-attachments/assets/c809f69e-3b9f-409d-abb3-fc7e4aa6853e" />

**Question 5**

<img width="1151" height="692" alt="Screenshot 2025-10-06 at 1 27 51 PM" src="https://github.com/user-attachments/assets/b40fb970-23ce-4467-9552-3e517d3d7def" />

**Output:**

<img width="1150" height="313" alt="Screenshot 2025-10-06 at 1 37 55 PM" src="https://github.com/user-attachments/assets/e49f1e7a-d7d0-4085-8779-37b45766643d" />

**Question 6**

<img width="1152" height="703" alt="Screenshot 2025-10-06 at 1 27 58 PM" src="https://github.com/user-attachments/assets/89360053-7cd2-4f9d-bc31-ff09cd95f13b" />

**Output:**

<img width="1151" height="270" alt="Screenshot 2025-10-06 at 1 40 26 PM" src="https://github.com/user-attachments/assets/2467781c-92e4-435b-838b-7a90a416f24c" />

**Question 7**

<img width="1155" height="722" alt="Screenshot 2025-10-06 at 1 28 05 PM" src="https://github.com/user-attachments/assets/eed0212a-33d3-4aef-b28d-b3edb946c434" />

**Output:**

![Output7](output.png)

**Question 8**

<img width="1157" height="679" alt="Screenshot 2025-10-06 at 1 28 13 PM" src="https://github.com/user-attachments/assets/fb97a3ea-8fcd-405b-84a7-77c631ce6823" />


**Output:**

![Output8](output.png)

**Question 9**

<img width="1152" height="621" alt="Screenshot 2025-10-06 at 1 28 20 PM" src="https://github.com/user-attachments/assets/02427825-69b0-466c-b2ce-ff56d89c41dd" />


**Output:**

![Output9](output.png)

**Question 10**

<img width="1151" height="655" alt="Screenshot 2025-10-06 at 1 28 26 PM" src="https://github.com/user-attachments/assets/7dd4ccd6-7690-4809-8be1-ae2ada42d8c6" />


**Output:**

![Output10](output.png)


## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.

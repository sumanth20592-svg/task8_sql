# SQL Developer Internship – Task 8  
### Stored Procedures & Functions (PostgreSQL)

## Topics Covered  
- CREATE PROCEDURE (PG ADMIN)
- CREATE FUNCTION  
- Using parameters  
- Conditional logic (IF / ELSIF / ELSE)  
- Returning values  
- Calling procedures and functions  

---

## Sample Table  
Used in this task:
employees(id, name, department, salary, city)
## Stored Procedures & Functions Implemented  

### 1. Procedure: Get Employees by Department
```sql
CREATE OR REPLACE PROCEDURE getEmployeesByDepartment(deptName TEXT)
LANGUAGE plpgsql
AS $$
BEGIN
    SELECT name, department, salary
    FROM employees
    WHERE department = deptName;
END;
$$;

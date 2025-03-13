# Case Study: Employee Attendance Management System

## Objective

Build a simple Employee Attendance System using lists and tuples in Python.

## Problem Statement

A company wants to track employee attendance using Python. The system should:

- Store employee records (ID, Name, Department).
- Mark attendance (Present/Absent) for each employee.
- Allow searching for attendance records by employee ID.
- Display a summary of attendance.

**Employee Details Tuple**

```python
(employee_id, employee_name, department)
```

**Attenance Records**

This will be a list of tuples.
```python
[(employee_id, date, status), ...]
```

### Tasks

- Create functions to mark attendance, search for attendance by id

### Sample Data

```python
attendance_records = [
    (101, "2025-03-01", "Present"),
    (102, "2025-03-01", "Absent"),
    (103, "2025-03-01", "Present"),
    (104, "2025-03-01", "Present"),
    (105, "2025-03-01", "Absent"),
]

employees = [
    (101, "Alice Johnson", "HR"),
    (102, "Bob Smith", "IT"),
    (103, "Charlie Brown", "Finance"),
    (104, "David White", "IT"),
    (105, "Eve Black", "Marketing")
]

```

### Sample Output

```
Attendance marked for Employee 101: Present
Attendance marked for Employee 102: Present
Attendance marked for Employee 103: Absent
Attendance marked for Employee 104: Present
Attendance marked for Employee 105: Present

Searching Attendance for Employee ID 102:
Date: 2025-03-01, Status: Absent
Date: 2025-03-02, Status: Present

Attendance Summary:
Alice Johnson: 100.00% Present
Bob Smith: 50.00% Present
Charlie Brown: 50.00% Present
David White: 100.00% Present
Eve Black: 50.00% Present
```


## Solution
"""
employees = [(101, "Alice Johnson", "HR"),(102, "Bob Smith", "IT"),(103, "Charlie Brown", "Finance"),(104, "David White", "IT"),(105, "Eve Black", "Marketing")]
attendance_records = [(101, "2025-03-01", "Present"),(102, "2025-03-01", "Absent"),(103, "2025-03-01", "Present"),(104, "2025-03-01", "Present"),(105, "2025-03-01", "Absent"),]

def mark_attendance(employee_id, date, status):
    attendance_records.append((employee_id, date, status))
    print(f"Attendance marked for Employee {employee_id}: {status}")

def search_attendance(employee_id):
    print(f"\nSearching Attendance for Employee ID {employee_id}:")
    found = False
    for record in attendance_records:
        if record[0] == employee_id:
            print(f"Date: {record[1]}, Status: {record[2]}")
            found = True
    if not found:
        print("No records found.")
        
mark_attendance(101, "2025-03-02", "Present")
mark_attendance(102, "2025-03-02", "Present")
mark_attendance(103, "2025-03-02", "Absent")
mark_attendance(104, "2025-03-02", "Present")
mark_attendance(105, "2025-03-02", "Present")

search_attendance(102)
"""

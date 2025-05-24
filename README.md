# Sql_Case

1/ Employee Table

CREATE TABLE Employees (
    emp_id INT PRIMARY KEY,
    name VARCHAR(50),
    department VARCHAR(20),
    salary INT,
    experience_years INT
);

INSERT INTO Employees (emp_id, name, department, salary, experience_years) VALUES
(1, 'Alice', 'HR', 50000, 2),
(2, 'Bob', 'IT', 75000, 5),
(3, 'Charlie', 'IT', 82000, 7),
(4, 'Diana', 'Finance', 67000, 3),
(5, 'Eve', 'HR', 55000, 6),
(6, 'Frank', 'IT', 47000, 1);

2/ Attendence Table

CREATE TABLE Attendance (
    emp_id INT,
    month VARCHAR(7), -- Format: YYYY-MM
    days_present INT,
    FOREIGN KEY (emp_id) REFERENCES Employees(emp_id)
);

INSERT INTO Attendance (emp_id, month, days_present) VALUES
(1, '2024-05', 20),
(2, '2024-05', 25),
(3, '2024-05', 15),
(4, '2024-05', 22),
(5, '2024-05', 18),
(6, '2024-05', 10);

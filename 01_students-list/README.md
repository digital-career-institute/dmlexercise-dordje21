# Student List

## Create a new database
Create a new database for this exercise.
```
CREATE DATABASE exercise_student_list
use exercise_student_list
```

## Create the student table
Create a table named **students** with the following columns:  
```
id (integer, primary key)  
name (varchar, maximum length 50)  
age (integer)  
grade (float)  
```

> ANSWER  
> ```
-- Create a new database
CREATE DATABASE IF NOT EXISTS exercise_student_list;
USE exercise_student_list;

-- Create the student table
CREATE TABLE IF NOT EXISTS students (
id INT PRIMARY KEY,
name VARCHAR(50),
age INT,
grade FLOAT
);
```

## Insert and Modify Data
### 1. Insert Data
Insert these records into the students table with the following data:
```
(1, 'John Doe', 20, 85.5, '123 Main St')
(2, 'Jane Smith', 22, 92.0, '456 Oak Ave')
(3, 'Bob Johnson', 21, 78.5, '789 Pine Rd')
(4, 'Tina Turner', 25, 71.0, '45 Columbia St')
```

> ANSWER  

```
-- Insert Data into students table
INSERT INTO students (id, name, age, grade)
VALUES
(1, 'John Doe', 20, 85.5),
(2, 'Jane Smith', 22, 92.0),
(3, 'Bob Johnson', 21, 78.5),
(4, 'Tina Turner', 25, 71.0);
```

### Update Data
Update the grade of 'Jane Smith' to 95.0.

> ANSWER  
```
-- Update the grade of 'Jane Smith' to 95.0
UPDATE students
SET grade = 95.0
WHERE name = 'Jane Smith';
```

### Delete Data
Delete the record of the student with id 3 from the students table.

> ANSWER  
```
-- Delete the record of the student with id 3
DELETE FROM students
WHERE id = 3;
```

### Select Data
Write a query to retrieve the names and ages of all students.  

> ANSWER  
```
-- Retrieve names and ages of all students
SELECT name, age
FROM students;
```
### Bonus: Select the best students
Write a query to retrieve the names and grade of all students with a grade higher than 80.

> ANSWER  
```
-- Retrieve names and grades of students with a grade higher than 80
SELECT name, grade
FROM students
WHERE grade > 80;
```

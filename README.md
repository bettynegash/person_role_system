# person_role_system
Student Record Management System

Project Description

The Student Record Management System is a Java Object-Oriented Programming (OOP) application that manages student records using Java File I/O and Streams.

The system allows users to add, search, update, delete, and display student information. It also generates reports and stores data using text files, binary files, and object serialization.

---

Features

- Add Student
- Search Student by ID
- Update Student Information
- Delete Student
- Display All Students
- Generate Report
- Save Data to Text File
- Save Data to Binary File
- Save Data using Object Serialization
- Display File Information
- Create Backup using Buffered Streams
- Exception Handling

---

Classes Used

1. Student.java

Stores student information:

- Student ID
- Name
- Department
- GPA

2. StudentManagement.java

Manages student operations:

- Add Student
- Search Student
- Update Student
- Delete Student
- Display Students
- Generate Report

3. FileManager.java

Handles file operations:

- Text Files (PrintWriter)
- Binary Files (DataOutputStream)
- Object Serialization (ObjectOutputStream)
- File Information (File class)
- Backup using Buffered Streams

4. Main.java

Contains the main method and menu-driven user interface.

---

File I/O Used

Text Files

- PrintWriter

Binary Files

- DataOutputStream

Object Serialization

- ObjectOutputStream

Buffered Streams

- BufferedInputStream
- BufferedOutputStream

File Class

Used to display:

- File name
- File path
- File size

---

Report Generated

The system generates:

- Total Students
- Highest GPA
- Lowest GPA
- Average GPA

---

Exception Handling

Try-catch blocks are used to handle exceptions that may occur during file operations.

---

Project Structure

StudentRecordManagementSystem
│
├── Student.java
├── StudentManagement.java
├── FileManager.java
├── Main.java
│
├── students.txt
├── students.dat
├── students.obj
└── students_backup.obj

---

Concepts Used

- Classes and Objects
- Encapsulation
- ArrayList
- File I/O
- Scanner
- PrintWriter
- DataInputStream and DataOutputStream
- ObjectInputStream and ObjectOutputStream
- Buffered Streams
- Exception Handling

---

Author

Student Name: __________________

Course: Object-Oriented Programming (Java)

Language Used: Java

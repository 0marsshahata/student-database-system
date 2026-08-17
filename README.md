# Student Database Management System

A lightweight embedded systems student database application built in C, designed to efficiently manage student records with CRUD operations.

## Project Overview

**Student Database Management System** (SDMS) is a command-line database management system implemented in C for the Embedded Systems Diploma. It provides a simple yet effective way to store, retrieve, and manage student information including academic records.

## Features

- ✅ **Add Student Entry** - Insert new student records with complete academic information
- ✅ **Read Student Data** - Retrieve individual student records by ID
- ✅ **Delete Student Entry** - Remove student records from the database
- ✅ **Check ID Existence** - Verify if a student ID exists in the database
- ✅ **Get Database Size** - Display the number of active records
- ✅ **List All Student IDs** - View all registered student IDs
- ✅ **Database Full Status** - Check if the database has reached capacity

## Student Record Structure

Each student record contains:
- **Student ID** - Unique identifier
- **Student Year** - Academic year
- **Course 1** - Course ID and Grade
- **Course 2** - Course ID and Grade  
- **Course 3** - Course ID and Grade

## Database Specifications

- **Maximum Capacity**: 10 student records
- **Storage Method**: In-memory array
- **Data Types**: Unsigned 32-bit integers for student/course data

## Project Structure

```
.
├── main.c              # Application entry point
├── SDBAPP.c           # User interface and menu system
├── SDBAPP.h           # Application function declarations
├── SDB.c              # Database implementation (core logic)
├── SDB.h              # Database API definitions
├── STD.h              # Standard type definitions
├── doxygen/           # Documentation configuration
└── program c project.cbp  # Code::Blocks project file
```

## Building the Project

### Prerequisites
- GCC compiler
- Code::Blocks IDE (optional)

### Compilation

```bash
gcc -o sdms main.c SDB.c SDBAPP.c -Wall -Wextra
```

### Running

```bash
./sdms
```

## Usage

The application provides an interactive menu:

```
To add entry, enter 1
To get used size in database, enter 2
To read student data, enter 3
To get the list of all student IDs, enter 4
To check if ID is existed, enter 5
To delete student data, enter 6
To check if database is full, enter 7
To exit enter 0
```

### Example Session

```
Enter choice: 1
Enter student ID, year, course1 ID, course1 grade, course2 ID, course2 grade, course3 ID, course3 grade:
101 2023 301 85 302 90 303 88
Entry added successfully.
```

## Technical Details

### Data Structure

```c
typedef struct SimpleDb {
    uint32 Student_ID;
    uint32 Student_year;
    uint32 Course1_ID;
    uint32 Course1_grade;
    uint32 Course2_ID;
    uint32 Course2_grade;
    uint32 Course3_ID;
    uint32 Course3_grade;
} SimpleDb;
```

### Core Functions

| Function | Purpose |
|----------|---------|
| `SDB_AddEntry()` | Add a new student record |
| `SDB_ReadEntry()` | Retrieve student data by ID |
| `SDB_DeleteEntry()` | Delete student record |
| `SDB_IsIdExist()` | Check if ID exists |
| `SDB_IsFull()` | Check database capacity |
| `SDB_GetUsedSize()` | Get current record count |
| `SDB_GetList()` | Retrieve all student IDs |

## Education Context

This project was developed as part of an **Embedded Systems Diploma** curriculum, demonstrating:
- C programming fundamentals
- Data structure implementation
- Menu-driven application design
- Array-based database management
- Type definition and abstractions

## Author

**Omar Shreif Shahata**  
Student ID: 1231070  
Mechatronics Engineering - Dual Degree Program  
Delta University & University of Plymouth

---

**Status**: Graduation Project ✓  
**Created**: 2024  
**License**: Educational Use

# c-oop-project-test
# Hospital Management System — Project Report

## 1. Project Title

**Hospital Management System using Object-Oriented Programming in C++**

---

# 2. Introduction

The Hospital Management System is a console-based application developed in C++ using Object-Oriented Programming (OOP) concepts. The purpose of this project is to manage patient and doctor information efficiently within a hospital environment.

This project demonstrates the implementation of major OOP concepts such as:

* Classes and Objects
* Inheritance
* Polymorphism
* Encapsulation
* Constructors and Destructors
* Friend Functions
* Static Members
* Structures
* Dynamic Memory Allocation
* Singleton Design Pattern

The system allows users to:

* Add patient records
* Display patient details
* Store doctor information
* Count total patients
* Simulate a centralized hospital database connection

---

# 3. Objectives

The main objectives of this project are:

1. To understand Object-Oriented Programming concepts in C++.
2. To design a simple hospital management system.
3. To implement dynamic memory allocation.
4. To practice inheritance and polymorphism.
5. To create a menu-driven application for user interaction.
6. To simulate centralized database access using the Singleton pattern.

---

# 4. Tools and Technologies Used

| Component            | Technology                             |
| -------------------- | -------------------------------------- |
| Programming Language | C++                                    |
| IDE                  | Visual Studio / Dev-C++ / CodeBlocks   |
| Concepts Used        | OOP, Dynamic Memory, Singleton Pattern |
| Platform             | Console Application                    |

---

# 5. System Features

The project provides the following features:

* Add new patients
* Display all patient records
* Store and display doctor information
* Show total number of patients
* Centralized database connection simulation
* Menu-driven user interface

---

# 6. OOP Concepts Implemented

## 6.1 Classes and Objects

Classes used in the project:

* `Person`
* `Patient`
* `Doctor`
* `Hospital`
* `Admin`
* `Counter`
* `CentralDatabase`

Objects are created from these classes to perform operations.

Example:

```cpp
Hospital h(5);
Admin admin;
Doctor d;
```

---

## 6.2 Inheritance

The `Patient` and `Doctor` classes inherit from the base class `Person`.

```cpp
class Patient : public Person
class Doctor : public Person
```

This promotes code reuse.

---

## 6.3 Polymorphism

Function overriding is used through the `display()` function.

```cpp
void display() override
```

Both `Patient` and `Doctor` provide their own implementation.

---

## 6.4 Encapsulation

Data members are declared private/protected and accessed through member functions.

Example:

```cpp
private:
    int id;
```

---

## 6.5 Constructors and Destructors

Constructors initialize objects while destructors clean memory.

Example:

```cpp
Patient(string n, int a, int i, string city, string street)
```

Destructor:

```cpp
~Patient()
```

---

## 6.6 Static Members

Static variable tracks total patients.

```cpp
static int totalPatients;
```

---

## 6.7 Friend Function

A friend function accesses private data of the `Patient` class.

```cpp
friend void showPatient(Patient p);
```

---

## 6.8 Dynamic Memory Allocation

Dynamic arrays are used to store patients.

```cpp
patients = new Patient[size];
```

Memory is released using:

```cpp
delete[] patients;
```

---

## 6.9 Singleton Design Pattern

The `CentralDatabase` class follows the Singleton Pattern to ensure only one database instance exists.

```cpp
static CentralDatabase* getInstance()
```

---

# 7. System Design

## 7.1 Class Diagram (Text Representation)

```text
                Person
               /      \
          Patient    Doctor

Hospital ---> stores Patient objects
Admin ---> accesses total patients
Counter ---> static patient count
CentralDatabase ---> singleton database
```

---

# 8. Explanation of Classes

---

## 8.1 CentralDatabase Class

### Purpose

Simulates a centralized hospital database.

### Key Features

* Singleton pattern
* Single shared instance

### Important Function

```cpp
getInstance()
```

---

## 8.2 Address Structure

### Purpose

Stores patient address information.

### Data Members

```cpp
string city;
string street;
```

---

## 8.3 Person Class

### Purpose

Base class for `Patient` and `Doctor`.

### Data Members

* Name
* Age

### Functions

* `display()`

---

## 8.4 Patient Class

### Purpose

Stores patient information.

### Additional Data

* Patient ID
* Address

### Functions

* Constructor
* Overridden `display()`
* Destructor

---

## 8.5 Doctor Class

### Purpose

Stores doctor information.

### Additional Data

* Specialization

### Functions

* Overridden `display()`

---

## 8.6 Hospital Class

### Purpose

Manages patient records.

### Main Functions

* `addPatient()`
* `showAll()`

### Special Features

* Dynamic memory allocation

---

## 8.7 Admin Class

### Purpose

Displays total patients.

### Function

```cpp
showTotal()
```

---

# 9. Program Flow

1. Program starts.
2. Singleton database connects.
3. User sees menu.
4. User selects options:

   * Add patient
   * Display patients
   * Show doctor info
   * Show total patients
5. Program exits.

---

# 10. Menu System

```text
===== HOSPITAL MANAGEMENT MENU =====
1. Add Patient
2. Show All Patients
3. Show Doctor Info
4. Show Total Patients
5. Exit
```

---

# 11. Sample Output

## Adding Patient

```text
Enter Patient Name: Ali
Enter Age: 22
Enter ID: 101
Enter City: Lahore
Enter Street: ModelTown
Patient Added Successfully!
```

---

## Display Patients

```text
Patient ID: 101
Name: Ali, Age: 22
Address: Lahore, ModelTown
```

---

## Doctor Information

```text
Name: Ahmed, Age: 40
Specialization: Cardiology
```

---

# 12. Advantages of the System

* Easy to understand
* Demonstrates complete OOP concepts
* Efficient patient handling
* Dynamic memory management
* Menu-driven interface
* Reusable code structure

---

# 13. Limitations

* Data is not stored permanently
* No file handling/database
* Limited validation
* Console-based interface only
* Fixed hospital size

---

# 14. Future Enhancements

The following improvements can be added:

1. File handling for permanent storage
2. Graphical User Interface (GUI)
3. Database integration (MySQL)
4. Search patient functionality
5. Delete/update patient records
6. Appointment management
7. Billing system
8. Login authentication

---

# 15. Conclusion

The Hospital Management System successfully demonstrates the implementation of important Object-Oriented Programming concepts in C++. The project provides a simple but effective way to manage hospital data using classes, inheritance, polymorphism, and dynamic memory allocation.

This project is highly useful for students learning OOP because it combines multiple concepts into one practical application.

---

# 16. Complete List of Concepts Used

| Concept             | Used |
| ------------------- | ---- |
| Classes & Objects   | Yes  |
| Inheritance         | Yes  |
| Polymorphism        | Yes  |
| Encapsulation       | Yes  |
| Constructor         | Yes  |
| Destructor          | Yes  |
| Friend Function     | Yes  |
| Static Variable     | Yes  |
| Dynamic Memory      | Yes  |
| Singleton Pattern   | Yes  |
| Structures          | Yes  |
| Menu-driven Program | Yes  |

---

# 17. References

1. Bjarne Stroustrup — *The C++ Programming Language*
2. Object-Oriented Programming Notes
3. C++ Documentation
4. Visual Studio C++ Compiler Documentation

# Day 3 - Salesforce Data Modeling

# Difference Between App, Object, Record, and Field

| Component | Description | Example |
|-----------|-------------|---------|
| App | Collection of related tabs, objects, and features | Sales App |
| Object | Database table used to store data | Student Object |
| Record | Single row of data inside an object | Student: Ravi Kumar |
| Field | Individual data attribute in a record | Name, Email, Phone |

---

# Explanation with Example

## App
An App is a group of related functionalities used for a business purpose.

### Example:
Student Management App

It may include:
- Students
- Courses
- Faculty
- Reports

---

## Object
An Object stores related data in Salesforce.

### Example:
Student Object

Stores:
- Student Name
- Roll Number
- Email

---

## Record
A Record is a single entry inside an object.

### Example:

| Student Name | Roll Number | Email |
|--------------|-------------|-------|
| Ravi Kumar | 101 | ravi@gmail.com |

This row is called a record.

---

## Field
A Field stores a specific piece of information.

### Example Fields:
- Student Name
- Phone Number
- Course Name

---

# Standard vs Custom Objects

| Standard Objects | Custom Objects |
|------------------|----------------|
| Already provided by Salesforce | Created by users |
| Used for common CRM processes | Used for business-specific needs |
| Cannot be deleted | Can be customized fully |
| Example: Account, Contact | Example: Student__c |

---

## Examples

### Standard Objects
- Account
- Contact
- Opportunity
- Lead

### Custom Objects
- Student
- Faculty
- Course
- Attendance

---

# My College Data Model

## Application Name:
College Management System

---

# Objects Used

## 1. Student Object
Stores:
- Student Name
- Roll Number
- Email
- Phone Number

---

## 2. Course Object
Stores:
- Course Name
- Course Code
- Duration

---

## 3. Faculty Object
Stores:
- Faculty Name
- Subject
- Email

---

## 4. Attendance Object
Stores:
- Attendance Date
- Status
- Student Reference

---

# Relationships

| Parent Object | Child Object | Relationship |
|---------------|--------------|--------------|
| Course | Student | One-to-Many |
| Faculty | Course | One-to-Many |
| Student | Attendance | One-to-Many |

---

# Data Model Diagram

```text
Faculty
   |
   | One Faculty teaches many Courses
   ↓
Course
   |
   | One Course has many Students
   ↓
Student
   |
   | One Student has many Attendance Records
   ↓
Attendance
```

---

# Diagram/Image Section

(Add your Salesforce schema builder screenshot or draw.io diagram here)

Example:

![College Data Model](screenshots/college-data-model.png)

---

# Formula Fields

Formula Fields automatically calculate values based on other fields.

---

## Example 1: Student Age Calculation

### Formula:
```text
TODAY() - Date_of_Birth__c
```

### Explanation:
Calculates the student's age automatically using Date of Birth.

---

## Example 2: Attendance Percentage

### Formula:
```text
(Classes_Attended__c / Total_Classes__c) * 100
```

### Explanation:
Calculates student attendance percentage automatically.

---

# Validation Rules

Validation Rules ensure data accuracy before saving records.

---

## Example 1: Phone Number Validation

### Rule:
Phone number must contain exactly 10 digits.

### Formula:
```text
LEN(Phone__c) <> 10
```

### Explanation:
Prevents saving invalid phone numbers.

---

## Example 2: Email Validation

### Rule:
Email must contain "@"

### Formula:
```text
NOT(CONTAINS(Email__c, "@"))
```

### Explanation:
Ensures proper email format.

---

# Reflection: Why Structured Enterprise Data Matters

Structured enterprise data is very important because it helps organizations:
- Store information properly
- Reduce duplicate records
- Improve reporting and analytics
- Increase productivity
- Maintain accurate business operations

In Salesforce, structured data helps:
- Faster decision making
- Better customer management
- Easier automation
- Improved security
- Better scalability

Without proper data modeling, businesses can face:
- Data inconsistency
- Poor reporting
- Difficult maintenance
- System confusion

A well-designed data model improves both business efficiency and user experience.

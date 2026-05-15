# Day 2 - Salesforce Platform Basics

## What is Salesforce Platform?

Salesforce Platform is a cloud-based application development platform that allows businesses to build, customize, and manage applications without managing servers or infrastructure.

It provides tools and services for:
- CRM (Customer Relationship Management)
- Data management
- Automation
- Security
- Reporting
- Custom application development

Salesforce Platform helps developers and businesses quickly create scalable and secure applications.

---

# Explain Important Salesforce Components

## 1. App

An App in Salesforce is a collection of tabs, objects, and features grouped together for specific business purposes.

Apps help users easily access related functionalities.

### Example:
- Sales App
- Service App
- Marketing App

A Sales App may include:
- Accounts
- Contacts
- Opportunities
- Reports
- Dashboards

---

## 2. Object

An Object in Salesforce is similar to a database table that stores data.

Objects contain:
- Records (rows)
- Fields (columns)

### Types of Objects:
- Standard Objects
- Custom Objects

### Standard Object Examples:
- Account
- Contact
- Opportunity

### Custom Object Example:
- Property
- Student
- Employee

---

## 3. Tab

A Tab is a user interface element used to access objects, records, dashboards, reports, or web pages.

Tabs make navigation easy for users.

### Example:
- Accounts Tab
- Contacts Tab
- Opportunities Tab

When a user clicks a tab, Salesforce opens related records and pages.

---

# Difference Between Configuration and Coding

| Configuration | Coding |
|---------------|--------|
| Done using clicks, drag-and-drop, and setup tools | Done using programming languages |
| Requires less technical knowledge | Requires development skills |
| Faster to implement | More flexible and powerful |
| Uses Flow, Process Builder, Validation Rules | Uses Apex, LWC, Visualforce |
| Best for simple automation | Best for complex business logic |

### Example:
- Creating a validation rule = Configuration
- Writing Apex Trigger = Coding

---

# My System Design

## Application Name:
Student Management System

---

## App

### Student Management App

This app is used by a college to manage students, courses, and faculty information.

---

## Objects

### 1. Student Object
Stores:
- Student Name
- Roll Number
- Email
- Phone Number

### 2. Course Object
Stores:
- Course Name
- Course Code
- Duration

### 3. Faculty Object
Stores:
- Faculty Name
- Subject
- Contact Details

---

## User Interaction Flow

1. Admin logs into Salesforce.
2. Admin opens the Student Management App.
3. Admin creates student records.
4. Faculty members view assigned students and courses.
5. Students are linked to courses using relationships.
6. Reports are generated to track student performance.

---

# Real-World Usage

This system can help:
- Colleges
- Schools
- Training institutes

Benefits:
- Easy data management
- Centralized information
- Faster communication
- Better reporting

---

# Conclusion

In this task, I learned:
- Basics of Salesforce Platform
- Difference between App, Object, and Tab
- Difference between Configuration and Coding
- How Salesforce applications are designed

This helped me understand the foundation of Salesforce application development.

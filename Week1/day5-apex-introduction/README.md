# Day 5 - Introduction to Apex

# What is Apex?

Apex is a strongly typed, object-oriented programming language developed by Salesforce.

It is used to add custom business logic and backend functionality to Salesforce applications.

Apex runs on the Salesforce platform and is similar to Java in syntax.

Developers use Apex to:
- Automate complex processes
- Write custom validations
- Integrate external systems
- Create REST APIs
- Handle advanced business logic

Apex is mainly used when Salesforce configuration tools are not enough to meet business requirements.

---

# Difference Between Flow and Apex

| Flow | Apex |
|------|------|
| Low-code automation tool | Full programming language |
| Drag-and-drop interface | Code-based development |
| Easy for admins | Used mainly by developers |
| Best for simple automation | Best for complex logic |
| Faster to build | More flexible and scalable |
| Limited advanced customization | Supports advanced customization |

---

# Difference Between Configuration and Coding

| Configuration | Coding |
|---------------|--------|
| No-code or low-code approach | Requires programming |
| Uses clicks and setup tools | Uses Apex, LWC, APIs |
| Easier to maintain | More powerful and flexible |
| Best for standard requirements | Best for complex requirements |
| Faster implementation | More development effort |

---

# Real Examples Where Apex Is Needed

## 1. Complex Student Fee Calculation

If fee calculation depends on:
- Scholarships
- Attendance
- Discounts
- Department rules

then simple Flow may not be enough.

Apex can handle complex calculations efficiently.

---

## 2. Integration with External University Portal

If Salesforce needs to:
- Send student data to another system
- Receive attendance from external software

Apex APIs and callouts are required.

---

## 3. Bulk Student Record Processing

Suppose thousands of student records need processing daily.

Apex Batch Jobs can:
- Process large data efficiently
- Reduce performance issues
- Automate background tasks

---

# Integrated System Design

# College Management System

This project is designed using Salesforce CRM concepts and automation tools.

---

# CRM Usage

The system helps manage:
- Student information
- Courses
- Faculty details
- Attendance
- Fee tracking

Salesforce CRM centralizes all college data in one platform.

---

# Objects Used

## Standard Objects
- Account
- Contact

---

## Custom Objects

### Student__c
Stores:
- Name
- Roll Number
- Email
- Attendance

---

### Course__c
Stores:
- Course Name
- Course Code
- Duration

---

### Faculty__c
Stores:
- Faculty Name
- Subject
- Email

---

### Attendance__c
Stores:
- Attendance Status
- Date
- Student Reference

---

# Relationships

| Parent Object | Child Object | Relationship |
|---------------|--------------|--------------|
| Course__c | Student__c | One-to-Many |
| Faculty__c | Course__c | One-to-Many |
| Student__c | Attendance__c | One-to-Many |

---

# Validation Rules

## Example 1
Phone number must contain exactly 10 digits.

### Validation Formula
```text
LEN(Phone__c) <> 10
```

---

## Example 2
Attendance cannot exceed 100%.

### Validation Formula
```text
Attendance_Percentage__c > 100
```

---

# Flow Automation

## Student Registration Flow
When a new student is added:
- Create student record
- Send welcome email
- Assign faculty advisor automatically

---

## Attendance Alert Flow
If attendance drops below 75%:
- Send warning notification to student

---

# Apex Usage

Apex is used for:
- Advanced attendance calculation
- External portal integration
- Batch processing student records
- Complex fee calculations

---

# Pseudocode Examples

## Example 1: Attendance Warning Logic

```text
IF attendance_percentage < 75
    SEND warning_email
END IF
```

---

## Example 2: Fee Discount Logic

```text
IF student_marks > 90
    APPLY scholarship_discount
ELSE
    APPLY normal_fee
END IF
```

---

## Example 3: Auto Course Assignment

```text
IF department = "Computer Science"
    ASSIGN CS courses
ELSE
    ASSIGN General courses
END IF
```

---

# Reflection: Why Enterprise Systems Eventually Need Programming

Enterprise systems become more complex as organizations grow.

Initially, configuration tools and automation can handle simple business processes. However, advanced requirements eventually need programming.

Programming is important because:
- Businesses need custom workflows
- Systems require integrations
- Large data volumes need optimization
- Advanced security and validations are required
- Complex calculations cannot always be handled by low-code tools

Apex gives developers the flexibility to build scalable and enterprise-grade solutions on Salesforce.

I learned that:
- Configuration is good for simple solutions
- Apex is necessary for advanced enterprise applications
- Real-world systems usually combine both low-code and coding approaches

---

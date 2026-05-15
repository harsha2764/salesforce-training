# Day 4 - Flow Builder

## What is Flow Builder?

Flow Builder is a Salesforce automation tool used to automate business processes without writing code.

It allows users and admins to create workflows using a drag-and-drop interface. Flow Builder helps reduce manual work, improve accuracy, and save time.

Using Flow Builder, we can:
- Create records automatically
- Update records
- Send emails or notifications
- Collect user input
- Build guided screens
- Automate approvals and tasks

Flow Builder is one of the most powerful low-code tools in Salesforce.

---

# Types of Flows

## 1. Screen Flow

A Screen Flow is an interactive flow that shows screens to users and collects input.

It is mainly used for:
- Forms
- Step-by-step wizards
- Data entry processes
- Guided user interactions

### Example:
A student registration form where users enter:
- Name
- Email
- Course

After submission, Salesforce creates a student record automatically.

---

## 2. Record-Triggered Flow

A Record-Triggered Flow runs automatically when a record is:
- Created
- Updated
- Deleted

It works in the background without user interaction.

### Example:
When a new student record is created:
- Send a welcome email automatically
- Assign the student to a course advisor

This type of flow is commonly used for automation.

---

# My Automation Ideas

## 1. Student Welcome Email Automation

When a new student record is created, Salesforce automatically sends a welcome email.

### Benefits:
- Saves manual effort
- Improves communication

---

## 2. Attendance Warning Notification

If attendance percentage falls below 75%, the system automatically sends a warning notification.

### Benefits:
- Helps students improve attendance
- Easy monitoring

---

## 3. Automatic Course Assignment

When a student selects a department, related courses are assigned automatically.

### Benefits:
- Faster process
- Reduces errors

---

## 4. Fee Payment Reminder

Before the due date, automated reminder emails are sent to students.

### Benefits:
- Improves payment tracking
- Reduces missed payments

---

## 5. Faculty Approval Process

When a student submits a project request, the system automatically sends it to faculty for approval.

### Benefits:
- Faster approvals
- Better workflow management

---

# My Flow Diagram

## Student Registration Automation Flow

```text
User Opens Form
       ↓
Enter Student Details
       ↓
Submit Screen Flow
       ↓
Create Student Record
       ↓
Send Welcome Email
       ↓
Assign Academic Advisor
```

# Manual vs Automated Process

| Manual Process | Automated Process |
|----------------|------------------|
| Requires human effort | Runs automatically |
| Takes more time | Saves time |
| Higher chance of mistakes | Reduces errors |
| Repetitive tasks | Smart workflow execution |
| Difficult to track | Easy monitoring and reporting |

---

# Example Comparison

## Manual Process
Admin manually:
- Creates records
- Sends emails
- Tracks approvals

This process is slow and repetitive.

---

## Automated Process
Flow Builder automatically:
- Creates records
- Sends notifications
- Updates data
- Assigns tasks

This makes the system faster and more efficient.

---

# Reflection: Why Automation Matters in Enterprise Systems

Automation is very important in enterprise systems because organizations handle large amounts of data and repetitive tasks daily.

Without automation:
- Processes become slow
- Human errors increase
- Productivity decreases

Automation helps businesses:
- Save time
- Improve accuracy
- Increase efficiency
- Standardize processes
- Improve customer experience

In Salesforce, Flow Builder allows companies to automate business operations without heavy coding, which makes development faster and easier.

I learned that automation is not just about saving time — it also improves reliability, scalability, and overall business performance.


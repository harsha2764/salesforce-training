# Day 6 - Triggers and SOQL

# What is SOQL?

SOQL stands for Salesforce Object Query Language.

It is used to retrieve data from Salesforce objects, similar to how SQL is used in databases.

Using SOQL, developers can:
- Fetch records
- Filter data
- Sort results
- Access related objects
- Retrieve specific fields

SOQL works only with Salesforce data and objects.

---

# Example of SOQL

```sql
SELECT Name, Email__c FROM Student__c
```

This query retrieves:
- Student Name
- Student Email

from the Student object.

---

# What is an Apex Trigger?

An Apex Trigger is a piece of Apex code that executes automatically when data changes happen in Salesforce.

Triggers run when records are:
- Inserted
- Updated
- Deleted
- Undeleted

Triggers help automate backend logic based on record changes.

---

# Example

When a new student record is created:
- Automatically assign a faculty advisor
- Send notification email
- Create attendance record

This automation can be handled using triggers.

---

# Difference Between Flow and Trigger

| Flow | Apex Trigger |
|------|---------------|
| Low-code automation tool | Code-based automation |
| Easier for admins | Used by developers |
| Drag-and-drop interface | Written in Apex language |
| Best for simple processes | Best for complex logic |
| Faster to develop | More flexible and scalable |
| Limited advanced control | Full programming control |

---

# Difference Between Before and After Trigger

| Before Trigger | After Trigger |
|----------------|---------------|
| Runs before data is saved | Runs after data is saved |
| Used for validation and updating fields | Used for related record creation |
| Faster because no extra database save needed | Used when record ID is required |
| Can modify record values directly | Cannot modify same record directly |

---

# Example

## Before Trigger Example
Automatically set:
- Default student status
before saving the record.

---

## After Trigger Example
After student creation:
- Create attendance record
- Send email notification

---

# My Trigger Use Cases

## 1. Automatic Welcome Email

When a new student joins:
- Send welcome email automatically.

---

## 2. Attendance Alert Trigger

If attendance drops below 75%:
- Send warning notification.

---

## 3. Auto Faculty Assignment

When a course is selected:
- Assign related faculty automatically.

---

## 4. Prevent Duplicate Student Records

Before saving:
- Check if Roll Number already exists.

---

## 5. Fee Status Update

After payment:
- Automatically update fee status as "Paid".

---

# Query Examples (English Ideas)

## Example 1
Get all students whose attendance is below 75%.

---

## Example 2
Find students enrolled in Computer Science course.

---

## Example 3
Retrieve all faculty members teaching Java subject.

---

## Example 4
Get students who have pending fee payments.

---

## Example 5
Find all attendance records created this month.

---

# Sample SOQL Queries

## Query 1

```sql
SELECT Name, Attendance_Percentage__c
FROM Student__c
WHERE Attendance_Percentage__c < 75
```

---

## Query 2

```sql
SELECT Name, Course__c
FROM Student__c
WHERE Course__c = 'Computer Science'
```

---

## Query 3

```sql
SELECT Name
FROM Faculty__c
WHERE Subject__c = 'Java'
```

---

# Reflection: Why Enterprise Systems React Automatically to Data Changes

Enterprise systems manage large amounts of real-time data.

Whenever data changes:
- Business processes must react immediately
- Notifications should be sent
- Records should stay synchronized
- Rules should be enforced automatically

Without automation:
- Manual work increases
- Errors become common
- Processes slow down

Triggers and automation help systems:
- Maintain data consistency
- Improve efficiency
- Reduce repetitive work
- Support real-time business operations

In Salesforce, triggers allow applications to respond instantly whenever records are created, updated, or deleted.

I learned that modern enterprise systems are event-driven, meaning the system automatically reacts whenever important business data changes.


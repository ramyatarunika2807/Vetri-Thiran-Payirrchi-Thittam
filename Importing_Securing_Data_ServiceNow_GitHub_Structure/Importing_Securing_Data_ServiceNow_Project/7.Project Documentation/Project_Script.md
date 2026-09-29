# Importing & Securing Data in ServiceNow

## Problem Statement
Linking each record to an employee and pulling some employee details (like department) into the record for easier reporting.

## Objective
The objective is to implement an Access Control List by using Impersonate user. This provides a foundation for managing and securing data in ServiceNow using key platform features.

## Milestone 1: Tables
### Activity 1: Create Table
1. Open ServiceNow.
2. Click on All and search for Tables.
3. Select Tables under System Definition.
4. Click New.
5. Fill in the details to create a new table.
6. Add:
   - Training Name (String)
   - Completion Date (Date)
   - Status (Choice)
   - Employee (Reference to `sys_user`)
7. Click Submit.
8. Click the Status field to add choices in the Dictionary Entry.

## Milestone 2: Import Data
### Activity 1: Importing Data
1. Create an `.xlsx` file with Training Name, Completion Date, Status and Employee.
2. Open ServiceNow.
3. Go to All → System Import Sets.
4. Select Load Data and upload the file.
5. Label: Employee Training.
6. Name: `u_employee_training`.
7. Click Submit.

### Activity 2: Map Fields
1. Open ServiceNow.
2. Go to All → System Import Sets → Administration → Transform Maps.
3. Fill in the details to create a Transform Map.
4. Click Submit.
5. Add Field Maps.
6. Under Related Links, click Transform to run the import.

## Milestone 3: Dot-Walking
1. Open ServiceNow.
2. Go to All → Employee Training Records → Employee Training Records.
3. Open the form using New.
4. Open Additional Actions and select Configure and Form Layout.
5. Click Employee [+], dot-walk, select Department and move it to the right.
6. Save.
7. The field can now be seen in the List view.

## Milestone 4: Roles and User Creation
### Create User
Go to All → User Administration → Users and create a new user named `backup user`.

### Create Role
Go to All → User Administration → Roles and create a new role named `HR Manager`.

### Assign Role to User
Open the backup user and, under Roles, click Edit and add the HR Manager role.

### Add Roles to Applications Menu and Modules
Go to Employee Training Records and add the required role to the application menu and module.

## Milestone 5: ACL
### Update Role
1. Go to Profile → Elevate Role.
2. Check `security_admin` and update.

### ACL Creation
1. Create a new ACL and give Read access to the Employee Training Records table.
2. Give the HR Manager role to the ACL.
3. Create another ACL and repeat the process for Write access.

## Milestone 6: Result
### Testing Result
1. Impersonate the `sys_user` and search Employee Training Records.
2. Verify that the fields can be seen and edited.
3. Impersonate another user and verify that the table cannot be seen.

## Conclusion
This project demonstrated importing data into ServiceNow using Import Sets, using dot-walking to access related table data, and applying Access Control Rules (ACLs) for data security. These functions support data integration, table relationships and role-based access control.

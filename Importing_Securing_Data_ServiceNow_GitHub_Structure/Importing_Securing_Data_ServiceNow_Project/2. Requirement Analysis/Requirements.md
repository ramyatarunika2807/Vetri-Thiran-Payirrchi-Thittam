# Requirement Analysis

## Objective
Implement an Access Control List by using impersonate user functionality to manage and secure data in ServiceNow.

## Required Data Fields
- Training Name — String
- Completion Date — Date
- Status — Choice
- Employee — Reference field to `sys_user`

## Main Functional Requirements
1. Create the Employee Training table.
2. Import employee training data using Import Sets.
3. Map imported fields using Transform Maps.
4. Use dot-walking to access Employee Department information.
5. Create users and roles.
6. Assign the HR Manager role to the backup user.
7. Add roles to the application menu and modules.
8. Create Read and Write ACLs.
9. Test access using impersonation.

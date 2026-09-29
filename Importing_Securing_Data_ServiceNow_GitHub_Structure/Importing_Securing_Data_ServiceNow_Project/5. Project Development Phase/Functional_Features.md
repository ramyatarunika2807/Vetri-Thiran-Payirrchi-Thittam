# Project Development Phase

## 1. Create Employee Training Table
Create the table and add:
- Training Name
- Completion Date
- Status
- Employee

## 2. Import Data
Create an `.xlsx` spreadsheet with the four fields and load it through:
**All → System Import Sets → Load Data**

Label:
`Employee Training`

Name:
`u_employee_training`

## 3. Map Fields
Create a Transform Map and add the required Field Maps. Run the transform using the Transform related link.

## 4. Dot-Walking
Open Employee Training Records, configure the form layout, select:
**Employee [+] → Department**

Save the layout so the department can be displayed.

## 5. Roles and Users
Create:
- Backup user
- HR Manager role

Assign the HR Manager role to the backup user.

## 6. Application Menu and Module
Add the required roles to the Employee Training Records application menu and module.

## 7. ACL Security
Elevate the role using `security_admin`, then:
- Create a Read ACL for Employee Training Records.
- Give the HR Manager role to the ACL.
- Create a Write ACL using the same process.

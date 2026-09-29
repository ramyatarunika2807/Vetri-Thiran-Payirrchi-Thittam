# Project Design Phase

## Table Design
**Table:** Employee Training

| Field | Type | Purpose |
|---|---|---|
| Training Name | String | Stores the training name |
| Completion Date | Date | Stores completion date |
| Status | Choice | Stores training status |
| Employee | Reference | References the `sys_user` table |

## Relationship / Dot-Walking Design
Employee is a reference field to `sys_user`. Dot-walking is used to access the employee's Department information and display it in the Employee Training record/list view.

## Security Design
- User: backup user
- Role: HR Manager
- ACL: Read access
- ACL: Write access

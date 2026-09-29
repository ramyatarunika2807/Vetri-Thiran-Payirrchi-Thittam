# Project Testing

## Testing Procedure

### Test 1 — Authorized User
1. Impersonate the `sys_user`.
2. Search for Employee Training Records.
3. Verify that the user can see and edit the fields.

### Test 2 — Other User
1. Impersonate another user.
2. Search for Employee Training Records.
3. Verify that the table is not visible.

## Expected Security Behavior
The configured ACLs should allow authorized users with the required role to access the Employee Training Records while restricting other users.

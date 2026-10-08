# IAM-user-lifecycle-project
Beginner IAM Project demonstrating User Lifecycle management (Joiner-Mover-Leaver), RBAC and Least Privilege
## 1. Project Overview

This project demonstrates a basic Identity and Access Management (IAM)
User Lifecycle Management process using the Joiner-Mover-Leaver (JML) model.

The project focuses on how an organization manages user access throughout
an employee's lifecycle.

## 2. Joiner – Employee Onboarding

### Scenario

Ananya Rao joins TechNova as a Finance Analyst.

### Employee Details

- Employee Name: Ananya Rao
- Job Title: Finance Analyst
- Department: Finance
- Employment Status: New Employee

### Required Access

Ananya requires access based on her job responsibilities:

- Microsoft 365
- Finance group
- Finance application
- Company HR portal

### IAM Process

1. HR creates the employee record.
2. IAM team receives the onboarding request.
3. Employee information is verified.
4. User account is provisioned.
5. User is added to the appropriate group.
6. Required access is assigned.
7. MFA is enabled.
8. Access is verified.

### Least Privilege

Ananya should receive only the permissions required for her Finance Analyst
role.

She should NOT receive unnecessary administrative privileges such as:

- Global Administrator
- Security Administrator
- IT Administrator

### IAM Process

1. HR creates the employee record.
2. IAM team receives the onboarding request.
3. Employee information is verified.
4. User account is provisioned.
5. User is added to the appropriate group.
6. Required access is assigned.
7. MFA is enabled.
8. Access is verified.

### Least Privilege

Ananya should receive only the permissions required for her Finance Analyst role.

She should NOT receive unnecessary administrative privileges such as:

- Global Administrator
- Security Administrator
- IT Administrator
## 3. Mover – Employee Role Change

### Scenario

Ananya Rao is promoted from Finance Analyst to Senior Finance Analyst.

Her responsibilities have increased, so her access must be reviewed and
updated according to her new role.

### IAM Actions

1. HR updates Ananya's job title and role.
2. IAM team receives the role-change request.
3. Existing access is reviewed.
4. Access that is no longer required is removed.
5. New access required for the Senior Finance Analyst role is assigned.
6. Group memberships are updated if required.
7. Access is verified after the changes.

### Access Review

| Access | Action | Reason |
|---|---|---|
| Microsoft 365 | Keep | Required for work |
| Finance group | Keep | Still part of Finance |
| Finance application | Keep | Required for role |
| Senior Finance application | Add | Required for new responsibilities |
| Unnecessary previous access | Remove | Least privilege |

### Least Privilege

Ananya's permissions should be aligned with her new responsibilities.

A role change should not automatically result in additional
administrative privileges. Only the access required for the new role
should be granted.
## 4. Leaver – Employee Offboarding

### Scenario

Ananya Rao leaves TechNova and her employment is terminated.

The IAM team must ensure that her access is removed promptly and
that her account cannot be used after her departure.

### IAM Actions

1. HR confirms the employee's termination.
2. IAM team receives the offboarding request.
3. User account is disabled.
4. Active sessions are revoked.
5. Group memberships are removed.
6. Application access is removed.
7. Assigned roles and permissions are reviewed and removed.
8. Company devices and resources are recovered according to company policy.
9. Offboarding actions are documented.
10. The IAM team verifies that access has been successfully removed.

### Access Removal

| Access | Action | Reason |
|---|---|---|
| Microsoft 365 | Remove | Employee has left |
| Finance group | Remove | No longer required |
| Finance application | Remove | No longer required |
| HR portal | Remove | No longer required |
| Active sessions | Revoke | Prevent continued access |

### Security Principle

Access should be removed as part of the employee offboarding process
to reduce the risk of unauthorized access.

### Verification

After access removal, the IAM team should verify that the user's account
is disabled and that unnecessary access, group memberships, roles and
active sessions have been removed.

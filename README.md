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
## 5. Role-Based Access Control (RBAC)

### Overview

Role-Based Access Control (RBAC) is an access control model where
permissions are assigned to roles, and users receive access based on
their assigned roles.

This helps organizations manage access consistently and reduces the
need to assign permissions individually to every user.

### Example

For Ananya Rao, who works as a Finance Analyst:

| Role | Access |
|---|---|
| Finance Analyst | Finance application |
| Finance Analyst | Finance group |
| Finance Analyst | Required Microsoft 365 resources |

Ananya should receive only the permissions associated with her job
responsibilities.

### RBAC Workflow

1. Identify the employee's job role.
2. Identify the access required for that role.
3. Assign the appropriate role or group.
4. Grant the required permissions.
5. Review access periodically.
6. Remove access when the role changes or employment ends.

### Benefits of RBAC

- Simplifies access management.
- Provides consistent access based on job roles.
- Supports least privilege.
- Reduces excessive permissions.
- Makes access reviews easier.
- Helps reduce the risk of unauthorized access.
- ## 6. Least Privilege

### Overview

The Principle of Least Privilege means giving a user only the minimum
level of access required to perform their job responsibilities.

Users should not receive unnecessary permissions or administrative
privileges.

### Example

Ananya Rao is a Finance Analyst.

She requires access to:

- Finance applications
- Finance group resources
- Required Microsoft 365 resources

She does not require:

- Global Administrator privileges
- Security Administrator privileges
- IT Administrator privileges
- Access to unrelated applications

### Access Decision

| Request | Decision | Reason |
|---|---|---|
| Finance application | Grant | Required for job |
| Finance group | Grant | Required for job |
| Microsoft 365 | Grant | Required for work |
| Global Administrator | Deny | Not required |
| Security Administrator | Deny | Not required |
| Unrelated application | Deny | Not required |

### Why Least Privilege Matters

Applying least privilege helps:

- Reduce unauthorized access.
- Reduce the impact of compromised accounts.
- Prevent excessive permissions.
- Improve security.
- Support access reviews and compliance.

### IAM Practice

Before granting access, the IAM team should verify:

1. Who is requesting the access?
2. What access is being requested?
3. Why is the access required?
4. Is the access appropriate for the user's role?
5. Is there a less privileged option?
6. When should the access be reviewed or removed?
## 7. Access Review

### Overview

An access review is a periodic process used to verify whether users
still need the access assigned to them.

The purpose is to identify and remove unnecessary or outdated access.

### Example

Ananya Rao's access is reviewed periodically.

The IAM team checks:

- Current job role
- Group memberships
- Application access
- Assigned permissions
- Administrative privileges

### Access Review Decision

| Access | Review Decision | Reason |
|---|---|---|
| Finance group | Keep | Required for current role |
| Finance application | Keep | Required for job |
| Microsoft 365 | Keep | Required for work |
| Old application access | Remove | No longer required |
| Unnecessary administrative role | Remove | Violates least privilege |

### Access Review Process

1. Identify users and their assigned access.
2. Compare access with the user's current job responsibilities.
3. Review group memberships and roles.
4. Identify unnecessary or excessive access.
5. Remove access that is no longer required.
6. Document the review decision.
7. Verify that the changes were completed.

### Benefits

Regular access reviews help organizations:

- Maintain least privilege.
- Detect excessive access.
- Remove outdated permissions.
- Reduce security risks.
- Support compliance requirements.
- ## 8. Complete JML Workflow

The Joiner-Mover-Leaver lifecycle can be summarized as:

### Joiner

Employee joins the organization.

HR request → Identity verification → Account provisioning →
Group assignment → Access assignment → MFA → Access verification

### Mover

Employee changes role or department.

HR role change → Access review → Remove unnecessary access →
Assign new required access → Verify access

### Leaver

Employee leaves the organization.

HR termination → Disable account → Revoke sessions →
Remove group memberships → Remove application access →
Remove roles → Verify access removal → Document completion

### Overall Workflow

Joiner → Access Provisioning → Mover → Access Review →
Leaver → Access Deprovisioning

## 9. IAM Concepts Demonstrated

This project demonstrates the following IAM concepts:

- Identity Lifecycle Management
- Joiner-Mover-Leaver (JML)
- User Provisioning
- User Deprovisioning
- Role-Based Access Control (RBAC)
- Least Privilege
- Authentication
- Authorization
- Group-Based Access
- Access Reviews
- Access Management
- Role Changes
- Offboarding

- ## 10. Authentication vs Authorization

### Authentication

Authentication verifies the identity of a user.

Example:

A user signs in using their username, password and MFA.

The system verifies that the person is who they claim to be.

### Authorization

Authorization determines what an authenticated user is allowed
to access.

Example:

After Ananya signs in, authorization determines whether she can
access the Finance application.

### Difference

Authentication = "Who are you?"

Authorization = "What are you allowed to access?"

## 11. Learning Reference

This project was created as a practical learning exercise based on
Microsoft Learn concepts related to Microsoft Entra ID and Identity
and Access Management.

Microsoft Learn:
https://learn.microsoft.com/training/

## 12. Project Outcome

Through this project, I learned how IAM teams manage user identities
and access throughout the employee lifecycle.

Key learning outcomes:

- Understanding the Joiner-Mover-Leaver lifecycle.
- Understanding user provisioning and deprovisioning.
- Applying Role-Based Access Control.
- Applying the Principle of Least Privilege.
- Understanding access reviews.
- Understanding authentication and authorization.
- Understanding why access must be modified when an employee changes
  roles.
- Understanding why access must be removed when an employee leaves.

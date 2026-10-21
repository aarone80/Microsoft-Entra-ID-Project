# Microsoft Entra ID IAM Home Lab

## Overview

This project documents a hands-on Microsoft Entra ID home lab built around a fictional organisation, **AETech**. The aim was to practise common Identity and Access Management (IAM) tasks and explore security controls available through a Microsoft Entra ID P2 trial.

The lab focuses on managing user access throughout the identity lifecycle, controlling privileged access, and evaluating Conditional Access policies.

## Objectives

- Create users with relevant job titles and department attributes.
- Use security groups to organise access by role or department.
- Practise joiner, mover and leaver (JML) procedures.
- Explore dynamic group membership based on user attributes.
- Configure  administrative access with Privileged Identity Management (PIM).
- Configure and evaluate Conditional Access policies.
- Configure an Access Review.

## What I Implemented

### 1. User and Group Management

Created user accounts for a fictional company and populated their department and job title attributes. Created security groups to represent departmental or project-based access, using an access matrix to help define the intended membership.

### 2. Joiner, Mover and Leaver (JML)

- **Joiner:** Created a new user account, populated identity attributes and assigned access through group membership.
- **Mover:** Changed an employee's department from Sales to HR, removed the Sales group membership and added the HR group membership. Reviewed project-group access as part of the change.
- **Dynamic group membership:** Configured a Finance group rule based on user attributes and verified that a newly created Finance user was added automatically.
- **Leaver:** Blocked sign-in for a departing employee, cleared the department and job title attributes, and checked group access. The account was retained in the lab to reflect a possible need to preserve records or evidence.

### 3. Privileged Identity Management (PIM)

Configured an eligible User Administrator role assignment for a fictional Helpdesk Administrator. The configuration included activation requirements such as multi-factor authentication (MFA), a justification and a time limit, rather than relying on a permanent active assignment.

### 4. Conditional Access

Configured and evaluated policies intended to:

- Require MFA for a test group.
- Apply additional protection to privileged accounts.
- Block legacy authentication clients.
- Require MFA when sign-in risk is medium or high.

**Testing note:** Policies were evaluated using the Conditional Access **What If** tool and Report-only mode where appropriate. These tests help assess policy targeting and expected outcomes; they do not, by themselves, prove that a policy has enforced access controls during a real sign-in. The privileged-account policy also had an administrator-account exclusion in the lab, so the evaluation demonstrated that exclusion rather than proving enforcement against that excluded account.

### 5. Access Reviews

Configured a recurring Microsoft Entra role access review for the Helpdesk Administrator role, scheduled quarterly over one year. The settings included handling for cases where a reviewer does not respond.

This project documents the configuration; it should not be interpreted as evidence that all scheduled reviews have been completed.

## Skills Practised

- Microsoft Entra ID user and group administration
- Identity lifecycle management (joiner, mover and leaver)
- Group-based and dynamic access management
- User attributes and access assignment
- Privileged Identity Management (PIM)
- Conditional Access policy configuration and evaluation
- MFA and legacy authentication controls
- Sign-in risk policy concepts
- Access review configuration
- Testing, troubleshooting and documenting IAM changes



## Limitations and Next Steps

This is a home lab using fictional users, not a production tenant. Some Conditional Access testing was performed through What If and Report-only evaluation rather than by enforcing every policy in live sign-ins.

Potential next steps include completing and documenting an access review, testing policies against additional user scenarios, and expanding the lab with further identity governance and automation exercises.

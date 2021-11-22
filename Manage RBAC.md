[//]: <> (AZ-104 Notes | Michael Teske | Pluralsight)

# ***Manage Role-Based Access Control***

## **Role-Based Access Controls**

> - *RBAC can be used to assign permissions to:*
>   - Users
>   - Groups
>   - Applications
> - *The scope of role assignment can be:*
>   - Subscription
>   - Resource Groups
>   - Single Resource

*RBAC Examples:*

> - Allow one user to manage VMs in a subscription and another user to manage vNets
> - Allow a DBA (Database Administrator) group to manage SQL DBs in a subscription
> - Allow an application to access all resources in a Resource Group

### *Security Principals*

**User:** Has a profile in AAD, can be assigned to suers in other tenants

**Group:** Multiple users are assigned within this scope, roles assgined to a group impact all users

**Service Principal:** A security ID for applications or services to access specific Azure resource (User / Password for application)

**Managed Identity:** Typically used in developing cloud applications to handle credential management (i.e. Key Vault)

#### *Roles*
(*Only apply to resource itself, not what the resource contains*)

**Owner:** Full access to all resources and grant access
**Contributor:** Can create/manage all resources, **cannot** grant access
**Reader:** Can view existing resources, cannot manage (i.e. cannot start/stop a VM)
**User Access Administrator:** Allows you to manage access to Azure resources

#### *Deny Assignments*

- Blocks user from performing specific actions if a role assignment allows it
- Created and managed in Azure to protect resources
- Can only be created using Azure Blueprints or Managed Apps
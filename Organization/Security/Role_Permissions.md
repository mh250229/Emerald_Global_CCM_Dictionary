## Role Permissions

**Role Permissions** allow users assigned to a specific role to create or change the passwords of other roles.

For example, you specify that users assigned to the Supervisor role can create the Cashier role, while users assigned to the Store Manager role can create all roles.

**Reference Path:** *Organization/Security/Role Permissions*

![Role Permissions Screen](/Images/RolePermissionsScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Role**|The role assigned with permissions to configure other roles or change their passwords.|
|**Roles Allowed for Configuration**|The roles users assigned to the role displayed in the Role field can configure. Multiple roles can be selected.<BR>For example, allow users assigned to the Store Manager role to only create the Cashier and Supervisor roles.<BR>If no roles are selected, users assigned to the role displayed in the Role field cannot create any other user's role.|
|**Roles Allowed for Password Change**|The roles users assigned to the role displayed in the Role field can change the user password. Multiple roles can be selected.<BR>For example, allow users assigned to the Store Manager role to only change the password of users assigned to the Cashier and Supervisor roles<BR>If no roles are selected, users assigned to the role selected in the Role field cannot change the passwords of any other user.|

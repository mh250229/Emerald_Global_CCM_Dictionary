## Users

**Users** defines the users in the system. For each user you can define personal details, authentication information (password/PIN), assign the user to roles relevant to their job requirements and view a clear indication if the user is active or not.

To log into the Store Manager or any touchpoint, users must be provided with a password, PIN, or both.

Passwords are assigned as a more ’strict’ authentication method. Once users are set up, a password is assigned, and is used by privileged users to sign into the Store Manager. The password policy determines password length, strength limitations, expiry periods, user lockout condition and more. Defining a strong password policy minimizes the risk of password theft or an account being ’hacked’. During user setup, when a password is provided, it is validated against the password policy.

PINs are used as a simpler authentication method, for example, where the touch point doesn’t allow typing alphanumeric characters, or/and when sign-in should be swift. A PIN is mostly used by cashiers and supervisors signing into the POS touchpoint.

A user is assigned both, for example, if they are required to access both the Store Manager and a POS touchpoint, and the retailer requires a secure sign-in process for the Store Manager, and a simple and faster sign-in to the POS touchpoint.

**Reference Path:** *Organization/Security/Users*

![Users Screen](/Images/UsersScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Store**|The store the users are assigned to.|
|**User Name**|The user name.|
|**First Name**|The user’s first name.|
|**Last Name**|The user’s last name.<BR>To comply with EU GDPR (European Union General Data Protection Regulations) requirements 75% of the user’s last name is masked, showing minimum one letter. All masking is done on the end of the name. For example:<BR>Johnson = Jo***** <BR>Levi = L*** <BR>Dan = D** <BR>Lo = L*<BR>If only one user is retrieved, the user's last name is not masked.|
|**Role**|The role assigned to the user.|
|**Users Grid**|
|User Name|The name assigned to the user|
|First Name|The user’s first name.|
|Last Name|The user’s last name.|
|Status|The user status: The options are:<BR><BR>**Active** - indicates that the user is able to sign in and access the touchpoints and perform any of the actions assigned to the user's role.<BR>**Disabled** - indicates that the user cannot sign in or access the touchpoints or perform any of the actions functions assigned to the user's role.<BR>**Locked** - indicates that the user was automatically locked out. For example, users who try to log in to the system and enter an incorrect password are automatically locked out of the system after a defined number of tries. Once a predefined period of time has elapsed the user is automatically unlocked.| 
|Role|The role assigned to the user, e.g., Administrator, Store Manager, Cashier, etc.<BR>Roles set the user’s permission levels.|

**Reference Path:** *Organization/Security/Users/Add New*

![User Form](/Images/UserForm.png)

|**Field**|**Description**|
|---------|----------|
|**User Name**|The user (login) name.|
|**First Name**|The user’s (personal) first name.|
|**Last Name**|The user’s (personal) last name.|
|**Status**|The user’s status. The options are:<BR><BR>**Active** - indicates that the user is able to sign in and access the touchpoints and perform any of the actions assigned to the user's role.<BR>**Disabled** - indicates that the user cannot sign in or access the touchpoints or perform any of the actions functions assigned to the user's role.<BR>**Locked** - indicates that the user was automatically locked out. For example, users who try to log in to the system and enter an incorrect password are automatically locked out of the system after a defined number of tries. Once a predefined period of time has elapsed the user is automatically unlocked.|
|**Personal Details**||
|Phone|The user’s phone number.|
|E-mail|The user’s e-mail.|
|Birth date|The user’s date of birth.|
|**Authentication**||
|Password|The password used by users to log into the system. Passwords are validated against the Password Policy, which determines the password length and strength limitations.<BR>A password is required to use the Emerald Global Office.<BR>If the default touch point group authentication method in security settings is Password, a password is required to sign in to the touch point.<BR>If the authentication method is Active Directory, the Password field is blank.|
|Confirm Password|The reconfirmed user’s password.|
|PIN|The PIN number used by the user, e.g., cashiers, supervisors, to sign in to touchpoints, and are used when a simpler and quicker authentication method is required.<BR>PINs are validated against the PIN Policy, which determines the length and character limitations of the PIN.|
|Confirm PIN|The reconfirmed user’s PIN.|
|Change password at next logon|Indicates that the user must change their password at the next login.|
|Change PIN at next logon|Indicates that the user must change their PIN at the next login.|
|Active directory user name|The user name defined in the (Windows Network) Active Directory. Once defined, the system uses the Active Directory user credentials to authenticate the user.<BR>When Active Directory is used as the authentication method in security settings, the user is not required to define a password.|
|Allow barcode authentication|Indicates that the user can scan a barcode to log in to the touch point.|
|**Role Assignment**|The number of roles assigned to the user is displayed in parenthesis.|
|Role|The roles linked to the user, e.g., admin, cashier, cash office person, etc.<BR>You can assign more than one role to a user. For example, the user may be assigned to Store 1 as a cashier and to Store 2 as a supervisor.|
|Stores|The store hierarchy in which the user roles apply. Users can have different roles in different stores. For example, a user may be a Manager in Store 1, and Cash Office Personnel in Store 2.|
|Is only for training mode|Indicates that the Role assigned to a certain user is only applicable in training mode. For example, you can specify that a new user training to be a cashier can only work in training mode. A user may have two roles, and one of the roles may be defined so that it is only applicable in training mode.<BR>**Note:** Users assigned to Training Mode only cannot change their passwords in Training Mode.|
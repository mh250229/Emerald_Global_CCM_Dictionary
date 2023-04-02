## Security Policy

**Security Policy** defines global definitions for password/PIN authentication and a policy to validate each authentication method and its contingencies.

To sign in to the Store Manager or any touchpoint, users must be provided with a password, PIN, or both. For example, a user would be assigned both if they are required to access both the Store Manager and a POS touchpoint and the retailer requires a more secure sign-in process in the Store Manager, and a simpler faster sign-in to the POS touchpoint.

The system supports the following authentication methods:

* Passwords are generally a more ’strict’ authentication method. Once users are set up and a password is assigned, the password is used to sign in to the Store Manager. The password policy determines password length and strength limitations, expiry periods, user lockout condition and more.  Defining a strong password policy minimizes the risk of password theft or an account being ’hacked’.
* PINs are used as a simple authentication method, for example, where the touchpoint doesn’t allow the typing of alphanumeric characters, and/or when sign-in should be swift. A PIN is mostly used by cashiers and supervisors signing in to the POS touchpoint. The PIN policy determines the PIN length, if it is numeric only or alphanumeric, expiry periods, user lockout conditions and more.
* Barcodes with the login details can be assigned to a user. On swiping the card, the system validates the user's login details and allows the user to access the system.
* Active Directory authentication is used to enter the username defined in the Active Directory. The Active Directory stores all user information and access settings in a central database. Once defined, the user passwords are authenticated externally by the Active Directory.

The system’s touchpoint default authentication method is Password and can be changed to PIN.

The user can sign in, approve business rules, etc., to authenticate a user's credentials with their defined authentication method.

**Reference Path:** *Organization/Security/Security Policy*

![Security Policy Screen](/Images/SecurityPolicyScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Default authentication method**|The authentication method used to authorize users when signing in to touchpoint groups. You can select different authentication methods for specific touchpoints. Password is the default authentication method.<BR>The options are:<BR>**Password** - indicates that users must sign in using a password<BR>**PIN** - indicates that users must sign in using a PIN<BR>**Barcode** - indicates that users must sign in by scanning a barcode on a card<BR>**Note:** The same authentication method defined in the Security Policy is used throughout the system when user validation is required, for example, when a supervisor is required to approve a Business Rule. If the system authentication method is Password, then the supervisor can only use their password to approve the Business Rule. If the supervisor enters their Pin or barcode, the rule is not approved.
|**Touchpoint Group Settings**|The authentication methods used to sign in to specific touchpoint groups. For example: Users can sign in to the POS terminals in the Main POS touchpoint group using a PIN, and sign in to the POS terminals in the Pharmacy touchpoint group using a password.|
|Touchpoint group|The Touchpoint Group for which the authentication method is defined.|
|Authentication method|The authentication methods used to verify access to the Touchpoint Group.  The options are: **Password** / **PIN** / **Barcode**.|
|Automatic Lock Time (Minutes)|The number of minutes of inactivity which automatically locks the user out of the touchpoint.|
|**Office authentication**|The authentication method used to verify the user password in the Store Manager. Users must sign into the Store Manager using a Password.|
|Authentication method|The authentication method used to verify the user's password when accessing the Store Manager. The options are:<BR>**OIDC (External)** – user authentication is performed via OIDC (External) authentication to allow third-party applications to verify the identity of the end-user. See also: OpenID Connect (OIDC) Protocol - Emerald Global CCM<BR>**Active Directory** - user authentication is performed in a central repository. The user's user name and access settings are defined and stored in the Active Directory central database.  Once defined, the user passwords are authenticated externally by the Active Directory. When using Active Directory authentication the Active Directory user credentials are in use, and therefore password authentication is not required for the user.<BR>**Emerald** - user authentication is performed by the server|
|Domain|The domain in which the servers connected to Active Directory are located.<BR>The Domain and Server Path fields are only enabled for Active Directory.|
|Server name/IP|The name or IP address of the server that connects to Active Directory.|
|**Password Policy**|The policy used to validate user passwords. Passwords require a stricter authentication policy and are used by privileged users to access the application.|
|Password expires after (days)|The number of days after a password is set or changed that the password expires. The default is 90 days.|
|Notify before expiry (days)|The number of days before the user's password expire that a notification message is displayed. The user can then reset their password or continue to perform activities. The default is 6 days.<BR>Cannot be set to 0 or more than the number of days defined in the Password expires after (days) field.|
|Password can’t be repeated|The number of password changes which must take place before a previously used password can be reused. The default is 4 times.|
|Strong password required|When checked, requires user passwords to use specific characters to minimize the risk of password theft or account hacking.  For example, a strong password should be long and can include letters, punctuation, symbols, and numbers. The default is No.|
|Minimum password length|The minimum number of characters the password must contain. The default is 0 Characters. This field is disabled if the Strong password required field is checked.|
|Maximum password length|The maximum number of characters the password must contain.|
|Allowed failed sign-in attempts|The number of times users can unsuccessfully sign in before the user is locked out of the system. The default is 5.|
|Automatic Unlock User (minutes)|The number of minutes after which a locked user is automatically unlocked. The default is 15 minutes.|
|![Restore Default Button](/Images/RestoreDefaultButton.png)|To restore the default password settings.|
|**PIN Policy**|The policy used to validate user PIN (Personal Identification Number) numbers. PINs require a simpler authentication method, and are used to access touchpoints, e.g., POS.|
|Days before PIN expiry|The number of days after which a user's PIN expires.|
|Days before PIN expiry warning|The number of days after which a message is displayed informing the user that the PIN is due to expire.|
|Cannot repeat the same PIN|The number of times a PIN number must be changed before a previously used PIN number can be reused.|
|Alphanumeric characters|The PIN can contain both letter and number characters.|
|Minimum PIN length|The minimum number of characters the PIN must contain.|
|Maximum PIN length|The maximum number of characters the PIN must contain.|
|Allowed failed sign-in attempts|The number of times users can unsuccessfully sign in before the user is locked out of the system.|
|Automatic unlock user (minutes)|The number of minutes after which a locked user is automatically unlocked.|
|![Restore Default Button](/Images/RestoreDefaultButton.png)|To restore the default PIN security settings.|
|**Barcode Policy**|The policy used when users sign in by scanning a barcode on a card.|
|Days Before Expiry|The number of days after which the user's barcode expires. The count starts from when the barcode is printed. This field cannot be 0. One day is equivalent to a business day in the system.|
|**Session**|The time after a user accesses the Store Manager until the user logs out.|
|Default timeout (minutes)|The number of minutes after which a user login session times out. For example, when the user logs from the POS or the CCM with a username and password.|
|Touchpoint timeout (minutes)|The number of minutes after the Touchpoint is left idle, the Touchpoint times out. A Touchpoint login is then required to login again. The defined timeout is the same timeout for all Touchpoint types.|
|Service Agent timeout (minutes)|The number of minutes after which if there is no activity, between the client and server, for example, between the Emerald Global Server and the Catalog service, a timeout is triggered.<BR>After a timeout is reached, on the next request of the same session, the requester is prompted with an invalid session message and must start a new session.|
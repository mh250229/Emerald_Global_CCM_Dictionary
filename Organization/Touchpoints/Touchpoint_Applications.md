## Touchpoint Applications 

**Touchpoint Applications** display the types of touchpoints configured in the system and the application which supports each touchpoint.

In an Emerald Global deployment, there are different kinds of applications that access the system, e.g., POS terminals, android client, IOS client, office client, Touch POS, Fuel Client, etc.

Each application has specific required settings, including (but not limited to):

* Screen Layout configuration
* Menu configuration
* Keyboard configuration

Touchpoint Applications enable the server to define and save these settings, which can then be used by the different applications.

Roles can be assigned to a touchpoint for logging the touchpoint into the Emerald Global server. This enables the server to identify the touchpoint and communicate with it before a user has logged in to the touchpoint.

**Reference Path:** *Organization/Touchpoints/Touchpoint Applications*

![Touchpoint Applications Screen](/Images/TouchpointApplicationsScreen.png)

|**Field**|**Description**|
|---------|----------|
|**ID**|The name of the touchpoint. The list of touchpoints is based on the default installation data and cannot be modified.|
|**Description**|The name of the application which supports the relevant touchpoint. You can manually enter the name of the application.|
|**Role**|The role assigned to the touchpoint which is used to log in to the Emerald Global server to authenticate the touchpoint application. The role defines the operations that can be carried out on the server by the touchpoint. Retailers can control the permitted operations by linking specific actions to a Role, and then assigning the Role to the touchpoint.<BR>A touchpoint can connect to the server only after it has been authenticated. Each touchpoint logs in using its own credentials and role.<BR>For example, users are not required to log in to the SelfScan. However, to maintain security, the SelfScan touchpoint must log in to the Emerald Global server, so that the server can authenticate the touchpoint. The SelfScan logs in using the touchpoint ID and assigned Role.|
|**Default Account Profile**|The default account profile. If no default Account Profile is defined for the Touchpoint Type, the system uses the default Account Profile defined for the Account Type.|
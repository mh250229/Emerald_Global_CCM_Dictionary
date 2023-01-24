## Touchpoints

**Touchpoints** is used to define touchpoints and connect them to a specific touchpoint group or store.

A touchpoint can be any client, e.g., a POS terminal, self-checkout.

You can define as many touchpoints as required from one central place. In addition, you can link devices to a touchpoint.

For example: Create a POS touchpoint with a printer, PIN pad, POS display, drawer and scale.

**Reference Path:** *Organization/Touchpoints/Touchpoints*

![Touchpoints Screen](/Images/TouchpointsScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Store Name**|To filter for touchpoints by the store linked to the touchpoint.|
|**Touchpoint Group**|To filter for touchpoints by the touchpoint group to which the touchpoint is linked.|
|**Secondary Touchpoint Group**|To filter for touchpoints by the secondary touchpoint group assigned to the touchpoint.|
|**Touchpoint Type**|To filter for touchpoints by the touchpoint’s type (e.g. POS, Self-Checkout).|
|**Touchpoint ID**|To filter for touchpoints by the touchpoint ID.|
|**Is Registered**|To filter for touchpoints by registered touchpoints.|
|**Touchpoints**|The touchpoint details.|
|**ID**|The touchpoint ID.|
|**Is Registered**|Indicates if the touchpoint is registered. A registered touchpoint is a touchpoint that has been authenticated and a session was created between the touchpoint and the Emerald Global server. When a session is created, a security token is saved encrypted in the touchpoint app.config file. The touchpoint can then be identified by the server.|
|**Is Clustered**|Indicates if more than one touchpoint application instance can be registered to the same server, for example, in a cluster touchpoint environment, an Emerald Global POS and FLSCO can share the same Touchpoint ID, meaning they can share the same transactions.<BR>The options are<BR><BR>**Yes** – indicates the touchpoint is part of a cluster instance and can be registered to the same server as another touchpoint ID, for example, an Emerald Global POS and FLSCO can share the same Touchpoint ID.<BR>**No** - indicates that the touchpoint can only be registered with its own ID and is not part of a cluster instance. This is the default value.|
|**Store ID**|The ID of the store the touchpoint is assigned to.|
|**Store Name**|The name of the store the touchpoint is assigned to.|
|**Touchpoint Group**|The touchpoint group the touchpoint is assigned to.
|**Touchpoint Type**|The touchpoint application assigned to the touchpoint. Touchpoint Applications define the specific settings that are required in order for the touchpoint to function properly, such as Keyboard, Screen Layout and Menu configuration.|

Reference Path: Organization/Touchpoints/Touchpoints/Add New 

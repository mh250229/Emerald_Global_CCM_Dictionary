## Stores

**Stores** is used to add, view or modify stores in the system.

When a store is setup, it is linked to a store hierarchy and added to a specific group within a chain of stores. The hierarchy is the classification of a group of stores according to your store's policy. Some may define the hierarchy according to the stores’ zone or maybe size.

In addition, you can link stores to touchpoint groups and specify that a touchpoint group such as self-checkout is part of a defined store.

**Reference Path:** *Organization/Stores/Stores*

![Stores Screen](/Images/StoresScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Business Unit**|The business unit to which the store is linked. A Business Unit is a parent level in the Store Hierarchy which groups stores. Stores can be grouped by region. A Business Unit of a store can either be the store hierarchy or a category in the store hierarchy depending on the configured system environment.|
|**Status**|The Business Unit status, Active or Not active. By default, the system displays all stores regardless of the status.|
|**Stores**||
|Store ID|The unique ID of the store.|
|Store Name|The name of the store.|
|Business Unit|The business unit to which the store is linked. Business Unit is a parent level in the Store Hierarchy which groups stores. Stores can be grouped by region. A Business Unit of a store can either be the store hierarchy or a category in the store hierarchy depending on the configured system environment.|
|City|The name of the city in which the store is located.|
|Street|The name of the street in which the store is located.|
|Phone|The phone number of the defined store.|

**Reference Path:** *Organization/Stores/Stores/Add New Store*

![Store Form](/Images/StoreForm.png)

|**Field**|**Description**|
|---------|----------|
|**Store ID**|The unique ID of the store.|
|**Store Name**|The name of the store.|
|**Parent**|Location of the store within the hierarchy.|
|**IsActive**|Indicates if the store is active or not.|
|**Contact and Location**|The store’s contact and location details.|
|Street|The street on which the store is located.|
|City|The city in which the store is located.|
|State|The state in which the store is located.|
|Country|The country in which the store is located.|
|Phone|The store’s telephone number.|
|Fax|The store’s FAX number.|
|Contact Person|The name of the store’s contact person.|
|**Touchpoint Groups**|Assigns Touchpoint Groups to the store.|
|Touchpoint Groups|The primary touchpoint groups in the store. Every touchpoint must be linked to a Touchpoint Group which is then linked to the store. Once a Touchpoint Group is linked to a store, all the touchpoints in the group are automatically linked.|
|Secondary Touchpoint Groups|The secondary touchpoint group assigned to the store in addition to the Primary Touchpoint Group.<br>For example, all POS touchpoints may be assigned to the same Primary Touchpoint Group. However, some of the POS touchpoints may require different PLU menus. Retailers can assign those touchpoints to a Secondary Touchpoint Group and apply the PLU Menu configuration to the Secondary Touchpoint Group only.|
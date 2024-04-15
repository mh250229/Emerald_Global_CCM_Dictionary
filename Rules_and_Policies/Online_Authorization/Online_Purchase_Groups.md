## Online Purchase Groups

**Online Purchase Groups** define the different providers, communication settings and item groups required when selling online items such as gift cards. An online item is any item that requires the third-party authorization during the sale process.

For example, if you sell gift cards in the store, you set up an online purchase group for gift cards and the relevant provider.

Online Purchase Groups represent a profile of online items as follows:

* Online Items that are sold under the same conditions, e.g., the item code is scanned, and the item is then sold.
* Online Items that are linked by specific external identification, e.g., a plan code. The plan code is scanned, and a list of the online items in the plan is displayed. The cashier then selects the relevant item from the list.

**Reference Path:** *Rules & Policies/Online Authorization/Online Purchase Groups*

![Online Purchase Groups Screen](/Images/OnlinePurchaseGroupsScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Name**|The name of the Online Purchase Group.|
|**Description**|A description of the Online Purchase Group.
|**Provider**|The name of the provider used to authorize the purchase of items in the Online Purchase Group. The Provider is the Emerald Global component responsible for connecting to the third-party Provider|

**Reference Path:** *Rules & Policies/Online Authorization/Online Purchase Groups/Add New*

![Online Purchase Group Form](/Images/OnlinePurchaseGroupForm.png)

|**Field**|**Description**|
|---------|----------|
|Name|The unique name of the Online Purchase Group.|
|Description|Description of the Online Purchase Group.|
|Locations|The locations the online purchase group is linked to.|
|Touchpoint Groups|The touchpoint groups on which the online purchase group is valid.|
|**Communication Settings**||
|Provider|The name of the provider which authorizes the items in the online purchase group. The provider is the Emerald Global component which connects to the third-party provider.|
|Target Module|The name of the external provider with which the purchase group is integrated.<BR>The target module field must contain the 'Exact Provider' name. For example, ‘ICP.Lottery. A dot is used as a separator between the name and module.<BR>**Note:** When an online item is sold, for example a lottery item, Emerald Global identifies the target module, i.e., the lottery provider, and sends a request via the GSE (Generic Service Engine) (GSEConfigurationMaintenance Request) to the provider with all the details to process authorization of the sale.|
|Authorization Upon|The authorization request is sent to the provider. The options are:<BR><BR>**Item Sale** - the authorization request is sent after the item is scanned.<BR>**Total** - the authorization request is sent after the cashier has completed scanning all the items and the Total function key is selected.<BR>**Transaction Complete** - the authorization request is sent after the transaction is tendered and completed.|
|Confirmation Request Required|Indicates that a pre-authorization request is sent to the provider after the item is scanned, and a confirmation authorization request is sent after the transaction is tendered and completed.<BR>**Bulk Confirmation** – indicates that confirmation for all the items in the sale is made in one request. If not, confirmation is requested per item.<BR>**Transaction Open On Failure** – indicates that a transaction remains open on the POS when a confirmation failure for the Online Item Purchase group with 2 step activation is received during the transaction.<BR>**Note:** The **Bulk Confirmation** and **Transaction Open On Failure** fields are enabled only when the **Confirmation Request Required** field is selected.|
|Refund Request Required|Indicates that checked, items returned in an online transaction require refund requests to the provider.|
|Void Request Required|Indicates that items voided in a transaction require that a void request is sent to the provider. This prevents third-party providers from activating unpaid for items.<BR>This option is not relevant if **Transaction Complete** is selected in the **Authorization Upon** option.|
|Exclusive Item|Indicates that the online item can only be purchased exclusively in a transaction and cannot be purchased with other items. On scanning the item at the POS, if the system identifies other items in the transaction, an error is prompted, and the item cannot be added.|
|External Unique Identifier|The external identifier used to authorize the items by the third-party provider.<BR>Select one of the options:<BR>**Second Barcode** - The External Identifier is the number on the item's long barcode that holds additional information about the item. This barcode is scanned along with the main barcode (that holds the Item Code number) if the External Identifier is not embedded in the first barcode.<BR>**In Barcode** - The Item ID and External Identifier are embedded in the item’s long barcode. In this case, the Item Code and the External Identifier can be extracted only by scanning the long barcode of the Item.<BR>**Card** - The External Identifier is embedded in the item’s magnetic stripe. The number is read when swiping the item after scanning the main barcode (that holds the Item code number).<BR>**External** - The External Identifier is defined by the Online Purchase Group next to each item included in the group. When the Item Code is scanned, the system identifies the External Identifier.|
|Scan Only|Indicates that when purchasing online items, the cashier can only scan the online item, it cannot be keyed-in or swiped.<BR>**Note:** The **Scan Only** field is enabled when **Second Barcode** or **In Barcode** is selected in the **External Unique Identifier** field.|
|Provider Message|A message received from the external third-party provider, usually card instructions. This message is printed on the receipt together with the online item information, when the online item is activated or topped up.|
|**Group Members**||
|Item Code|The code of the item linked to the Online Purchase Group.|
|Description|A description of the item linked to the Online Purchase Group.<BR>This field is automatically populated when the Item Code is entered.|
|External ID|The external ID used by the provider to identify the item.<BR>This field is automatically populated when the Item Code is entered.|
|**Printing Definitions**||
|Online Authorization|Indicates that the online authorization is printed on a separate slip. If not selected, the online authorization is printed on the main receipt.|
|Offline Authorization|Indicates that the offline authorization is printed on a separate slip. If not selected, the offline authorization is printed on the main receipt.|
|Decline|Indicates that the decline online authorization is printed on a separate slip. If not selected, the decline online authorization is printed on the main receipt.|
## Tender Item Restrictions

**Tender Item Restrictions** configure an item eligibility policy to:

Prohibit paying for selected items or item hierarchies using a specific tender, e.g., vouchers cannot be used to purchase cigarettes and alcohol.

* Allow paying for selected items using a specific tender, e.g., Starbucks gift card can be used to purchase Starbucks items only.

The link between tenders and items should be a many-to-many relationship.

For Example:

The store has a policy to prohibit a specific gift card from being used to pay for alcohol. You can set up a policy in the Business Rule domain in the Tender Item Restriction module. If a customer purchases alcohol and the cashier tries to accept a voucher, a message is triggered to prohibit the sale.

**Reference Path:** *Financial/Tendering/Tender Item Restrictions*

![Tender Item Restrictions Screen](/Images/TenderItemRestrictionsScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Name**|The restriction name.|
|**Locations**|The business unit to which the tender item restriction is applied.|
|**Touchpoint Groups**|The touchpoint groups to which the tender item restriction is applied.|

**Reference Path:** *Financial/Tendering/Tender Item Restrictions/Add New*

![Tender Item Restriction Form](/Images/TenderItemRestrictionForm.png)

|**Field**|**Description**|
|---------|----------|
|**Name**|The restriction name.|
|**Locations**|The business unit to which the tender item restriction is applied.|
|**Touchpoint Groups**|The touchpoint groups to which the tender item restriction is applied.|
|**Display Tenders Balance On**|Define when the restricted tender’s balance is displayed on the POS:<BR>**None** - the balance of the restricted tender is not displayed.<BR>**Total** - the total balance of the restricted tender is displayed when the Total button is selected by the cashier.<BR>**Running Total** - a running total of each restricted tender is displayed throughout the transaction. Up to 7 different running tender amounts can be displayed. After the first item linked to the restricted tender is scanned at the POS, the total of each tender is displayed and updated each time another product linked to the tender is scanned.<BR>The running total is displayed next to the amount due section on the touchpoint screen.<BR>**Note:** Up to 7 different running tender amounts can be displayed.|
|**Return Item Reduces Eligibility**|Specifies if the customer returns an eligible item, e.g., an EBT item, the returned amount is deducted from the customer's eligibility balance.<BR>The options are:<BR><BR>**Yes** – indicates that when an eligible item is returned, the amount is deducted from the customer's eligibility balance.<BR>**No** – indicates that when an eligible item is returned, the amount is deducted from the customer's eligibility balance.<BR>**Note:** The eligibility balance cannot be reduced to less than 0.|
|**Allow Reverse Eligibility**|Specifies if the item eligibility can be reversed by the cashier during a SNAP transaction. The user can specify that an item defined as non-eligible for a specific tender can be reversed to be eligible for that specific tender and vice versa.<BR>For example, if a SNAP item is incorrectly defined as a non SNAP item, the cashier can reverse the item eligibility, and sell the item in a SNAP transaction.<BR>The options are:<BR><BR>**Yes** - indicates item eligibility can be reversed.<BR>**No** - indicates item eligibility cannot be reversed.|
|**Tenders**|The tender the restriction is applied to.|
|Relation|The restriction type:<BR>**Prohibit Tender For** – indicates that the tender cannot be used to pay for the selected items.<BR>**Allow Tenders For Only** – indicates that the tender can only be used to pay for the selected items.|
|Items|The items the tender restriction is applied to.|
|Groups|The item groups the tender restriction is applied to.|
|**All items in Ticket Must Be Eligible**|Specifies if the selected restricted tender can be used to pay for any item or only for items eligible for payment with the tender.<br>When selected, all items in the transaction must be eligible for payment with the selected tender.<br><br>**Note:** The All items in Ticket Must Be Eligible checkbox is enabled only when AllowTendersForOnly is selected in the Relation field.<br><br>At the POS, on selecting a restricted tender, the system validates that all the items in the transaction are eligible for the tender. If there are ineligible items in the transaction, the tender is not accepted, and the following error is prompted.<br>‘Cannot pay with tender’<br>‘All items in the ticket must be eligible for tender {x}<br>On partially paying with different tenders, validation is performed once the restricted tender is added.|


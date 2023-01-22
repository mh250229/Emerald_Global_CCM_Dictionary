## Return Policies

Return Policies allows you to define your policy as how to handle items returned to store by customers. Return Policies can be managed centrally from head office. The Central Returns solution provides central management with all return transactions, and determines if items can be returned, when the items can be returned, and specific rules preventing items from being returned for different reasons. For example: Not accepting the return of an item after its return expiry date. It also supports multi stores, enabling shoppers to purchase items in one store and return them at another store within the chain, while complying with defined return policies and rules.

The Central Management solution enables tighter control on all return transactions and security. Different options to prevent fraud are available in the suite of functions offered in the Return Policies module. In addition, a range of functionality is available to make it easy for a customer to return items they do not want, or defective, etc.

Different return policies types can be defined, each with its own details and restrictions. You can define Return Policies associated with a business unit in the organization.

Return Policies must be defined for each type of return transaction. Once defined, the Return Policy is submitted and is active. Multiple return policies of the same type can be defined and submitted, however, only one policy is active at a time. The system validates the activation dates of each submitted policy, and applies the policy with the current date. For example, when customers return items, the system validates the return date against the item purchase date. If a Return Policy was defined on January 1, and another Return Policy of the same type was defined and submitted on February 1, and the customer returns items purchased before February 1, the returned items are validated against the Return Policy defined on January 1.

Return Policy types include:

* **Non Receipted** - to define general refund policy details for all transactions in which items are returned without a receipt.
* **Transaction Based** - to define general refund policy details for all transactions in which items are returned with a receipt.
* **Return All** - to define general refund policy details for returns in which all the items in the transaction are returned. The system validates if the items on the receipt are returnable. If one item on the receipt is not returnable, the return transaction cannot be performed. If the items are all returnable, the cashier does not have to scan the items, and the full transaction is recorded as a return transaction.
* **Gift Receipt Redemption** - to define general refund policy details for the return of an item purchased as a gift. A Gift Receipt is printed when an item is purchased as a gift, and enables the gift recipient to exchange or return the item without the main sale receipt.
* **Bottle Deposit** - to define a refund policy when empty bottles are returned to refund the deposit amount.

For example: The store has a Return Policy for returns based on a transaction. The Return Policy includes rules that specify that the customer cannot return an item after a defined number of days since the item was purchased, or if the packaging is damaged, the item can only be exchanged, etc. On returning the item, the cashier scans the receipt, if the return date exceeds the defined number of days since the original date of purchase, the item cannot be returned.

Users can define Return Policies for future dates, which would be pending until activated.

**Note:** If a Return Policy is not defined for a return type, the specific returns cannot be performed. For example, if a return policy is not defined for Non Receipted returns, then return transactions without a receipt cannot be performed.

**Reference Path:** *Rules & Policies/Returns/Return Policies*

![Return Policies Screen](/Images/ReturnPoliciesScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Business Unit**|The business unit in which you want to search for the return policies.|
|**Date Activated**|The date from which the return policy is implemented.|
|**Time Activated**|The time from which the return policy is implemented.|
|**Date Deactivated**|The date from which the return policy is no longer implemented.|
|**Time Deactivated**|The time from which the return policy is no longer implemented.|
|**Status**|The policy status. The options are:<BR>* Draft - indicates that the policy is defined but has not been submitted<BR>* Submitted - indicates that the policy has been submitted|
|**Grid**||
|Blank Column|Indicates the status of the refund policy. The options are:<BR> ![Checkmark icon](/Images/checkmarkicon.png) - indicates the return policy currently implemented in the system. There can be only one active return policy for each return type.<BR> - indicates that the return policy has been submitted, however the activation date is in the future and is not yet implemented in the system<BR> ![Grey circle](/Images/greycircle.png)- indicates that the return policy was submitted, and implemented in to the system but is no longer active as another submitted policy with the current date has replaced the previously active policy. The system implements this return policy when a customer returns an item or ticket purchased when the return policy was active.<BR> ![Grey circle](/Images/greycheckmark.png) - indicates that the return polic!y is a draft, and has not been submitted.|
|ID|The Return Policy ID which is automatically generated by the system.|
|Policy Name|The name of the Refund Policy.|
|Activation Period|The date and time from which the Refund Policy is implemented in the system.|
|Status|The policy status, e.g., Draft, Submitted.|
|![Grey check circle](/Images/greycheckcircle.png)|To implement the return policy in the system. Once a return policy is submitted, the system validates the Activated Date value. If the date is the current date, the system implements the policy.<BR>Multiple draft policies can be submitted. Each submitted policy must have a different activation date. If a draft policy with the same date as a previously submitted policy is submitted, the system prompts an error, and the user must change the activation date to another date.|
|![Grey copy icon](/Images/greycopyicon.png)|To copy an existing return policy, including all the current values. This enables you to define a return policy based on a previous policy without having to redefine all the policy details.<BR>For example, during the holiday season you may want to create a return policy with fewer restrictions in order to process returns in the store faster. This policy would apply only for the holiday season, and at the end of the season, the previously defined return policy is reapplied. Since there is no time limit on a policy, you can copy the previously defined return policy and then change the activation date to the date and time you want the policy to be reapplied.<BR>This option is available for policies with both a Draft and Submit status. Each copied return policy is assigned a Draft status.|

**Reference Path:** *Rules & Policies/ Returns/Return Policies/Add New*

![Return Policy Form](/Images/returnpolicyform.png)

|**Field**|**Description**|
|---------|----------|
|**Business Unit**|The business unit in which you want to search for the return policies.|
|**Date Activated**|The date from which the return policy is implemented.|
|**Time Activated**|The time from which the return policy is implemented.|
|**Date Deactivated**|The date from which the return policy is no longer implemented.|
|**Time Deactivated**|The time from which the return policy is no longer implemented.|
|**Status**|The policy status. The options are:<BR>Draft - indicates that the policy is defined but has not been submitted<BR>Submitted - indicates that the policy has been submitted|
|**Details Tab**|To define the general details of the return policy.|
|**Restrictions Tab**|To define the restrictions applied to the return policy.|

### Details Tab

The **Details tab** is used to define the general details, such as the basic return policy definitions, as well as the tenders used to reimburse customers. You can specify if the cashier is required to enter a reason when an item is returned, as well as configure the list of reason codes displayed the POS when a specific item is returned.

![DetailsTab](/Images/DetailsTab.png)

|**Field**|**Description**|
|---------|----------|
|**Basic Definitions**|Defines the general details of a return policy|
|Return Best For|Specifies if the refund policy favors the customer or the retailer, when the item is returned against a Receipt in which the same item was purchased more than once and sold for different prices. For example, open price items such as magazines.<BR>The options are:<BR><BR>**Retailer** - indicates that the retailer is favored<BR>**Customer** - indicates that the customer is favored<BR><BR>For example:<BR>The Receipt Return Policy is set up as Return Best For - Retailer.<BR>A customer purchases 2 magazines one is sold $10.00 and the other is sold $5.00, and request a Gift Receipt.<BR>The customer returns one of the magazines and presents the Gift Receipt.<BR>The system validates the Receipt Return Policy, and identifies best for Retailer. The Gift Receipt records the value of $5.00, which is the better deal for the Retailer.<BR>The customer only gets back $5.00.|
|Prompt For Reason Code|Indicates when and if reason codes are prompted at the POS terminal when items are returned.<BR>The options are:<BR><BR>**None** - indicates that reasons codes are not required.<BR>**For each item** - indicates that reason codes are prompted when a return item is scanned, and a reason code must be selected for each item during a return.<BR>**For the entire transaction** - indicates that reason codes are prompted only once in the return transaction, and a reason code must be selected once for the whole transaction.<BR>**Note:** This option is not enabled in Gift Receipt Return Policies.|
|Reason Codes|The reason codes prompted at the POS when an item is returned. Reason Codes can be linked to items or item hierarchies. On performing a return transaction which includes the linked item, the system prompts the selected reason code.|
|Included Products/Categories|The specific items linked to the selected Reason Code. You can narrow down the number of Reason Codes displayed by selecting specific items or categories or linking the reason codes to the entire Merchandise Hierarchy. When one of the linked items is returned at the POS, the system displays only the selected reason codes linked to the item.<BR>Departments are associated to categories in the Merchandise Hierarchy. Reason codes defined for the selected category are applied to all departments linked to that category. For example, you can specify that when a customer returns an item from the Grocery department only the Customer Regrets Reason Code is displayed at the POS.|
|Excluded Products/Categories|The specific items not linked to the selected Reason Code. You can narrow down the number of Reason Codes displayed by excluding specific items or categories. When one of the linked items is returned at the POS, the system does not prompt the reason codes linked to the item.|
|Returned Product Destination|The destiny of the returned item. For example, you can specify that bottles of Coke that are returned, are returned to the store stock, or items for which the expiry date has expired are returned to the supplier.<BR>This option is used to indicate if the returned item is added back to the stock.<BR>The options are:<BR><BR>Repair<BR>Return to Manufacturer<BR>Return to Stock<BR>Return to Supplier<BR>Transform<BR>Undecided|
|Prompt For Price Verify|Indicates that the cashier is required to verify the item price before the item can be returned. For example, the store policy is to refund the full item price up to 3 months from the purchase date, after which only 75% of the item price is refunded. In this scenario, the cashier can reduce the item price by 75% to reflect the store policy.<BR>**Note:** This option is not relevant to Gift Receipt Return Policies.|
|Capture Customer Details|Indicates if the cashier is required to enter the details of the customer returning items.<BR>**Note:** This option is not relevant to Gift Receipt Return Policies.|
|Customer Details|The relevant customer details, such as First Name, Last Name, Address, City, Province, and Postal Code.|
|**Non Receipted Tender**|The tenders and amounts used to refund money to customers when items are returned in a Non Receipted return.<BR>Returned products must be refunded to the customer in the currency used to purchase the product in the original transaction. For example, if a customer purchases a box of chocolates and pays in US dollars, and the customer cannot return the box of chocolates in a store in another region which uses another currency, for example, CAD dollars. Different currencies are not supported|
|Refund Tender|The tender used to refund money to the customer.|
|Up to amount|The amount up to which the tender can be used to reimburse the customer.|
|**Transaction Threshold**|Defines the threshold on the amount that can be refunded to the customer in a return transaction. When the return amount exceeds the specified threshold, only the amount within the threshold is refunded and the selected action is applied to the amount above the threshold.|
|Connected to HQ|The connectivity state for which the transaction thresholds are defined. The options are:<BR>**Offline And Online** - indicates that the defined thresholds are applied when the system is either online or offline from HQ<BR>**Offline** - indicates that the defined thresholds are applied only when the system is offline from HQ<BR>**Online** - indicates that the defined thresholds are applied only when the system is online with HQ<BR>You can create a different threshold for each connectivity state.|
|Minimum Amount|The minimum return amount that must be exceeded in order to be included in the threshold. The selected action is applied to any amount less than the minimum amount.|
|Maximum Amount|The maximum return amount included in the threshold.  The selected action is applied to any amount more than the maximum amount.|
|Action|The action performed when the transaction amount exceeds the defined threshold. The options are:<BR><BR>**Deny** - indicates that any amount which exceeds the specified threshold is not returned<BR>**Allow With Manager Approval** - indicates that any amount which exceeds the specified threshold can be refunded only once the manager approves the return transaction<BR>**Forced Exchange With Manager Approval** - indicates that any amount which exceeds the specified threshold can only be exchanged for other items. However, the forced exchange restriction can be overridden when approved by a manager.<BR>**Allow** - indicates that any amount which exceeds the specified threshold can be refunded to the customer.<BR>**Forced Exchanged** - indicates that any amount which exceeds the specified threshold can only be exchanged for other items.|
|Message|The message displayed when the return transaction amount exceeds the threshold. For example, if the action selected is Forced Exchange, and the return amount exceeds the threshold, the system prompts the following message at the POS terminal:  The customer must exchange the item. The Return amount is  < with the rules threshold>.<BR>A message is only prompted once in a return transaction.|
|Allowed Roles|The roles that must be assigned to a user, to enable the user to authorize a return which requires manager approval. More than one role can be applied.|

### Restrictions Tab

The Restrictions tab is used to define the rules and actions which restrict item returns. Restrictions are applied using specific attributes and conditions, which when met trigger a specific action.

The rules are validated upon each return according to the order they are defined in the Restrictions tab. Once a rule is met, the validation stops and the action for that rule is executed.

**Note:** This option is not relevant to Gift Receipt Return Policies. 

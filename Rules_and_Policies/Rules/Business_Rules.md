## Business Rules

**Business Rules** define rules and restrictions which are linked to messages that are triggered by various actions and/or conditions at any touchpoint. Business rules are based on the store's policies and rules.

Business Rules can be defined for a specific store or touchpoint, or applied to all stores and all touchpoints in the hierarchy, etc.

The rules can be set up according to their specific attributes, and/or according to a range of generic conditions that are relevant to the type of business rule selected.

To be able to set up specific business rules, you need to understand the business. Future versions of this guide will include a range of 'How To's to guide users on defining business rules based on different retail business activities.

The following Business Rules are supported:

* Batch/Lot Number
* Batch Order
* Cash Office Adjustments
* Coupon
* Coupon Limits
* Coupon Override
* Finalize Transaction
* Gift Card Reward Voided
* Manual Input
* Open Price
* Payment
* POS Function
* Price Override
* Price Verify
* Product/Department
* Quantitative Limit
* Recall Transaction
* Remove Loyalty Card
* Suspend Transaction
* Switch Loyalty Card
* Tender Exchange
* Total Transaction
* Transaction Begin
* Unavailable Items
* Unknown Coupon
* Unused Coupon
* Void Item
* Void Tab
* Void Transaction

The Business Rule module includes:

* **Location Conditions** – trigger messages in a specific store.
* **Touchpoint Group Conditions** – trigger messages targeted at specific touchpoint groups.
* **Product Conditions** – trigger messages when selling a product with specific characteristics, e.g., prompt the cashier with information when a certain number of a particular group of products is sold, or trigger a message if the cashier scans an item with a past expiry date.
* **Payment Conditions – trigger messages when accepting tenders of a specific type, e.g., if you wish to prevent a customer paying a cash amount of more than $1000.00, and the cashier tenders more than the specified amount, a message can be prompted when that limit is exceeded.
* **Tender Conditions** - trigger messages when a cash office activity is adjusted, e.g., If you want to prohibit adjusting the cash tender in declarations.
* **Customer Order Conditions** – trigger messages during transactions which have not yet been completed.
* **Reason Conditions** – trigger a message when a specific reason code is selected at a touchpoint, e.g., prompt the cashier to request manager approval when the cashier overrides an item price and selects damaged as the reason code.
* **Coupon Conditions** – define a rule for a certain group of coupons based on the coupon series the coupons are linked to, e.g., if you want to prevent the cashier from overriding the face value of coupons in a specific coupon series by more than $10.00.
* **System Environment Conditions** – to trigger messages when the store server is offline, e.g., if you want to prevent the cashier from recalling saved transactions while the server is offline.
* **Role Conditions** - to prohibit users with permissions to adjust specific cash office activities from adjusting a specific cash office activity by role in a BRM.
* **Batch Order Conditions** – trigger messages when a QR Code is scanned in a transaction, for example, to prevent the cashier from voiding a single item in a QR Code.

**Reference Path:** *Rules & Policies/Rules/Business Rules*

![Business Rules Screen](/Images/BusinessRulesScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Name**|The name of the business rule. For example, Deny a 20% threshold for Price Overrides.|
|**Type**|The type of business rule. Each type represents an activity performed on a touchpoint.|
|**Location**|

**Reference Path:** *Rules & Policies/Rules /Business Rules/Add New*

![Business Rules Form](/Images/BusinessRulesForm.png)

|**Field**|**Description**|
|---------|----------|
|**Name**|The name of the business rule.|
|**Type**|The list of business rule types that can be defined. Each type represents an activity performed on a touchpoint.|
|**Conditions tab**|Displays the rules and attributes used to create a Business Rule. Rules are a collection of conditions which evaluate the business activity.<BR>On selecting the Type of business activity, the properties relevant to that type of business activity are displayed, and in addition, the default areas are displayed. See also: Conditions Tab.|
|**Action tab**|Defines the actions applied once the business rule is triggered. Actions refer to the actual actions triggered by the system which must be acknowledged or handled according to screen instructions. See also: Action Tab.|

### Business Rule Types

The Conditions tab is used to define the selected rule criteria with which you are defining the business rules. Conditions can be defined per line or transaction during a sale. For example, a sale may include 10 lines. Each line represents an item sold. A rule may apply to one line or the whole transaction.

Rules are a collection of conditions, which evaluate an activity, and if met, trigger the linked action.

**Note:** The Location Condition, Touchpoint Group Condition, System Environment Condition, Product Condition, Payment Condition, Customer Order Condition, Reason Condition, and Coupon Condition criteria are displayed according to the selected Types. See also: Generic Rule Conditions.

The following Business Rule Types are supported.

|**Business Rule Type**|**Description**|**Attributes**|
|---------|----------|-------------|
|**Batch/Lot Number**|To define a rule to limit the selling of products with specific batch/lot numbers to prevent selling products from a specific batch that are locked for sale and are recalled.<BR>For example, prohibit the sale of baby food from batch 123.|**Batch/Lot Number** – The options are:<BR>**Is equal to (=)**  Prohibit the sale if the item batch # matches the Value.<BR>**Is in (List)**  Prohibit the sale if the item batch # is one of the listed Values.<BR>**Is not equal to (<>)** Prohibit the sale if the batch # is not in the Value field.<BR>**Is not in (List)** Prohibit the sale if the item batch # is not in the Value field.<BR>**Contains** – Prohibit the sale if the batch # includes the Value field entry.<BR>**Does Not Contain** – Prohibit the sale if the item batch # does not include the Value field entry.<BR>**Value** – The batch/lot number. This is a free text field. Baby food from batch 123 must be recalled and is prohibited for sale.|
|**Batch Order**|To evaluate the maximum number of QR Codes of a certain type that can be scanned in the transaction.|**Batch Order Type** – currently only QR Code is supported.<BR>**Batch Order Label** – the label name used to differentiate between batches of the same type. (For example: pharma and Deli). If this field is empty, the Max Order Quantity value is applied to QR Codes of any type.<BR>**Apply only if QR Code not first in ticket** – specifies if the QR Code can be added to the ticket at any stage in the transaction with no action applied.<br>If not selected, the QR Code can only be added to the ticket as the first item, i.e., scanned from No Sale Mode.<BR>**Max Order Quantity** – the maximum number of QR Codes of a certain type that can be scanned in the transaction, for example, only allow one QR code to be scanned per transaction. An empty field indicates no limitation.|
|**Cash Office Adjustments**|To evaluate if a specific Cash Office activity can be adjusted or not. When the rule is selected and applied to a Cash Office activity, the selected activity cannot be adjusted. The rule can be applied to more than one Cash Office activity.|**Adjustment Activities** – The options are:<BR><BR>Tender Loan<BR>Open Loan<BR>Paid Out<BR>Paid In<BR>Bank Receipt<BR>Bank Deposit<BR>Safe Transfer<BR>Tender Pickup<BR>System Pickup<BR><BR>**Note:** Currently, only the Prohibit action is supported.|
|**Coupon**|To evaluate if a coupon did not trigger a promotion. For example, when a coupon is scanned and other conditions defined in the promotion are not met, or the promotion was suspended or expired, and as a result the promotion is not triggered.<BR>Or<BR>The coupon value was not totally rewarded. For example, when a $5.00 coupon is scanned and the total amount of items purchased is $4.00. Since the customer cannot receive a reward for more than the transaction amount, only a partial amount of the full coupon reward of $5.00 is issued.|**Rule Applies to** – the option the rule is applied to. The options are:<BR><BR>Promotion Not Triggered – to specify if the rule is triggered when a scanned coupon did not trigger a promotion<BR><BR>Partial Reward – to specify the rule is triggered when only part of the coupon amount is rewarded<BR><BR>Promotion Not Associated – to specify the is triggered when the coupon is not associated to a promotion.|
|**Coupon limits**|





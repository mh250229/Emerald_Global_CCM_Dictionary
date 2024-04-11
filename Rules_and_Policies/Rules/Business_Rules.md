## Business Rules

**Business Rules** define rules and restrictions which are linked to messages that are triggered by various actions and/or conditions at any touchpoint. Business rules are based on the store's policies and rules.

Business Rules can be defined for a specific store or touchpoint, or applied to all stores and all touchpoints in the hierarchy, etc.

The rules can be set up according to their specific attributes, and/or according to a range of generic conditions that are relevant to the type of business rule selected.

To be able to set up specific business rules, you need to understand the business. Future versions of this guide will include a range of 'How To's to guide users on defining business rules based on different retail business activities.

The following Business Rules are supported:

* Batch or lot Number
* Batch Order
* Cash Office Adjustments
* Coupon
* Coupon Limits
* Coupon Override
* Finalize Transaction
* Gift Card Reward Voided
* Manual Input
* Open Price
* Pay By Points
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
* **Partial Payment  Condition** – to prohibit voiding/adding items in a transaction that were partially paid for with a specific tender

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
|**Conditions tab**|Displays the rules and attributes used to create a Business Rule. Rules are a collection of conditions which evaluate the business activity.<BR>On selecting the Type of business activity, the properties relevant to that type of business activity are displayed, and in addition, the default areas are displayed. See also: [Conditions Tab](<../../Rules_and_Policies/Rules/Conditions Tab.md/Conditions Tab.md>)|
|**Action tab**|Defines the actions applied once the business rule is triggered. Actions refer to the actual actions triggered by the system which must be acknowledged or handled according to screen instructions. See also: [Action Tab](<../../Rules_and_Policies/Rules/Action Tab.md/Action Tab.md>)|
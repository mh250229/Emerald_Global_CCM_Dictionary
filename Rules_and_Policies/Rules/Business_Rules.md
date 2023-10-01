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
|**Conditions tab**|Displays the rules and attributes used to create a Business Rule. Rules are a collection of conditions which evaluate the business activity.<BR>On selecting the Type of business activity, the properties relevant to that type of business activity are displayed, and in addition, the default areas are displayed. See also: Conditions Tab.|
|**Action tab**|Defines the actions applied once the business rule is triggered. Actions refer to the actual actions triggered by the system which must be acknowledged or handled according to screen instructions. See also: Action Tab.|

### Business Rule Types

The Conditions tab is used to define the selected rule criteria with which you are defining the business rules. Conditions can be defined per line or transaction during a sale. For example, a sale may include 10 lines. Each line represents an item sold. A rule may apply to one line or the whole transaction.

Rules are a collection of conditions, which evaluate an activity, and if met, trigger the linked action.

**Note:** The Location Condition, Touchpoint Group Condition, System Environment Condition, Product Condition, Payment Condition, Customer Order Condition, Reason Condition, and Coupon Condition criteria are displayed according to the selected Types. See also: Generic Rule Conditions.

The following Business Rule Types are supported.

|**Business Rule Type**|**Description**|**Attributes**|
|---------|----------|-------------|
|**Batch or lot number**|To define a rule to limit the selling of products with specific batch/lot numbers to prevent selling products from a specific batch that are locked for sale and are recalled.<BR>For example, prohibit the sale of baby food from batch 123.|**Batch/Lot Number** – The options are:<BR><BR>**Is equal to (=)**  Prohibit the sale if the item batch # matches the Value.<BR>**Is in (List)** Prohibit the sale if the item batch # is one of the listed Values.<BR>**Is not equal to (<>)** Prohibit the sale if the batch # is not in the Value field.<BR>**Is not in (List)** Prohibit the sale if the item batch # is not in the Value field.<BR>**Contains** – Prohibit the sale if the batch # includes the Value field entry.<BR>**Does Not Contain** – Prohibit the sale if the item batch # does not include the Value field entry.<BR>**Value** – The batch/lot number. This is a free text field. Baby food from batch 123 must be recalled and is prohibited for sale.|
|**Batch Order**|To evaluate the maximum number of QR Codes of a certain type that can be scanned in the transaction.|**Batch Order Type** – currently only QR Code is supported.<BR>**Batch Order Label** – the label name used to differentiate between batches of the same type. (For example: pharma and Deli). If this field is empty, the Max Order Quantity value is applied to QR Codes of any type.<BR>To apply the BRM to one or more Batch Order Labels, in the Batch Order Labels field, click +Add New. A blank field is displayed to add each additional Batch Label. <BR>**Apply only if QR Code not first in ticket** – specifies if the QR Code can be added to the ticket at any stage in the transaction with no action applied.<BR>If not selected, the QR Code can only be added to the ticket as the first item, i.e., scanned from No Sale Mode.<BR>**Max Order Quantity** – the maximum number of QR Codes of a certain type that can be scanned in the transaction, for example, only allow one QR code to be scanned per transaction. An empty field indicates no limitation.|
|**Cash Office Adjustments**|To evaluate if a specific Cash Office activity can be adjusted or not. When the rule is selected and applied to a Cash Office activity, the selected activity cannot be adjusted. The rule can be applied to more than one Cash Office activity.|**Adjustment Activities** – The options are:<BR>Tender Loan<BR>Open Loan<BR>Paid Out<BR>Paid In<BR>Bank Receipt<BR>Bank Deposit<BR>Safe Transfer<BR>Tender Pickup<BR>System Pickup<BR>**Note:** Currently, only the Prohibit action is supported.|
|**Coupon**|To evaluate if a coupon did not trigger a promotion. For example, when a coupon is scanned and other conditions defined in the promotion are not met, or the promotion was suspended or expired, and as a result the promotion is not triggered.<BR>Or<BR>The coupon value was not totally rewarded. For example, when a $5.00 coupon is scanned and the total amount of items purchased is $4.00. Since the customer cannot receive a reward for more than the transaction amount, only a partial amount of the full coupon reward of $5.00 is issued.|**Rule Applies to** – the option the rule is applied to. The options are:<BR><BR>Promotion Not Triggered – to specify if the rule is triggered when a scanned coupon did not trigger a promotion<BR>Partial Reward – to specify the rule is triggered when only part of the coupon amount is rewarded<BR>Promotion Not Associated – to specify the is triggered when the coupon is not associated to a promotion.|
|**Coupon limits**|To evaluate if a coupon scanned in a transaction exceeds specified thresholds.<BR>Coupon limits can be defined for:<BR><BR>The total coupon reward amount, either monetary or points, issued in a transaction.<BR>The number of coupons allowed in a transaction.<BR>The reward amount manually entered by the cashier when a coupon barcode cannot be scanned or keyed in.<BR>The reward amount entered when the system prompts the cashier to enter the coupon reward.|**Limit Applies to** – The options are:<BR>**Monetary Rewards** – Limits the total monetary reward amount received from coupons in a single transaction<BR>**Points Rewards** –Limits the total points rewarded from coupons in a single transaction.<BR>**Quantity** – Limits the quantity of coupons that can be scanned in a single transaction.<BR>**Manual Coupon** – Limits the coupon amount manually entered by the cashier when the coupon barcode is not scannable or cannot be key entered. Minimum and maximum coupon amounts can be specified.<BR>**Prompt Reward** – Limits the coupon amount entered when the system prompts the cashier to enter the coupon amount. Minimum and maximum coupon amounts can be specified.|
|**Coupon override**|To evaluate if the coupon amount overridden by the cashier is within a defined threshold.<BR>This rule enables the retailer to limit the coupon amount entered by a cashier.<BR>**Coupon Price Override Direction** – The options are:<BR><BR>**Increase** - the amount up to which the coupon value can be increased<BR>**Decrease** - the amount up to which the coupon value can be decreased<BR><BR>**Coupon Price Override Change** – The options are:<BR><BR>**Percentage** – the percentage up to which the coupon amount can be changed.<BR>**Fixed** – the amount up to which the coupon amount can be changed.<BR>**Coupon Price Override Value** – the value by which the coupon was overridden.|
|**Finalize transaction**|To evaluate when a transaction is finalized (i.e., once the change calculation is performed and before the transaction slip is printed,) in order to prompt a message at the time of finalizing a transaction to remind customers regarding specific information.|There are no specific attributes.|
|**Gift card reward voided**|To evaluate when a cashier voids a promotion in which a Gift Card was issued as a reward in a promotion|There are no specific attributes.|
|**Manual Input**|To evaluate if the amount or quantity keyed in or scanned per item exceeds a defined limit. The Input limit is validated per line.|**ManualLimitType** – the limit type<BR>**QuantativeLimit** – to apply the limit to the number of items<BR>**Weight** – to apply the limit to the item weight<BR><BR>**Limit Type** – The threshold limit applied to the selected limit type<BR>**Max Value** – the maximum item amount/weight<BR>**Min Value** – the minimum item amount/weight<BR><BR>**Quantity/Weight** – The quantity/weight applied to the selected limits which if exceeded triggers the rule|
|**Open price**|To evaluate the amount added to an open price item, e.g., Gift Card or E-Topup.<BR>**Note:** The rule is triggered once the actual product price exceeds the defined min/max values, before any promotions or taxes are calculated on the product’s price.<BR>This rule can also be triggered in return transactions.|**Max Value** - the maximum amount that can be added to the item.<BR>**Min Value** – the minimum amount that can be added to the item.<BR>**Price Multiple Level Value** –the price multiples by which online items can be sold, e.g., if the Price Multiple Level Value is 5, and Min Value is $5.00, you cannot add a gift card for the price of $6.00.|
|**Pay By Points**|To evaluate transactions in which a customer wants to redeem their Loyalty points to receive a discount or pay with points, and the cashier is required to confirm the customer’s identity.|**Rule applies to Promotion ID** - the promotion ID the rule is applied to.|
|**Payment**|To evaluate the amount that can be paid with a specific tender in a sales transaction.|Trigger when payment limits are exceeded.<BR>**Limit Value** – Enter the amount that can be paid with a specific tender in a sales transaction.<BR>**Limit Type** – Options are:<BR>**Max allowed amount per ticket** – the maximum amount that can be paid with the tender for the entire transaction.<BR>**Max allowed amount per line** – the maximum amount that can be paid with the tender for a selected line in the transaction.<BR>**Min allowed amount per line** – the minimum amount that can be paid with the tender for a selected line in the transaction.<BR>**Over Tender Amount** – the maximum amount that can be over-tendered in a transaction. The limit is applied to the difference between the balance due and the amount tendered. This rule is used to limit the amount that can be given as change with a specific change tender.<BR>For example, if the over tender limit for cash is $50.00, and the change due to the customer is $80.00 in cash, the rule is triggered.<BR>**Note:** The Over Tender Amount limit is applied to the Change tender|
|**POS function**|To evaluate selected cash office and POS activities.|**Activity** – The options are:<BR><BR>**Add Tip** - when manually adding a tip to a tab.<BR>**Blind Pickup** – when money is transferred from the POS touchpoint to the safe without counting the money.<BR>**Cold Start** - when the user tries to open the Cold Start tool prior to logging in at the POS.  For example, prompt for manager approval when the user selects the Cold Start function from the Menu on the main POS screen.<BR>**Note:** Business rules are not triggered when Cold Start is run via a ColdStart.exe<BR>**Collective Tips** - when adding a cash tip transaction associated to all cashiers who worked during the working day/shift.<BR>**CTM Disable** - when the cashier selects the CTM Disable POS Function from the CTM Errors screen. Used to remove the CTM tender from the list of available tenders and block any action that requires processing with the CTM.<BR>**CTM Errors** - when the cashier selects the CTM Errors function to view CTM errors that occurred due to a technical issue, e.g., coins stuck.<BR>**CTM Ignore** - when the cashier selects the CTM Ignore POS Function from the CTM Errors screen to ignore the CTM error and return to the POS screen.<BR>**CTM OK** - when the cashier selects the CTM OK POS Function from the CTM Errors screen, for example, to acknowledge a CTM error. The button in the screen is called ‘I’ve corrected the Problem’.<BR>**CTM Popup Disable** - when the cashier selects the CTM Disable POS Function from the CTM Error pop-up screen during a sale or when moving to Tender mode to ignore the CTM error and close the pop-up screen. The button is called ‘Disable Cash Mode’.<BR>**CTM Popup Ignore** - when the cashier selects the CTM Ignore POS Function from the CTM Error pop-up screen during a sale or when moving to Tender mode to ignore the CTM error and close the error pop-up screen.<BR>**CTM Popup OK** - when the cashier selects the ‘I’ve Corrected the Problem’ from the CTM Error screen POS Function from the CTM Error pop-up screen during a sale or when moving to Tender mode to ignore the CTM error and close the error pop-up screen. The button is called ‘I’ve Corrected the Problem’.<BR>Customer Order Resumed – <BR>Customer Removing – <BR>Customer Replacing -<BR>**Department Return** - on returning items not found by a Department Return.<BR>**Department Sale** - when the cashier selects the Department Sale function to sell items not in the store catalog<BR>**Edit Tab** - when the cashier selects the Edit Tab function to update a tab. The cashier can edit the following details:<BR>Pre-authorized Card<BR>Loyalty<BR>Customer Name<BR>Table Name<BR>**EFT Tip** - when the cashier selects the Add EFT Based Tip function to add a tip with EFT.<BR>**Enter Training Mode** – on moving to Training Mode to train new cashiers.<BR>**Fiscal Reprint Last Transaction** – when reprinting the last transaction performed on the POS via the Fiscal Printer Device.<BR>**Fiscal Supervisor Application** – on launching a Fiscal Device Supervisor application. This application is an exte<BR>**Force Unlock** - when a locked touchpoint is unlocked in Secure Mode, allowing a different user to use the touchpoint.<BR>**Fuel Price Update** – when cashiers without the relevant privileges manually update fuel prices.<BR>**Fund Transfer Transaction Closing** – on completing a transaction transferring funds.<BR>**Go To CTM** - when the cashier selects the GO TO CTM POS Function from the Menu in the Hello Login screen to access the CTM devices Cash Management application.<BR>Import Tab –<BR>Import Tab Items –<BR>Item Availability -<BR>**Item Tax Exempt** – on exempting tax from an item in a transaction.<BR>**Manual Promotion** -when a promotion is manually triggered at the POS. The cashier can offer the customer a promotion, and select it manually.<BR>**Merge Transaction**- when multiple orders are merged at the POS/QSR to enable customers to pay the total amount of all their products purchased at once.<BR>**Move Tab To Venue** - when moving items from one Tab to another in the same venue.<BR>**Non Receipted Returns** - when the cashier selects the Non Receipted Return function to return items when the customer does not have a receipt.<BR>**Open Drawer** – when opening the cash drawer to add or remove cash.<BR>**Paid in** – when accepting a payment for goods and services other than sales.<BR>**Paid out** – when paying for goods and services other than sales.<BR>**Personal Tips** - when the cashier adds a cash (or any other tender) tip transactions associated to the cashier.<BR>**Price Override** – when the cashier overrides the catalog price of an item.<BR>**Recall Drive Off/Unpaid Fuel Transaction** - when the cashier recalls an Unpaid Fuel transaction, by either selecting the Recall Unpaid function or scanning a Drive Off or an Unpaid transaction barcode.<BR>**Note:** This rule applies to both Unpaid and Drive Off fuel transactions.<BR>For example, prompt for manager approval when the cashier selects the Recall Unpaid function to enable the customer to pay for fuel dispensed in a previous transaction that was not paid for as the customer forgot their credit card.<BR>**Recall Self Scan Transaction** - when the cashier recalls a transaction performed on a Self-Scan device using the ‘Scan & Go’ function<BR>**Note:** Only Self Scan transactions saved after the End of Trip barcode was scanned can be recalled.<BR>Self-Scan transactions that were recalled and later saved at the POS are displayed in the ‘Scan & Go’ list and not in the ‘Recall Transaction’ list, and the Recall Self Scan business rule can be applied to them.<BR>For example, when the cashier selects the Scan & Go function to recall a Self-Scan transaction, a business rule requiring manager approval can be prompted<BR>**Recall Transaction** - when the cashier recalls a saved transaction using the Recall Transaction function, or when the cashier scans the barcode of a suspended transaction.<BR>**Note:** This business rule is only applied to transactions that were saved using the 'Save Transaction' function, including Self Scan and Fuel transactions that were saved at the POS.<BR>**Remove Loyalty Card** – when a loyalty card is removed from a transaction.<BR>**Reprint** - when reprinting the receipt of a transaction.<BR>**Return All** - when the cashier selects the Return All function to return all items in a ticket.<BR>**Return Item** - when the cashier selects the Return Item function to return an item in a sales transaction.<BR>**Reverse Eligibility** – when the item eligibility defined for an item is reversed to enable a non-restricted item to be sold in a restricted transaction, e.g., SNAP.<BR>**Review Tips** - when the cashier selects the Review Tips function to view a summary of the total amount of tips received.<BR>**Split Tab** - when the cashier selects the Split Tab function to split a tab into two tabs either in the same venue or different venues.<BR>**Switch Loyalty card** – when a loyalty card that was scanned in a sales transaction is replaced with another loyalty card in the same transaction.<BR>**Tax Exempt** – on exempting tax on the entire transaction.<BR>**Tax Reverse** – when tax is exempted in a transaction by mistake and must be added to the transaction amount.<BR>**Tender Loan** – on adding money to amount in the POS drawer.<BR>**Tender Pickup** - on recording money transferred from the POS when the cash drawer is too full or at the end of a shift.<BR>**Till Closing** – on recording the money in the cash drawer at the end of a shift.<BR>**Till Declaration** – on declaring the money in the cash drawer during trading, or as part of the Till Balancing process.<BR>**Transaction Based Return** - when the cashier selects the Transaction Based Return function to return all items in a transaction with a receipt.<BR>**Walkoff** - when applying a tip to a tab in which the customer walks off without paying/closing their bill.<BR>**X Report Printing** - when printing an X Report at the POS.<BR>**Z Report Printing** - when printing a Z Report at the POS.|
|**Price override**|To evaluate if a transaction includes an item for which the price is overridden, in order to be able to prevent/allow cashiers to override an item price by a defined percentage.<BR>You cannot override the price with an amount greater than the original price. (There is a hard coded validation).<BR>**Note:** The rule is triggered once the actual product price exceeds the defined limits, before any promotions or taxes are calculated on the product’s price.<BR>This rule can also be triggered in return transactions.<BR>In a Return, the system validates the absolute value of the price and prevents the override if the cashier enters a price above or below the original price.|**Max discount (percentage)** –Triggered if the item price is overridden and decreased by a larger percentage than this.|
|**Price verify**|To evaluate if a transaction includes an item for which the price is verified, in order to be able to prevent/allow cashiers to change an item price by a defined percentage or amount.<BR>This rule can also be triggered in return transactions.<BR>**Note:** The rule is triggered once the actual product price exceeds the defined limits, before any promotions or taxes are calculated on the product’s price.|**Direction** - to specify if the item price is increased or decreased.<BR>**Change by** – to specify if the item price is changed by an amount or percentage.<BR>**Value** – the amount by which the price is changed.|
|**Product/Department**|To evaluate the sale of products during a transaction. This enables rules to be set up according to item attributes, such as the item code or the department the item is linked to.|There are no specific attributes.|
|**Quantitative limit**|To evaluate the total quantity/weight/amount of an item scanned in a transaction in order to  control the maximum or minimum quantity, weight, or amount allowed for that item.|**Aggregate on** – to specify how the sale is measured. The options are<BR><BR>**Quantity** – indicates if the total quantity purchased of the selected item/s is greater than, less than, etc. the defined Maximum or Minimum field, to trigger the rule.<BR>**Weight** – indicates that if the item weight is greater than, less than, etc. the Maximum or Minimum field, the rule is triggered.<BR>**Amount** – indicates that if the item weight is greater than, less than, etc. the Maximum or Minimum field, the rule is triggered.<BR>**Max/Min value** – Specifies if the limitation is based on the maximum or minimum amount.<BR>Max value – the maximum amount, weight, or quantity that can be sold. If exceeded, the rule is triggered.<BR>Min value – the minimum amount, weight, or quantity that can be sold. If exceeded, the rule is triggered.<BR>**Quantity** – The quantity, weight or amount value.|
|**Recall transaction**|To evaluate the time period in which a saved transaction can be recalled.<BR>**Note:** This rule type is used to define a rule based on the time period allowed to recall a transaction. If you want to define a rule to monitor recall transactions performed at the POS, for example, prompt for manager approval when a cashier recalls a transaction or prohibit a specific cashier from recalling a transaction, you must use the Recall Transaction option in the POS Function type.|**Max recall time (hours)** – the maximum number of hours a transaction can be recalled.<BR>**Limit recall for the same business day** – to indicate that only transactions saved during the same business day (i.e., before the EOD process is completed), can be recalled.<BR>If both attributes are defined, the system first checks the Max recall time (hours) attribute value, and if the rule is triggered prompts the action defined in the business rule.<BR>If the business rule is not triggered, the system then checks the Limit recall for the same business day attribute, and if the rule is triggered prompts the relevant action.<BR>If the rule is not triggered, the transaction is recalled.<BR>**Note:** One of the options must be defined when setting up the business rule.|
|**Remove loyalty card**|To evaluate transactions in which a customer's Loyalty card is scanned in a transaction and is removed in the same transaction.|There are no specific attributes.|
|**Suspend transaction**|To evaluate transactions saved at the POS terminal.<BR>This rule can also be triggered in return transactions.|**Apply only if transaction contains authorized online items** – Indicates that the rule is triggered only if authorized online items are included in the transaction.|
|**Switch loyalty card**|To evaluate transactions in which a customer's Loyalty card scanned in a transaction is switched to another Loyalty card in the same transaction.|There are no specific attributes.|
|**Tender exchange**|To evaluate transactions in which a tender is exchanged for another tender. For example, the customer has a voucher and wants to exchange it for cash or credit to their account.|**Tender Exchange Commands** – to specify the type of tender exchange transaction:<BR>The options are:<BR><BR>**Select All** – to select both Tender Exchange and Cashout<BR>**Tender Exchange** – indicates a transaction in which one tender is exchanged for another.<BR>**Cashout** – indicates a transaction in which the balance of a Gift Card is refunded.|
|**Total transaction**|To evaluate transactions at the time the POS moves from Sale mode to Tender mode.|There are no specific attributes.|
|**Transaction begin**|To evaluate transactions at the time the transaction is started.|None|
|**Unavailable item**|To evaluate if the cashier selects an item that is marked as an unavailable item.<BR>This is only relevant to QSR touchpoint functionality. Items are selected as unavailable items on the QSR POS.<BR>For example:<BR>If the cashier selects to sell an item that was declared as unavailable, e.g., a Hamburger is currently unavailable, a relevant message is prompted, e.g., 'This item is currently unavailable' and the selected item is not added to the ticket.<BR>A Kit (Item), such as a Hamburger, which always comes with a Bun, Meat, and Tomato slices by default. If one of the default ingredients was declared as unavailable, i.e., the store ran out of Tomato slices, once the cashier selects a Hamburger to sell, a relevant message is prompted, e.g., 'The following default ingredients are not available: Tomato slice, do you wish to continue?'. If 'OK' is selected, the hamburger is added to the ticket. If 'Cancel' is selected, the item is not added to the ticket.|**Apply On** -<BR>**Unavailable product (parent items or ingredient)** – To specify that the BRM will be applied once the Item (Kit/Combo/Simple Item/Ingredient) that was declared as unavailable, is selected/scanned/ keyed-in to be sold.<BR>**Note:** The recommended Action Type is Prohibit.<BR>Once the Prohibit message is prompted, when the message is confirmed, the Item is not added to the ticket, the pop up message is closed, and the QSR stays in the last screen.<BR>MA/confirmation/Notification action types are not blocked. In case any of those actions is selected and the rule is approved, the item will be added to the ticket as any item (price etc.) despite the fact it is declared as unavailable. Other action types are not supported and can cause unexpected system behavior.<BR>**Combo/Kit (parent item) with default unavailable ingredient** – to specify that the BRM will be applied once the Kit/Combo (Parent Item) with default unavailable ingredient/s was selected/scanned/ keyed-in to be sold.<BR>E.g.: A Hamburger always comes with a Bun, Meat & Tomato Slice. Tomato slice is unavailable; therefore, once the Hamburger is selected a confirmation message will be prompted. ‘Ok’ - will continue with ordering the selected item, ‘Cancel’- will cancel the selection of the item<BR>**Note:** The recommended Action Type is Confirmation<BR>Confirmation is prompted with 2 buttons: ‘OK’ and Cancel’<BR>Press ‘OK’ – Confirm the flow, pop-up is closed, QSR stays on the same screen and item is added to the ticket.<BR>Press ‘Cancel’ – cancels the selection, pop-up is closed, QSR stays on the same screen and the item is not added to the ticket.<BR>Manager Approval/Prohibit/Notification action types will not be blocked. In case any of those actions is selected and the rule is confirmed/approved, the system works according to the action. Other action types are no supported and may cause unexpected system behavior.<BR>In the 'Unavailable Items' BRM type, the following conditions are configurable:<BR>Location Condition - to define on which business unit to apply the rule.<BR>Touchpoint Group Condition - to define in which venue to apply the rule|
|**Unknown coupon**|To evaluate if there are any unused coupons in the transaction.<BR>For example, when a Loyalty Card is required before a coupon is accepted. If the Loyalty Card is scanned and then voided, the coupon cannot be accepted.<BR>Or<BR>When a customer presents a coupon and purchases an item which triggers a promotion and then decides to cancel the item. The cashier voids the item and as a result the coupon is no longer used.<BR>A rule may be configured for each coupon type.|None|
|**Unused coupon**|To evaluate if there are any unused coupons in the transaction.<BR>For example, when a Loyalty Card is required before a coupon is accepted. If the Loyalty Card is scanned and then voided, the coupon cannot be accepted.<BR>Or<BR>When a customer presents a coupon and purchases an item which triggers a promotion and then decides to cancel the item. The cashier voids the item and as a result the coupon is no longer used.<BR>A rule may be configured for each coupon type.|**Due To Activity** – the reason the coupon can no longer be used.<BR>**Remove Loyalty** – to specify if a customer's Loyalty card scanned in a transaction is voided in the same transaction..<BR>**Void Item** – to specify if an item linked to a coupon is voided in a transaction|
|**Void item**|To evaluate the items voided in a transaction.|**Limit Value** – to specify the maximum amount of voided item.<BR>**Limit Type** – to specify if the Limit Value is per item line or in the entire transaction.<BR>**Max amount per ticket** – the maximum amount that can be voided in a transaction.<BR>**Max allowed per line** – the maximum amount that can be voided in line of a transaction.|
|**Void tab**|To evaluate voided tabs|**Apply only if transaction contains authorized online item** – indicates that the rule is triggered only if authorized online items are included in the tab.|
|**Void transaction**|To evaluate voided transactions.<BR>This rule can also be triggered in return transactions.|**Apply only if transaction contains authorized online item** – indicates that the rule is triggered only if authorized online items are included in the transaction.|
|**Void Tender**|To evaluate if Supervisor Approval is prompted when a cashier voids a tender at the POS.|**Max Tender Line Amount** – to specify the maximum tender amount that can be voided without supervisor approval.|

### Generic Rule Conditions 

The **Conditions** tab is also used to configure a range of generic conditions. Rules are configured according to the type of business rule.

Based on the Type, a range of dynamic properties specific to the activity and the generic conditions relevant to the selected rule type are available. See also: Business Rule Types

The user is not obligated to define all the conditions. It depends on the business requirement.

**Reference Path:** *Sales Rules/Business Rules/ Add Business Rule*

|**Field**|**Description**|**Applied to Business Rule Types**|
|---------|----------|-------------|
|**Location Condition**|Applies a rule triggered in a specific Business Unit or store. You can specify the business units in which you want to apply a business rule, as well as the business units you want to exclude from the business rule.<BR>For example, a rule is set up to prompt a message when the customer tries to purchase more than the maximum number of pharmaceutical items, e.g., pharmacy items that require prescriptions in Store A only, or in all the stores except for Store B.<BR>![Location Condition](/Images/LocationCondition.png)|Batch or Lot Number<BR>Cash Office Adjustments<BR>Coupon<BR>Coupon Limits<BR>Coupon Override<BR>Finalize Transaction<BR>Gift Card Reward<BR>Manual Input<BR>Open Price<BR>Payment<BR>POS Function<BR>Price Override<BR>Price Verify<BR>Product/Department<BR>Quantitative Limit<BR>Recall Transaction<BR>Remove Loyalty Card<BR>Suspend Transaction<BR>Tender Exchange<BR>Total Transaction<BR>Transaction Begin<BR>Unavailable Item<BR>Unknown Coupon<BR>Unused Coupon<BR>Void Item<BR>Void Tab<BR>Void Transaction|
|Included locations|The business units in which you want to apply the rule.||
|Excluded locations|The business units in which you do not want to apply the rule.||
|**Touchpoint Group Condition**|Specifies the touchpoint group the business rule is applied to as well as the touchpoint groups excluded from the business rule.<BR>![Touchpoint Groups Condition](/Images/TouchpointGroupsCondition.png)|Batch or Lot Number<BR>Coupon<BR>Coupon Limits<BR>Coupon Override<BR>Finalize Transaction<BR>Gift Card Reward<BR>Manual Input<BR>Open Price<BR>Payment<BR>POS Function<BR>Price Override<BR>Price Verify<BR>Product/Department<BR>Quantitative Limit<BR>Recall Transaction<BR>Remove Loyalty Card<BR>Suspend Transaction<BR>Switch Loyalty Card<BR>Tender Exchange<BR>Total Transaction<BR>Transaction Begin<BR>Unavailable Item <BR>Unknown Coupon<BR>Unused Coupon<BR>Void Item<BR>Void Tab<BR>Void Transaction|
|Touchpoint Groups are inclusive|Indicates that the business rule is applied to the selected Touchpoint Groups and Secondary Touchpoint Groups.<BR>If not selected, the rule is not applied to the selected Touchpoint Groups and Secondary Touchpoint Groups.||
|Touchpoint Groups|The touchpoint group to which the rule is applied or not depending on the Touchpoint Groups are inclusive parameter configuration||
|Secondary Touchpoint Groups|The secondary touchpoint groups to which the rule is applied or not depending on the Touchpoint Groups are inclusive parameter configuration||
|**Product Condition**|Applies rules on an item or sale of items by department, in sales transactions. The rule can be applied on the sale or return of the item in the sales transaction.<BR>For example, define a rule to prompt for manager approval if the cashier performs a department sale, or define a rule to prohibit the sale of dairy products in a department sale, etc.<BR>![Product Condition](/Images/ProductCondition.png)|Batch or Lot Number<BR>Finalize Transaction<BR>Manual Input<BR>Open Price<BR>Price Override<BR>Price Verify<BR>Product/Department<BR>Quantitative Limit<BR>Remove Loyalty Card<BR>Suspend Transaction<BR>Switch Loyalty Card<BR>Total Transaction<BR>Void Item<BR>Void Tab<BR>Void Transaction|
|Department Sale|Indicates that the business rule is applied on an item, or sale of an items by department in a sales transaction.<BR>The options are:<BR>**Item and Department Sale (Default)** - indicates that if the transaction includes a defined item or sale of an item by department, the business rule is triggered. E.g., set up a business rule that requires manager approval for department sales on the Electronics department, or Electronic items in general. If the cashier scans an electronic item, the business rule will trigger, and if the cashier tries to sell an item via the Electronic department the business rule triggers.<BR>**Department Sale** -indicates that if an item is sold by a specific department or any department, the business rule is triggered. E.g., set up a business rule that requires manager approval for department sales on the Electronics department. If the cashier tries to sell an item via the Electronic department the business rule triggers.<BR>**Item Sale** - indicates that if the transaction includes a specific item or any item, the business rule is triggered. E.g., set up a business rule that requires manager approval for sales of Electronic items in general. If the cashier scans an electronic item, the business rule will trigger.||
|Return Item|Indicates that the business rule is applied to returned items.<BR>The options are:<BR>**Sale and Return Item** – indicates that if an item or item within a selected department is sold or returned in a sales transaction, the rule is triggered.<BR>**Return Item** - indicates that if an item or item within a selected department is returned the rule is triggered.<BR>**Sale Item Only** - indicates that if an item or item within a selected department is sold in a sales transaction, the rule is triggered.||
|Included Products|To select the products, categories, product groups and departments the Business Rule is applied to.<BR>The options are:<BR>**Groups** - the Product Groups the rule is applied to.<BR>**Categories** – the item category the rule is applied to<BR>**Products** - the product the rule is applied to.||
|Excluded Products|To select the products, categories, product groups and departments the Business Rule is not applied to.<BR>The options are:<BR>**Groups** - the Product Groups the rule is not applied to.<BR>**Categories** – the item category the rule is not applied to<BR>**Products** - the product the rule is not applied to.||
|**Customer Order Condition**|Applies a rule to prevent or allow customer orders from exceeding a defined amount or quantity. For example, you can define a rule that prompts the cashier to call for manager approval if the customer order is over $500.00.<BR>In addition, you can configure the business rule to trigger based on whether the transaction includes a Loyalty card or not.<BR>![Customer Order Condition](/Images/CustomerOrderCondition.png)|Batch or Lot Number<BR>Finalize Transaction<BR>Manual Input<BR>Open Price<BR>Price Override<BR>Price Verify<BR>Product/Department<BR>Quantitative Limit<BR>Remove Loyalty Card<BR>Suspend Transaction<BR>Switch Loyalty Card<BR>Total Transaction<BR>Void Item<BR>Void Tab<BR>Void Transaction|
|Max Transaction Amount|The maximum amount allowed in the Customer Order, which if exceeded triggers the rule.||
|Max Transaction Quantity|The maximum quantity allowed in the Customer Order, which if exceeded triggers the rule.||
|Loyalty Card Exists|Specifies if the business rule is triggered depending if the system identifies that a loyalty card was swiped/not swiped/or both during the transaction.<BR>The options are:<BR><BR>Includes/Excludes Loyalty Card (default) - indicates that a notification is always prompted on the POS after the cashier selects the Save Transaction function during a sales transaction, regardless if a loyalty card was added to the ticket or not<BR>Includes Loyalty Card - indicates that a notification is only prompted on the POS after the cashier selects the Save Transaction function during a sales transaction if a loyalty card was added to the ticket<BR>Excludes Loyalty Card - indicates that a notification is only prompted on the POS after the cashier selects the Save Transaction function during a sales transaction if a loyalty card was not added to the ticket||
|Excludes Loyalty Card|indicates that a notification is only prompted on the POS after the cashier selects the Save Transaction function during a sales transaction if a loyalty card was not added to the ticket||
|**Reason Condition**|Applies a rule which is triggered when a specific Reason Code type is selected at the POS.<BR>For example, the customer purchases a CD and the package is broken. The customer asks the cashier to discount the item price as the CD is damaged. The cashier overrides the price of the CD. If the price is overridden by more than the defined amount, a rule is triggered to prompt the cashier to enter a Reason Code. The cashier selects a reason, e.g., Damaged, from the Reason Codes list, and the system triggers another rule prompting for Manager Approval.<BR>![Reason Condition](/Images/ReasonCondition.png)|Batch or Lot Number<BR>Finalize Transaction<BR>Manual Input<BR>Open Price<BR>Price Override<BR>Price Verify<BR>Product/Department<BR>Quantitative Limit<BR>Total Transaction<BR>Remove Loyalty Card<BR>Suspend Transaction<BR>Switch Loyalty Card<BR>Void Item||
|Reason|The selected reason codes linked to the business rule.||
|**Role Condition**|Applies a rule to prohibit users with permissions from performing the action assigned to the BRM.<BR>If one of the Business Rule is triggered, and the user is assigned to a Role selected in the Role condition, the user is restricted from performing the activity assigned to the Business Rule.<BR>If a Business Rule is triggered and no Role is assigned in the Role Condition or all the available roles are selected, no user can perform the activity assigned to the Business Rule.<BR>For example, prohibit the cash officer who has the Monetary Adjustment permissions enabled in their role, from performing a pickup adjustment.<BR>If the user is not assigned to the Monetary adjustment activity role action, the user cannot perform ANY adjustment regardless of the BRM configuration.<BR>If the user does have the Monetary adjustment activity role action, i.e., is assigned to it, and a BRM is configured and assigned to the user's role, then the BRM is validated during a transaction.  The user will be restricted from adjusting the activity assigned to the BRM.<BR>If the BRM is configured, and not assigned to any role, no user can adjust the selected activities.<BR>![Role Condition](/Images/RoleCondition.png)|Cash Office Adjustments<BR>Price Override<BR>Quantitative limit<BR>Item Void<BR>Transaction Void|
|Role|The selected roles prohibited from adjusting a Cash Office Activity. Users assigned to the selected role cannot adjust the selected Cash Office Activity.||
|**Tender Condition**|Defines a Cash Office Adjustment rule for a specific tender. For example, prohibit adjusting the amount recorded in a Tender Pickup for cash. You can select one or more tenders and on trying to adjust a cash office activity with one of the defined tenders, the prohibit message is prompted.<BR>![Tender Condition](/Images/TenderCondition.png)|Cash Office Adjustments|
|Tender|The tender types applied to the business rule. The same business rule can be applied to more than one tender.|
|**Coupon Condition**|Defines rules for groups of coupons based on the Coupon Series ID or coupon type in order to prompt for additional cashier validation. A coupon series is a range of coupons based on defined attributes, which can be controlled centrally.<BR>Different coupon rules can be defined for different Coupon Series IDs and types, as well as the action required when certain coupons are scanned, e.g., inform the cashier, prompt for confirmation, request manager approval, etc.<BR>For example, you can define a rule for unknown coupons, i.e. coupons not found in the coupon repository. If the cashier scans an unknown coupon at a touchpoint, a message can be triggered to request additional validation.<BR>![Coupon Condition](/Images/CouponCondition.png)|Coupon<BR>Coupon Limits<BR>Coupon Override<BR>Unknown Coupon<BR>Unused Coupon|
|Apply to Coupon Series/ Coupon Type|Specifies if the business rule is applied to a coupon type or series.<BR>The options are:<BR>**Series ID** – a range of coupons based on defined attributes that can be controlled centrally. If selected, the Coupon Series field is enabled, and you can select the Coupon series you want to apply the business rule to.<BR>**Coupon Types** – a specific coupon type, e.g., UPC5, Store, Databar and so on. If selected, the Coupon Type field is enabled, and you can select the coupon you want to apply the business rule to.||
|Coupon Series|	The ID of the Coupon Series the business rule is applied to. One or more coupon series can be selected.<BR>This field is enabled only when Series ID is selected from the Apply to Coupon Series/Coupon Type drop-down list.||
|Coupon Type|The Coupon type the business rule is applied to. One or more coupon types can be selected.<BR>The following coupon types can be selected:<BR>UPC5 – vendor coupons in which the coupon reward is based on the UPC Coupon Value Code.<BR>DataBar – coupons based on the GS1 DataBar™ symbols, and provide retailers with more options and control over the information in the barcode than the EAN/UPC barcode.<BR>Manual – coupons for which the reward amount is entered manually by the cashier.<BR>Store – coupons that are valid only at a particular store and are usually distributed in the store in which they will be honored.<BR>This field is enabled only when Coupon Type is selected from the Apply to Coupon Series/Coupon Type drop-down list.||
|**Payment Condition**|Applies a rule to a specific tender used to pay for items in a transaction.<BR>For example, a rule is defined to specify that the Cash tender must be used to pay for cigarettes.<BR>![Payment Condition](/Images/PaymentCondition.png)|Finalize Transaction<BR>Payment|
|Tender|The tender types applied to the business rule. The same business rule can be applied to more than one tender.||
|Entry Method|The method used to add the tender, e.g., manually enter an EFT card, swipe the card, etc.<BR>The options are:<BR>Smart Card<BR>MICR<BR>MSR<BR>Keyed<BR>Scanned<BR>Weighed<BR>Measured<BR>RFID<BR>Automatic<BR>Integrated Chip Card<BR>Tapped<BR>Waved|
|**System Environment Condition**|Applies a rule which is triggered when the store server is offline. A server is offline when there is no communication between the DMS Agents, i.e., the parent server did not get a preconfigured number of heartbeats from the child node.<BR>For example, you can define a rule to prevent cashiers from recalling a saved transaction when the POS is offline to its parent server (Store or HQ server). This prevents customers, for example, from receiving a reward more than once, since when the system is offline, the cashier cannot verify if the customer previously received a reward or not.<BR>The Business Rule is configured and this condition is set with Store Server is Offline to Yes.<BR>Scenario:<BR>The cashier tries to recall a saved transaction while the POS is offline to the Store server. A message is prompted notifying the cashier that the transaction cannot be recalled as the server is offline.<BR>![System Environment Condition](/Images/SystemEnvironmentCondition.png)|Recall Transaction|
|Store Server is offline|Indicates that the business rule is applied when the store server is offline. For example, prohibit recalling transactions when the store server is offline.<BR><BR>If selected:<BR><BR>if the POS is offline from its parent server (Store Server or HQ) according to the deployment, the Business Rule is triggered<BR>If the POS is offline from its parent server (Store Server), but online to the HQ server, the Business Rule is triggered<BR>If the POS is online to both, the Business Rule is not triggered.<BR><BR>If not selected:<BR><BR>If the POS is offline from its parent server (Store Server or HQ) according to the deployment, the Business Rule is not triggered<BR>If the POS is offline from its parent server (Store Server), but online to the HQ server, the Business Rule is not triggered||
|**Batch Order Condition**|Applies a rule to a specific QR Code.<BR>For example, a rule is defined to specify that specific items in a QR Code cannot be voided.<BR>![Batch Order Condition](/Images/BatchOrderCondition.png)|Price Override<BR>Void Item<BR>Void Transaction|
|Batch Order Type|Currently only QR Code is supported.||
|Batch Order Label|The label used to differentiate between batches of the same type, for example pharma and Deli.||
|**Batch Combination**|Applies a rule to define which batch label combination will trigger the BRM. You can use it to prevent specific QR Codes from being sold in the same transaction.<BR>![Batch Combination Condition](/Images/BatchCombinationCondition.png)<BR>The options are:<BR>**Batch Order Type** – includes all the batch order types, currently QR Code.<BR>**Batch Order Label** – a free text field to enter which Batch orders combination will trigger the  action of the BRM defined. This field is only enabled once the Batch Order Type field is selected.<BR>**For example:**<BR>If the following BRM is defined:<BR>BRM Type – Batch Order<BR>Batch Order Type – QR Code<BR>Batch Order Label - PH<BR>Batch Combination Condition:<BR>Batch Order Type: QR Code<BR>Batch Order Label – FO.<BR>Action – Prohibit (Message: Action Prohibited).<BR><BR>If the cashier scans the QR Code of type PH, and then scans another QR Code of type FO. The BRM is triggered and the POS prompts: Action Prohibited.|Batch Order|
| **Partial Payment Condition**|Applies a rule to prohibit voiding/adding items in a transaction that were partially paid for with a specific tender.<BR>![Partial Payment Condition Screen](/Images/partialpaymentcondition.png)|Product / Department<br>Void Item|


### Action Tab

The Action Tab defines the action taken when a business rule is triggered. A message is always displayed, and additional user or cashier action may be necessary. 

**Reference Path:** *Rules & Policies/Rules/Business Rules/Add New/ Action Tab*

![Action Tab](/Images/ActionTab.png)

The following Action types are supported:

* Member Validation
* Prohibit
* Approval required
* Select reason
* Enter loyalty card
* Prompt for confirmation
* Form
* Input date required
* Notification

#### Action Types

##### Member Validation

The Member Validation action is used to validate Loyalty members who request to pay or partially pay for their transaction with ‘Points’.
The Member Validation action type is used for the payment BRM.

![Member Validation](/Images/MemberValidation.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g., Member Validation|
|**Message**|The message prompting the customer/cashier that the action is prohibited.|
|**Scope**|Defines how often the business rule can be triggered. The options are:<BR>**Request** - indicates that the business rule is always triggered.<BR>**Transaction** - indicates that the business rule is only triggered once per transaction.|
|**Input Label**|Defines the text title above the message input fields. For example, if a Date is selected from the Input Type drop-down list, and the cashier is required to enter the date of birth for a customer, the input label may be: Enter the date (DD/MM/YYYY).|
|**Validate By**|Specifies how the loyalty member validated. The options are:<BR>Date of Birth<BR>4 last digits of ID|
|**On Self Checkout**|Specifies how the Business Rule/Intervention is handled on the Self Checkout.<BR>The options are:<BR>**Requires attendant** - indicates that an attendant is required to resolve the intervention.<BR>**Triggered as delayed** – indicates if the intervention is handled immediately or is delayed so that the attendant can handle the intervention anytime during the transaction.<BR>If selected, the intervention is delayed and the shopper can continue shopping. Once the shopper finishes scanning their items and selects the Finish & Pay button, and the attendant has not yet handled the intervention, it then becomes an immediate intervention and the required action must be performed by the attendant to clear the intervention .<BR>If not selected, the intervention must be handled immediately. The shopper cannot continue shopping until the intervention is resolved.|

##### Prohibit

The **Prohibit** Action Type restricts certain items, or groups of items from being sold on a specific touchpoint, or prevent specific functions, etc. which are part of a business rule.  

![Prohibit](/Images/Prohibit.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g., Prohibit|
|**Message**|The message prompting the customer/cashier that the action is prohibited.|
|**On Self Checkout**|Specifies how the Business Rule/Intervention is handled on the Self Checkout.<BR>The options are:<BR>**Requires attendant** - indicates that an attendant is required to resolve the intervention.<BR>**Triggered as delayed** – indicates if the intervention is handled immediately or is delayed so that the attendant can handle the intervention anytime during the transaction.<BR>If selected, the intervention is delayed and the shopper can continue shopping. Once the shopper finishes scanning their items and selects the Finish & Pay button, and the attendant has not yet handled the intervention, it then becomes an immediate intervention and the required action must be performed by the attendant to clear the intervention.<BR>If not selected, the intervention must be handled immediately. The shopper cannot continue shopping until the intervention is resolved.|

##### Approval Required

The **Approval Required** Action Type requires the manager to approve the transaction before the cashier can continue.

![Approval Required Screen](/Images/ApprovalRequiredScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g., Approval required|
|**Message**|The message prompting the customer/cashier that the action requires supervisor/attendant/customer approval.|
|**Roles**|The role indicating the privileges required by the person who is approving the activity.|
|**Display Confirmation Message for Approved Roles**|Specifies if a confirmation message is displayed on the POS when the user logged in to the POS is assigned to one of the approved roles when the BRM is triggered. If the rule is triggered and the user logged in to the POS is not assigned to an approved role, the Approval message is prompted.|
|**Message**|The confirmation message prompted at the POS when the user logged in is assigned to one of the approved roles.|
|**Scope**|Defines how often the business rule can be triggered. The options are:<BR>**Request** - indicates that the business rule is always triggered.<BR>**Transaction** - indicates that the business rule is only triggered once per transaction.|
|**On Self Checkout**|Specifies how the Business Rule/Intervention is handled on the Self Checkout.<BR>The options are:<BR>**Requires attendant** - indicates that an attendant is required to resolve the intervention.<BR>**Triggered as delayed** – indicates if the intervention is handled immediately or is delayed so that the attendant can handle the intervention anytime during the transaction.<BR>If selected, the intervention is delayed and the shopper can continue shopping. Once the shopper finishes scanning their items and selects the Finish & Pay button, and the attendant has not yet handled the intervention, it then becomes an immediate intervention and the required action must be performed by the attendant to clear the intervention.<BR>If not selected, the intervention must be handled immediately. The shopper cannot continue shopping until the intervention is resolved.|

##### Select Reason

The **Select Reason** Action Type requires the user to select a reason the activity was performed, before continuing with the transaction.
For example, the cashier may be required to enter a reason when performing Price Overrides, Tax Exemptions, Open Drawer, and so on, at the POS.

![Select Reason Screen](/Images/SelectReasonScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g., Select reason|
|**Reason Codes**|The list of reasons from which the user can select, indicating the reason for having performed a certain activity.|
|**Scope**|Defines how often the business rule can be triggered. The options are:<BR>**Request** - indicates that the business rule is always triggered.<BR>**Transaction** - indicates that the business rule is only triggered once per transaction.|
|**Message**|The message prompting the customer/cashier that the action requires supervisor/attendant to select a reason and why.|

##### Enter Loyalty Card
The **Enter Loyalty Card** Action Type requires the requires the cashier to enter the customer's loyalty card information.

![Enter Loyalty Card Screen](/Images/EnterLoyaltyCardScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g., Enter Loyalty Card|
|**Message**|The message prompting the cashier to enter the Loyalty card details|
|**Scope**|Defines how often the business rule can be triggered. The options are:<BR>**Request** - indicates that the business rule is always triggered.<BR>**Transaction** - indicates that the business rule is only triggered once per transaction.|


##### Prompt For Confirmation

The **Prompt For Confirmation** Action Type requires the user to confirm the message by selecting Yes or No before continuing with the transaction.

![Prompt For Confirmation Screen](/Images/PromptForConfirmationScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g., Prompt for Confirmation|
|**Message**|The message prompted to inform the cashier that confirmation is required.|
|**Scope**|Defines how often the business rule can be triggered. The options are:<BR>**Request** - indicates that the business rule is always triggered.<BR>**Transaction** - indicates that the business rule is only triggered once per transaction.|

##### Form

The **Form** Action Type requires the cashier to select a form and enter the relevant information.

![Form Screen](/Images/FormScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g. Form|
|**Form Name**|The form displayed when the business rule is triggered. This field is mandatory. All the forms are predefined forms defined by the retailer.<br>The options are:<br>**Customer Data** - to prompt a form that includes fields to enter  the Customer name and Customer phone number<br>**Table Number** - to prompt a form that includes a field to enter the table number.<br>**Configurable Form** – to prompt a form that was configured by the retailer with their own retailer data. It provides 3 fields, 2 of which are mandatory when this form is used. This configuration can be changed.|
|**Scope**|Defines how often the business rule can be triggered. The options are:<br>**Request** - indicates that the business rule is always triggered.<br>**Transaction** - indicates that the business rule is only triggered once per transaction.|

##### Input Data Required

The **Input Data Required** Action Type requires the user to enter information in order to continue with the transaction.

![Input Data Required Screen](/Images/InputDataRequiredScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g., Input Data Required|
**Message**|The message prompting the customer/cashier that the action requires input.|
|**Scope**|Defines how often the business rule can be triggered. The options are:<BR>**Request** - indicates that the business rule is always triggered.<BR>**Transaction** - indicates that the business rule is only triggered once per transaction.|
|**Input Label**|Defines the text title above the message input fields. For example, if a Date is selected from the Input Type drop-down list, and the cashier is required to enter the date of birth for a customer, the input label may be: Enter the date (DD/MM/YYYY).|
|**Input Name**|Defines the name of the input message fields. This is a free text field, and you can enter a name to reflect the message displayed. For example, if a Date is selected from the Input Type drop-down list, and the cashier is required to enter the date of birth for a customer, the input name may be: Customer's Birthday|
|**Input Type**|Allows the user to enter data when a message linked to this option is triggered. The user can select the type of data they plan to enter when the message is triggered: The options are: Text, Numeric, Yes/No, Date, Birthday|
|**Max Time Period**|The maximum duration period during which online items can be activated, calculated from the current date. The cashier is able to activate an item with an activation date any time from the starting day until the maximum defined date.|
|**Time Period**|The time period is defined for either days or months.|

##### Notification

The **Notification** Action Type prompts a message informing the user but enables the user to continue with the transaction.

![Notification Screen](/Images/NotificationScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g., Notification|
|**Message**|The message prompted to notify the cashier.|
|**Scope**|Defines how often the business rule can be triggered. The options are:<BR>**Request** - indicates that the business rule is always triggered.<BR>**Transaction** - indicates that the business rule is only triggered once per transaction.|

##### Enter Salesperson

The **Enter Salesperson** Action Type prompts the cashier to scan the salesperson’s barcode when adding a salesperson to the transaction.

Salespersons are employees who help customer purchases items. Retailers can reward the salesperson with a sales commission.

![Enter Salesperson Screen](/Images/EnterSalespersonScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g., Enter Salesperson|
|**Message**|The message prompted to notify the cashier to scan the Salesperson’s barcode.|
|**Scope**|Defines how often the business rule can be triggered. The options are:<BR>**Request** - indicates that the business rule is always triggered.<BR>**Transaction** - indicates that the business rule is only triggered once per transaction.<BR>**Note:** The Scope field only defines the number of times the BRM is triggered in the transaction. If Scope is set to Transaction, the salesperson is only linked to the first item scanned in the transaction that triggered the BRM and not to all the items in the ticket.|
|**Mandatory**|If selected, the cashier must scan or enter the Salesperson’s barcode in the message screen prompted when the BRM is triggered. The items cannot be sold until the cashier adds the salesperson.<BR>An error message is prompted if the cashier closes the message screen without scanning the salesperson’s barcode or enters an invalid salesperson.<BR>If not selected, the cashier can close the message screen without scanning the salesperson’s barcode, and the item is not sold.|
## Roles

**Roles** sets up the user roles (job types) in the system, for example, Administrator, Cashier, Cash Officer, and so on. Roles are based on the available roles in the business.

Every role can be assigned role actions. When creating Roles you can define the roles actions to which each role has access, and specify the activities that can be performed by each role action.

For example:

A Role can be created for the Supervisor and another role for a Cash Officer. You can specify that the Supervisor can perform all the Cash Office actions, Sales and Return transactions as well as change, or reset a user’s password. While the Cash Officer can only perform Bank Deposits and Safe Declarations.

Once the Roles are defined, you can associate users to the Roles.

**Reference Path:** *Organization/Security/Roles*

![Roles Screen](/Images/RolesScreen.png)

|**Field**|**Description**|
|---------|----------|
|**ID**|The ID of the defined role.|
|**Name**|The role name, such as Cashier, Store Manager etc.|

**Reference Path:** *Organization/Security/Roles/Add New*

![Role Form](/Images/RoleForm.png)

|**Field**|**Description**|
|---------|----------|
|ID|The Role ID.|
|Name|The name of the defined role, such as Cashier, Store Manager etc.|
|Touchpoint Groups|The touchpoint group linked to the Role. Users assigned to the Role can perform the linked actions only on touchpoints in the selected touchpoint group.|
|Available actions (X/Y)|The available actions that can be assigned to a role. Each drawer represents an action and contains only the sub-actions that can be performed by a user.|

### Role Actions

The actions that can be selected and applied to a Role. The actions define the activities that can be performed by users assigned to each role. Users assigned to a Role have permissions to perform only those actions linked to the Role.

|**Module**|**Action**|**Description**|
|---------|----------|-------------|
|Age Restriction Rule|Configure|To configure restrictions based on the date and time items are sold, the customers age, or the user's age.|
|Alert|Alert Delete or Update|To delete or modify alert templates used to identify alerts manually triggered at the POS.|
|Auto Load|Configure|To configure the Auto Load functionality on the POS.|
|Branding Images|Configure|To enable users to upload images to display on the screens on the Cashier and Customer Displays.|
|Business Rule|Configure|To define rules and restrictions that are triggered by various actions and/or conditions at any touchpoint.|
|Cash Office|Add Coins to ATM|To enable users to add money in the ATM at the Self Checkout to ensure there is cash available to give change to the customer if required.|
||Approve Pay In Out Exceeding Threshold|To enable users to approve Paid In or Paid Out amounts which exceed the limit defined in the system configuration.|
||Balancing Threshold Override|To enable users to override the maximum amount allowed for cash office activities.|
||Bank Deposit|To enable users to deposit money into the store bank account.|
||Bank Receipt|Withdraw money from the store's bank account and transfer the money to the safes.|
||Blind Pickup|To enable users to collect money in the touchpoint's cash drawer and transfer the cash to the safe without counting the cash amount.|
||Cash Drawer Limit Configuration|To enable users to define the maximum cash amount allowed in the Cash Drawer. Once the limit is exceeded, a Tender Pickup is performed.|
|	Cashier Balancing	To enable users to balance the cashier accounts in a business period.
	Cashier Declaration	To enable users to declare all the money in the cashier drawer. 
	Cashier Settlement	To enable users to settle the cashier accounts once the amounts recorded in each account in a business period are approved.
	Configure Opening Funds	To enable users to define the cash amount in the cash drawer at the start of each business day.
	Go To CTM	To enable users to access the Cash Tender Module (CTM) Cash Management Application used to provide automated cash tendering at assisted lanes. During a transaction, notes and coins are inserted into the recycler device and change is distributed from the recycler units. 
For example, during a sale, if the CTM runs out of cash, the cashier selects the GoToCTM command and can add cash to refill the chute.
	Monetary Adjustment	To enable users to adjust the amounts recorded in cash office activities such as Tender Pickup, Paid In, Paid Out, in order to correct any discrepancies before approving the amounts recorded for the activity.
	No Sale	To enable users to 0pen the cash drawer in No Sale mode.
	Paid In	To enable users to perform a Paid in transaction, in which money is accepted at a touchpoint for services other than sales.
	Paid Out	To enable users to perform a Paid Out transaction, in which money is paid at a touchpoint for services other than sales.
	Safe Balancing	To enable users to balance the store safe accounts in a business period.
	Safe Settlement	To enable users to settle the safe accounts once the amounts recorded in each account in a business period are approved.
	Safe Transfer	To enable users to transfer money form one safe to another.
	Tender Loan	To enable users to transfer money from the safe to a touchpoint, e.g., POS, to add money to the cash drawer.
	Tender Pickup	To enable users to pick up money from the POS terminal and record it in the system, for example, at the end of a shift or to prevent excessive amounts of money accumulating in the cash drawer during trading.
	Till Balancing	To enable users to approve a pending business period, once the accounts in the business period are balanced or any over/short amounts are approved.
	Till Closing	To enable users to close the Till at the end of a shift to record the amount received during the shift at the Till. The amount is recorded in the business period when balancing the business period.
	Till Declaration	To enable users to declare all the money in the drawer at the Till.
	Till Settlement	To enable users to settle an approved till business period. Business periods are settled after all the accounts are balanced or approved. Once settled, the till accounts cannot be modified.
	View Audit	To enable users to view the cash office activities performed in a specific store, during a defined date, and then drill down to view the details of each activity.
	X Report	To enable cashiers to print an X Report.
	Z Report	To enable cashiers to print an Z Report.
Coupon	Configure	To enable users to set up a coupon series.
Data Pattern	Configure	To define data patterns used to identify any input accepted at a touchpoint, (e.g., a POS terminal, by scanning, swiping, or keying-in alpha-numeric characters) through any POS input peripheral with a specific business entity, so that the entity related business process is activated automatically.
Device 	Configure	To enable user to set up peripheral devices required by touchpoints, e.g., printer, cash drawer, scale etc.
	Device Type Configuration	To enable user to set up the default configuration for the devices supported in the system. This configuration is applied to each device
DMS	Instrumentation Activity	
	Skip Stuck Token	To skip failed messages downloaded to the server that cannot be immediately fixed in order to synchronize the server.
E-Commerce	Picking	
End Of Day Manual	Configure	To enable users to manually postpone the EOD process.
End Of Day Schedule	Configure	To enable user to configure EOD scheduling, which specifies the weekdays and times on which EOD is executed.
Fuel (4)	Declare Drive Off	To enable users to report an unpaid fuel transaction as a Drive Off, in which the customer has fueled their car and driven off without paying
	Declare Unpaid	To enable users to report a transaction in which the customer requests to pay for the transaction at a later time. For example, when the customer forgets their wallet.
	Pump Calibration	To enable users to report a fuel transaction as a Calibration Test from the POS touchpoint.
A Calibration Test compares the flow measurement between the actual device and the formally configured standard, defined by the international bureau of weights and measures.
	Pump Test	To enable users to report a fuel transaction as a Pump Test from the POS touchpoint.
A Pump Test is a process in which the pump is tested to verify that it dispenses the correct amount of fuel or if the fuel is dispensed for lab testing.
Inventory – Product Availability 	View	
Inventory Adjustment 	Approve	
	Edit	
	View	
Inventory Order 	Approve	
	Edit	
	View	
Inventory Picklist	Edit	
	View	
Inventory Receiving	Approve	
	Edit	
	View	
Inventory Return	Approve	
	Edit	
	View	
Inventory Stock Count	Approve	
	Edit	
	View	
Inventory Transfer	Approve	
	Edit	
	View	
InventoryReportResource	Configure	
Menus Configuration 	Configure PLUGroup	To enable users to configure PLU Groups.
	Configure PLUGroup Menu	To enable users to configure PLU menus.
	Configure Tender	To enable users to configure Tender menus.
	Configure Touchpoint Commands	To enable users to configure the Command menu comprising the functions that can be used in touchpoints.
Message	Configure	To enable users to configure messages displayed when a specified action is triggered at the touchpoint.
Notification	Create Or Update	To enable users to create or update user notification messages.
	Delete	To enable users to delete user notification messages.
Online Authorization Messages	Configure	To enable users to configure online authorization messages.
Open Close Days	Configure	To enable users to configure the days the store is opened or closed.
Personal Account	Configure	To enable users to configure Personal Accounts.
	Deposit	To enable users to record money deposited by a customer into their Personal Account.
Price Approval 	Approve Price changes	To enable users to approve price changes.
Product	Configure General	To enable users to add the product details, such as the item description and sellable codes to the store catalog.
	Configure Price	To enable users to define the price of products in the store catalog.
	Configure Restriction	To enable users to apply selling restrictions to a product in the store catalog.
	Configure Store Range	To enable users to configure the stores in which products can be sold.
Promotion 	Configure	To enable users to set up promotions.
Refund Policy 	Configure	To enable users to set up the store's return policy.
Regional Settings	Culture Maintenance	To enable users to set up and apply the culture settings used in the store environment to support multi languages.
	Resources Export	To enable users to export the resource files containing a language to be translated.
	Resources Import	To enable users to import the resource files containing a translated language.
Register Touchpoint	Register	To enable users to authenticate a touchpoint and create a session between the touchpoint and the Emerald Global server. When a session is created a security token is saved encrypted in the touchpoint app.config file. The touchpoint can then be identified by the server. This is a one time procedure performed the first time the user logs in to the touchpoint.
Rescan Policy	Configure	To enable users to set up or modify the rescan policy for customers using the Self Scan device.
	View	To enable users to view the rescan policy for customers using the Self Scan device.
Retention Policy 	Execution Of Retention Policy	To enable users to run the retention policy. It is used to determine the period to keep relevant business data for specific entities.
A Retention Policy can be configured per entity and for each level in the organization (server group), for example, on the POS, history may be kept for 1 day at a time, whereas on the HQ Server, it may be kept for 24 months. 
	Save Or Update Retention Policy	To enable users to save or edit the retention policy
Return Transaction Mode 	Non Receipted Return	To enable users to perform a Non Receipted Return transaction.
	Return All	To enable users to perform a Return All transaction.
	Transaction Based Return	To enable users to perform a Transaction Based Return transaction.
Role	Configure	To enable users to configure roles applied to users.
Sales Functions 	Apply Loyalty Customer	To enable users to add a Loyalty customer to a transaction.
	Cancel Tax Discount	To enable users to cancel a Tax Discount applied in a sales transaction. Tax Rates may be preset with discounts on transactions involving qualifying individuals. For example, when alternate taxes are applied for seniors and disabled citizens.
	Coupon Add	To enable users to add coupons to the transactions.
	Department Sale	To enable users to perform a Department Sale in a sales transaction when an unknown item is scanned at the touchpoint, and the system does not recognize the item’s barcode.
	End Of Trip	To enable users to complete a transaction performed on the Self Scan by scanning the End Of Trip barcode to display the transaction at the POS touchpoint, the cashier can them accept payment and complete the transaction.
	Exempt Item Taxes	To enable users to exempt tax in a sales transaction on specific items. For example, when the customer has a tax ID number for tax exemption.
	Exempt Taxes	To enable users to exempt tax in a sales transaction in a transaction.
	Finalize Transaction	To enable users to finalize a transaction.
	Manual Coupon Add	To enable users to manually enter a coupon barcode in a sales transaction.
	Manual Promotion Add	To enable users to trigger a promotion at the POS manually. The cashier can offer the customer a promotion, and select it manually.
	Price Override	To enable users to manually override the price of an item (higher or lower than the catalog price) in a sales transaction.
	Price Query	To enable users to search for an item’s price in a sales transaction. The item can then be sold from the Price Query screen. Promotions relevant to the item are also presented
	Remove Loyalty Customer	To enable users to remove a Loyalty card from a transaction.
	Return Department	To enable users to return products that are not found in the store catalog by a department return.
	Reverse Taxes	To enable users to remove tax incorrectly applied to a product or transaction.
	Save Transaction	To enable users to save the current transaction for later recall. For example, if the customer forgets their wallet, they can request the cashier to save the transaction until they return and pay for the transaction.
	Search Item	To enable users to search for a product during a sales transaction.
	Sell Item	
	Switch Loyalty Customer	To enable users to replace a loyalty card that was scanned in a sales transaction with another loyalty card in the same transaction.
	TaxDiscount	To enable users to apply a discount on the tax applied to an item or transaction Used to apply a discount on the tax for qualifying customers, e.g., senior citizens, or special needs, etc.
	Tender Accept	
	Total Transaction	
	Update Loyalty Customer	To enable users to update the existing Loyalty customer in a transaction. For example, the cashier scans the customers Loyalty, and then the customers gives the cashier their staff discount card. The cashier scans the staff card, and the servers updates the customer with the relevant data.
	Void Item	To enable users to void an item scanned in a sales transaction.
	Void Linked Item	To enable users to void linked items in a sales transaction.
	Void Tender	To enable users to void a tender accepted as payment in a sales transaction.
	Void Transaction	To enable users to void a sales transaction before the transaction is completed.
Sales Transaction	Eat In Transaction	To enable users to perform an Eat In transaction, in which a specific tax rate is applied on items that are consumed on site.
	E-GIFT Balance Check	To enable users to query the balance of a gift card.
	Post Update Sales Transaction	
	Recall Sales Transaction	To enable users to recall a sales transaction that was previously saved.
	Reprint	To enable users to reprint a sales transaction receipt.
	WIC Transaction	To enable users to perform a WIC transaction (.Special Supplemental Nutrition Program for Women, Infants, and Children)
	WICCVV Transaction	To enable users to perform a WIC CVV transaction 
Salesperson	Add or Remove to/from Item	To enables users to add or remove a salesperson from an item added in a sales transaction.
Security 	Configure	To enable users to configure the Security Scale.
Self Scanner Monitoring 	Change Availability	To enable users to change the status of a Self Scan device to not available, for example, when the device is damaged.
	Cold Reboot	To enable users to cold reboot a Self Scan device. A cold reboot clears the entire memory of the Self Scan device. Once performed, the Self Scan application must be reinstalled.
	Release device	To enable users to manually release a Self Scan device from the cradle.
	Send message	To enable users to send a text message from a Self Scan device.
	Swap a device	To enable users to swap a device, for example, if a shopper’s device’s battery dies. An attendant at the service desk can save the transaction and give the user a different device, on which the shopper’s transaction is recalled.
	View current transaction	To enable users to view the current transaction performed on a Self Scan device, and monitor the activities of Self Scan customers currently shopping in the store.
	View customer details	To enable users to view the details of customers currently using a Self Scan device.
	Warm Reboot	To enable users to manually reboot a device whilst it is still locked in the cradle. A warm reboot clears the device's program memory. Once a reboot is completed, the device is fully operational.
SelfCheckout 	Intervention Configuration	To enable users to configure interventions prompted at the Self Checkout.
	Intervention Handling	To enable users to resolve an intervention prompted at the Self Checkout.
	Open Lane	To enable users to change a closed SCO (self check out) lane to No Sale or Sale mode.
	Security Scale Maintenance	To enable users to switch the Security Scale on and off in the stores.
Servers Hierarchy Monitoring	Remove Server	To enable users to remove a Central or store server.
Shoppers Data	Create and Delete	
	Update	
	View	
Store 	Configure	To enable users to set up stores.
	Update	To enable users to modify the details of existing stores.
Store Sales Reports	Reports – Compare Online Store Sales	
	Reports – Compare Re-Scanned transactions	To enable users to generate the Rescan Comparison Report.
	Reports – Online Store Sales	
	Reports – View store sales of business day range	
Supplier	Configure	To enable users to set up suppliers.
Tax	Configure	To enable users to set up taxes and tax authorities.
TDM Configuration	Configure	To enable users to configure the TDM.
Tender	Configure	To enable users to set up tenders.
	Search Tender	To enable users to search for specific tenders.
Tender Exchange	Configure	To enable users to specify which tenders can be exchanged for another tender.
Tender Item Restriction 	Configure	To enable users to configure tender item restrictions.
Tender Rounding Rules 	Configure	To enable users to configure rounding rules.
Touchpoint	Configure	To enable users to set up touchpoints.
Touchpoint Groups	Configure	To enable users to set up touchpoint groups.
Touchpoint Groups Additional	Configure	To enable users to create, and edit Secondary Touchpoint Groups and assign touchpoints to Secondary Touchpoint Groups.
Training Mode 	Training Mode	To enable users to move from the regular Sales mode to Training mode at the POS.
Trust Levels	Configure	To enable users to define the trust settings used to determine when a rescan is required at the Self Checkout.
	View	To enable users to view the trust settings used to determine when a rescan is required at the Self Checkout.
UPCS5	Configure	To enable users to define UPC5 codes.
User	Change Password	To enable users to change the password of other users.
	Configure	To enable users to set up other users.
	Force Sign-In	To enable users to sign in users remotely.
	Force Sign-Out	To enable users to sign out users remotely, for example, when a cashier has not signed at the end of a shift.
	Reset Password	To enable users to reset the password of other users.
	Sign-out	To enable users to log out of the system.
	View Users	To enable users to view the users defined in the system.
Venue Shift	Configure	To enable users to configure Venue Day Shifts.
Services		All the business services.


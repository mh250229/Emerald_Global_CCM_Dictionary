## Customers

**Customers** enables you to manage customers via a central customer repository (CDM – customer data management). The CDM is integrated with all Emerald Global touchpoints and allows retailers to manage identified customers. Some customers can be subscribed to loyalty while other customers can be customers that have subscribed to use a touchpoint such as a self-scan / mobile shopper / e-commerce device, etc., and are not necessarily loyalty members.

All customers must be identified via several identification options, allowing them to be recognized when using the different touchpoints. For example: presenting a loyalty card at the POS terminal, logging in with a username and password at the web portal or mobile shopper application, etc.

The retailer can set up loyalty programs, allowing the customers to accumulate different types of points, redeeming these points to get rewards, clip digital coupons, opt in to clubs according to their interests (sports club, baby club, etc.), share loyalty benefits with other household members, and more.

The main areas of functionality supported are:

* Creating, updating, and retrieving customer details at touchpoints (on the Store Manager for customer service, at the customer touchpoints, on the POS etc.).
* Manage customer subscriptions to loyalty, touchpoints, clubs, etc.
*  Manage customer accounts, allowing customers to earn and redeem points as part of promotions, or different touchpoint functions. Manage account definitions such as points expiration, resetting accounts, etc.
* Manage customer identification such as loyalty card, user name and password, identification related flows such as sign up/login/forgot password, etc.
* Manage customer households.
* Customers Segmentation.
* Manage physical and digital coupons linked to customers. Physical coupons are issued to customers and contain a barcode. Digital coupons are linked to a promotion linked to the customer, for example, by clipping the coupon.

**Note:** This functionality is supported only when the customer data master is set to Loyalty Pro.  
This makes all customer properties, except for transactions and identifications (such as, user name and password), come from the CDM.

To comply with EU GDPR (European Union General Data Protection Regulation) regulations and protect customer’s privacy rights, the Customer Screen is not populated with any data until the user runs a customer search with at least one search criteria.

On searching for a customer, the system returns a list of customers that meet the search criteria. All loyalty customer’s personal information is masked/removed as follows:

**Last Name** – 75% of the last name is masked, showing at least one letter, for example a customer with the following names is displayed as follows:

* Johnson = Jo*****
* Levi = L***
* Dan = D**
* L0 = L*

**Phone Number** – most of the phone number is masked, leaving only the last 4 digits visible

When only one customer is retrieved, the customer's details are not masked, however, if more than one customer is retrieved the customer details are masked. This is configurable based on the ProtectCustomerPersonalInformation system parameter.

**Reference Path:** *Catalog, Promotions & Marketing/Customers/Customers*

![Customers Screen](/Images/CustomersScreen.png)

|**Field**|**Description**|
|---------|----------|
|**First Name**|The customer's first name.<BR>**Note:** When searching by First Name, Last Name, or Email, capital letters and spaces at the beginning or end are ignored.<BR>For example, the customer service representative wants to search for a customer whose first name is David.<BR>The search results include all customers with the names David, david, (with space at the beginning) etc.|
|**Last Name**|The customer's surname.|
|**Card Number**|The customer's registered card number.|
|**Email**|The customer's email address.|
|**Phone (home or mobile)**|The customer's contact phone number.<BR>**Note:** Phone numbers can be entered in any format. If you enter 046595944 or 04-6595944 or (04)6595944, the system ignores the non-numerical characters and retrieves the same results.|

**Reference Path:** *Catalog, Promotions & Marketing/Customers/Customers/Add New*

![Customers Form](/Images/CustomersForm.png)

|**Field**|**Description**|
|---------|----------|
|**ID**|The system allocated ID number used to identify the customer.|
|**Card Number**|The customer's registered card number.|
|**Title**|The prefix used before the customer's name to indicate their marital or academic status. The options are:<BR>Mr. / Mrs. / Miss. / Ms. / Dr. / Prof. / Rev. / Other|
|**First Name**|The customer's first name.|
|**Last Name**|The customer's surname.|
|**Gender**|The options are: Male, Female or Unknown.|
|**Birth Date**|The customer's date of birth.|
|**Personal Details tab**|The customer's personal details.|
|**Loyalty tab**|The customer’s loyalty information.|
|**Promotions tab**|The customer’s registered promotions.|
|**Visits tab**|The number of times a customer visited the store.|
|**Self-scan tab**|The customer’s rescan details.|

### Personal Details Tab

The **Personal Details tab** displays the customer's contact information, family members, and marketing preferences.

**Reference Path:** *Catalog, Promotions & Marketing/Customers/Customers/Add New*

![Personal Details](/Images/PersonalDetails.png)

|**Field**|**Description**|
|---------|----------|
|**Contact Information**|The customer's personal contact information.|
|Country|The country the customer resides in.|
|State|The state the customer resides in.|
|City|The city the customer resides in.|
|Street name|The name of the street in the customer's address.|
|House number|The customer's house number.|
|Zip code|The postal code for the customer's address.|
|Email|The customer's email address.|
|Home phone|The customer's home phone number|
|Mobile phone|The customer's mobile phone number.|
|Receipt configuration|The customer's preferred method to receive a digital receipt.<BR>The options are:<BR>**Always ask** - The customer is always asked.<BR>**No Receipt** - No paper receipt or digital receipt is printed.<BR>**Retailer Default** - The Receipt Settings option selected by the retailer is applied. This is the default value.<BR>**Channel Select** - if this option is selected, the following options are displayed:<BR>* Email - The receipt is sent to an email address.<BR>* SMS - An SMS is sent.<BR>* Paper- The receipt is printed.<BR>**Note:** The selected options must comply with the options selected in the **Propose to receive sale digital receipt** field in the Receipt Settings screen. For example, if Email is selected in the **Propose to receive sale digital receipt** field, then the customer cannot ask for a receipt by SMS. If the retailer has specified that a paper and Email receipt is never printed/sent, then the SMS option is not displayed when Channel Select is selected. If the selected options do not comply, a message is prompted.|
|**Family Members**|The customer's family members. Family Members are used as segments. For example, you can search for all customers who have children under 12 years of age. Family Members are not Household Members unless defined in the Household drawer in the Loyalty tab.|
|Type|The family member’s relationship to the customer.<BR>The options are:<BR>* Child<BR>* Spouse<BR>* Parent<BR>* Relative<BR>* Other.|
|Description|The name of the family member.|
|Gender|The options are: Male, Female or Unknown.|
|Birth Date|The family member’s date of birth.|
|**Marketing Preferences**|The customer's preferred method to receive targeted marketing incentives and advertisements.|
|Email updates|Indicates if the customer wants to receive marketing incentives and advertisements to their email address.|
|Newsletters|Indicates if the customer wants to receive marketing newsletters.|
|SMS updates|Indicates if the customer wants to receive marketing incentives and advertisements updates by SMS.|
|Preferred language|The language the customer wants displayed at the touchpoint after they log in.|
|Preferred store|The store the customer registered in and visits the most. For example, when a customer creates a Shopping List, the system retrieves the item prices form the store catalog of the customer's preferred store.|

### Loyalty Tab

The Loyalty tab displays the customer's Loyalty details, for example, segments the customer is linked to, point account balances, as well as the customer's household members.

Customers can subscribe to a Loyalty program automatically at a touchpoint using the Auto Add function, or by customer service person via the Customer Form.

Once a customer has subscribed to a Loyalty Program, they can enjoy special benefits and rewards. Loyalty customers can have accounts in which points, e.g., Fuel Gallons, Visits and so on, are accumulated, clip digital coupons, be included in customer segments, subscribe to clubs, e.g., baby club, sports clubs and more.

Loyalty customers can also share loyalty benefits such as account points and digital coupons between the household members.

**Reference Path:** *Catalog, Promotions & Marketing/Customers/Customers/Add New* 

![Loyalty](/Images/Loyalty.png)

|**Field**|**Description**|
|---------|----------|
|**Loyalty member**|Indicates that the customer has subscribed to a loyalty program.|
|**Customer tier**|The tier rating assigned to the customer. The tier system is used to classify customers, and help retailers learn which customers deserve the most time and attention enabling retailers to create promotions and campaigns to target a specific group of customers.<BR>Customers are classified according to the amount they spend in the store. Each purchase rewards the customer with points which are accumulated and used to assign the customer to the relevant tier.<BR><BR>For example:<BR><BR>Basic Tier - 0-1000 points <BR>Silver Tier - 1001-5000 points<BR>Gold Tier - 5001-10000 points <BR>Platinum Tier - 10001 points and up<BR>You can give a 10% discount to members linked to the Basic tier, 15% to members linked to the Silver tier and so on.|
|**Segments**|The segments that are linked to a customer.|
|egment ID|The ID of the segment linked to the customer.|
|Segment Name|The name of the segment linked to the customer.|
|**Accounts**|The customer's accounts and account balances.|
|Redemption allowed|Indicates that the customer can redeem points from their accounts. If a Loyalty customer has more than one account and is permitted to redeem points, then points can be redeemed from all the accounts. However, if the customer is not permitted to redeem points, all the accounts are blocked.<BR>You can use this option as an incentive. For example, to encourage customers to provide more personal details to allow for more specific targeting, you can prevent customers who did not enter their full personal details from redeeming points.<BR>Household members can have different redemption privileges to the customer.
|Redemption restriction reason|The reason the customer is not permitted to redeem points from their accounts. A reason must be provided when a Loyalty customer is prohibited from redeeming points.|
|**Account Balances**|The points balance in each accumulator linked to the customer. An Accumulator is an account in which points earned are saved and redeemed. Once a member in a household earns points during a transaction, the information is sent to the CDM, and the balance is updated. The new account balance and the date the account balance was updated are saved.|
|Account ID|The account ID number.|
|Account Name|The account name.|
|Balance|The current account balance.|
|**Household**|The other customers who belong to the same household and share the customer accumulator accounts.<BR>A household is a group of connected customers, for example, a family who share points and coupons earned in a specific account, also known as an accumulator. When a Household member earns points, the points are accumulated in the account linked to the household, and all members of the household benefit from the aggregated earned benefits.<BR>A customer cannot be included in two households simultaneously.
|Customer ID|The customer ID number.|
|First Name|The customer’s first name.|
|Last Name|The customer’s last name.|
|Card Number|The customer’s card number.|
|Redemption allowed|Indicates that the customer can redeem points from their accounts. If a Loyalty customer has more than one account and is permitted to redeem points, then points can be redeemed from all the accounts. However, if the customer is not permitted to redeem points, all the accounts are blocked.<BR>You can use this option as an incentive. For example, to encourage customers to provide more personal details to allow for more specific targeting, you can prevent customers who did not enter their full personal details from redeeming points.<BR>Household members can have different redemption privileges to the customer.|
|Redemption restriction reason|The reason the customer is not permitted to redeem points from their accounts. A reason must be provided when a Loyalty customer is prohibited from redeeming points.|

### Promotions Tab

The **Promotions tab** displays the promotions and coupons the customer and/or any member of the household are registered to.

**Reference Path:** *Catalog, Promotions & Marketing/Customers/Customers/Add New*

![Promotions Tab](/Images/PromotionsTab.png)

|**Field**|**Description**|
|---------|----------|
|**Registered Promotions**|Displays a list of the promotions registered to the customer. When a transaction is started at the POS, and the customer is registered either as a Loyalty customer or a mobile shopper, the system identifies the customer and the promotions registered to the customer are available.<br>Currently, a promotion can be redeemed only once. Once the promotion is triggered, it is disconnected from the customer, and removed from the list of registered promotions.|
|Promotion ID|The ID of the promotion registered to the customer.|
|Promotion name|The name of the promotion.|
|Registration Date|The date the customer registered to the promotion.|
|Expiration Date|The date on which the registration to the promotion expires.|
|Status|The promotion status. The options are:<BR>**Registered** - The customer registered to the promotion.<BR>**Burned** – The customer was registered to the promotion and has received the promotion reward.<BR>**Expired** - The customer registered to the promotion, however, the promotion or the registration period expired before the customer received the promotion reward.<BR>**Unregistered** - The customer registered to the promotion and then cancelled their registration.|
|**Coupons**|Displays the coupons registered to the customer or to one of the household members. Active coupons are displayed first and then redeemed coupons. The coupons are sorted by End Date in ascending order (active coupons are displayed first).|
|Coupon Barcode|The barcode of the coupon.|
|Reward value|The coupon reward value.|
|Start Date|The date from which the coupon can be redeemed.|
|Expiration Date|The date from which the coupon expires.|
|Redeemed|The customer redeemed the coupon and received the coupon reward.|
|Redemption Date|The date on which the customer redeemed the coupon.|

### Visits Tab

The Visits tab displays the number of times a customer or a member of the same household visited the stores. You can view a list of the customer's transactions as well as the store the customer prefers to shop in, the total amount spent by the customer and the customer's card number

**Reference Path:** *Catalog, Promotions & Marketing/Customers/Customers/Add New*

![VIsits Tab](/Images/VisitsTab.png)

|**Field**|**Description**|
|---------|----------|
|**Training mode tickets**|Indicates that the Show Results displays only tickets performed in Training mode when viewing Customer Visits information.|
|**Visits**|Displays a list of the customer's transactions made when the customer visited the store and purchased items.|
|Purchase Date|The date and time of the purchase.|
|Store Name|The store in which the customer purchased the items.|
|POS Code|The ID of the POS touchpoint on which the transaction was performed.|
|Total Ticket Spend|The total amount spent in the transaction.|
|Card Number|The number of the customer's card used to pay for the transaction.|
|**Stores**|Displays a list of stores the customer frequently shops in. Stores are added to a customer's list of local stores based on their shopping history. For example, if a customer visits the same store in the last x months, the store is added to their list.<BR>The Customer Data Management (CDM) adds/removes the local stores to and from a customer's stores list. Currently, this logic is external, and is not calculated by the CDM. The CDM only updates the stores list in the Customer Management screen on request.|
|Store|The ID of the customer’s local store.|
|Store Name|The Store name.|
|Business Unit|The business unit to which the store is linked.|
|City|The city in which the store is located.|
|Card Number|The number of the customer card used to pay for the transaction.|
|Phone (home or mobile)|The store's phone number.|

### Self-Scan Tab

The Self Scan tab displays customer rescan information. You can view the details of customers’ self scan transactions as well as the number of transactions rescanned.

Customers have the option to take a Self-Scan device, and scan each item before placing it in the shopping cart. The Self Scan comes with security features to protect the retailer. This includes a mechanism to automatically trigger a rescan of the items, or manually trigger a forced rescan of the items. This option enables the retailer to double-check that customers scanned all the items in their shopping cart.

**Reference Path:** *Catalog, Promotions & Marketing/Customers/Customers/Add New*

![Self-Scan Tab](/Images/SelfScanTab.png)

|**Field**|**Description**|
|---------|----------|
|**Rescan details**||
|Trust Level|The trust level assigned to the customer determines the frequency that a full or partial rescan is performed. A rescan requires the cashier to rescan the items previously scanned by the customer as a security measure to prevent theft.<BR>When the customer uses their Self Scan card to start a Self Scan transaction, the system validates the assigned trust level.<BR>Trust Levels are configured in the Security Policy and are configurable.<BR>The probability of a rescan being performed increases with lower Trust Level. For example, rescans are not performed for customers with Trust Level 5, however a customer assigned Trust Level 1 will always be rescanned.|
|Force rescan on next trip|A rescan is enforced next time a customer performs a Self Scan transaction. Can be used if the customer service desk suspects inappropriate shopping behavior. The options are:<BR>**Full** - All the items in the transaction are rescanned by the cashier.<BR>**Partial** - A defined number of items in the transaction are rescanned by the cashier. The number of items rescanned is defined in the system parameters.<BR>**None** - No rescan is performed.|
|Suspended User|The user is suspended due to fraudulent use.<BR>Prevents fraudulent customers, known to the retailer, from using the Self Scan service. When a suspended customer scans/swipes their loyalty card on the Entry Unit, a message informing the customer to approach the customer service desk for further assistance is displayed on the Entry Unit.<BR>The shopper status can be changed at any time from suspended to not suspended. A ‘Status change reason’ is provided  to track a shopper’s history.|
|Suspended Reason|The reason the customer was suspended. The suspended reason can be updated.|
|**Last Transactions summary**|
|No. of self scan transactions since last rescan|The number of the self scan transactions performed by the customer since the last full or partial rescan was performed on the customer's scanned items.|
|Total no. of self scan transactions|The total number of the customer’s self scan transactions.|
|**Last self scan transaction:**||
|Amount|The amount of the last self scan transaction performed by the customer.|
|Date|The date of the last self scan transaction performed by the customer.|
|**Last full rescan:**||
|Date|The date the last full rescan was performed on the customer's self scan transactions.|
|Succeeded|Indicates if the rescan was successful and there were no discrepancies between the self scan transaction and the rescan transaction.|
|**Last partial rescan:**||
|Date|The date the last partial rescan performed on the customer's self scan transactions.|
|Succeeded|Indicates that the rescan was successful, and there are no discrepancies between the self scan transaction and the rescan transaction|

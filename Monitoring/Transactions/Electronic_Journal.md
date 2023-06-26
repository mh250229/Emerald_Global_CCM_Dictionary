### Electronic Journal

**Electronic Journal (EJ)** is used to query transactions recorded at the POS terminal. You can locate any type of transaction, such as sales transactions, POS events and cash office transactions at any date. For example, store managers can query or track any transaction performed by the cashiers, or if a customer returns to the store and is querying an amount in the ticket, the store manager can retrieve the transaction in question from the EJ.

After defining the search criteria, the results are displayed in a grid enabling easy access and ability to analyze the results. You can sort the results according to specified requirements, export an actual image of each ticket, and electronic signatures, as well as print a copy of the grid results if required.

**Reference Path:** *Monitoring/Transactions/Electronic Journal*

![Electronic Journal Screen](/Images/ElectronicJournalScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Transaction Types**|The transaction type searched in the Electronic Journal.<BR>The options are:<BR><BR>**Retail** – Sales transactions<BR>**Control** – Transaction such as Cashier sign on, Invalid sign on.|
|**Store**|The store for which the report is generated.|
|**Start Date/Time**|The date and time from which the transaction was performed.|
|**End Date/Time**|The date and time up to which the transaction was performed.|
|**Transaction Number**|The transaction number. The full or partial transaction number can be used to search for transactions.|
|**Total Amount**|The total transaction amount. The options are:<BR><BR><=<BR>=<BR>>=<BR>The total amount is entered in the Enter Total Amount field.|
|**Transaction Display**|Specifies which transactions that meet the search criteria are retrieved. The options are:<BR><BR>**Show All Transactions** – indicates that all transactions that meet the search criteria are retrieved.<BR>**Show All Transactions, excluding Voided Transactions** - indicates that all transactions that meet the search criteria are retrieved excluding voided transactions.<BR>**Show Only Voided Transactions** - indicates that only voided transactions that meet the search criteria are retrieved.|
|**Show Only Training Mode Transactions**|Indicates that only transactions that were performed in Training Mode are retrieved. This enables supervisors to view the transactions performed by trainee employees, e.g., trainee cashiers, to monitor their progress and provide feedback. When viewing a Training Mode transaction, a Training Mode indication is displayed on the ticket.|
|**Show Only Employee’s Transactions**|Indicates that only transactions performed for employees are retrieved. This is applicable to Retail Transaction Types only.|
|**Customer Id**|The customer's Loyalty (Member) ID number.|
|**Touchpoint ID**|The ID of the touchpoint on which the transaction was performed.|
|**Items**|The item code of the item in the transaction. The full or partial item code can be used to retrieve transactions containing the item.|
|**Touchpoint Type**|The touchpoint type. The options are:<BR><BR>Customer Order Management<BR>Customer Scale<BR>DMS Agent<BR>Forecourt<BR>FuelPOS<BR>KeyboardPOS<BR>MobilePOS<BR>Mobile Shopper<BR>Online Shopping<BR>Portal<BR>POS<BR>Pump<BR>QSRPOS<BR>SelfCheckout<BR>SelfScanDevice<BR>SelfScanEU<BR>Unknown|
|**Origin Touchpoint ID**|The ID number of the touchpoint on which the transaction was originally generated.|
|**Rescan Status**|The rescan status of specific transactions on which a rescan was performed.  The options are<BR><BR>**Success** - indicates transactions in which the rescan was successful<BR>**Failure** - indicates transactions in which the rescan was not successful<BR>**All** – indicates all transactions in which a rescan was performed|
|**Operator ID**|The ID of the user who performed the transaction.|
|**Tenders With Amounts**|The tender and the amount paid with the tender. The options are:<BR><BR>**Tender ID** - the Tender ID according to which you want to search for transactions.<BR>**Tender Amount** - the Amount paid with the selected tender.|

#### Electronic Journal Transaction List

The **Transaction List** shows a list of the transactions that meet the search criteria.

**Reference Path:** *Monitoring/Transactions/Electronic Journal/View Transactions*

The following screen displays Retail transactions.

![Electronic Journal Transaction List Screen](/Images/ElectronicJournalTransactionListScreen.png)

The following screen displays Control transactions.

![Transaction List](/Images/ControlTransactions.png)

|**Field**|**Description**|
|---------|----------|
|Transaction Number|The number of the retrieved transaction.|
|End Date/Time|The date up to which date criteria was selected. For example, if you performed a search for a transaction between the 01/06/2011 and the 05/06/2011, this field displays the last date on which the transaction was identified.|
|Store Name|The store name in which the transaction was performed.<BR>Not displayed for Control Transactions.|
|Touchpoint ID|The ID number of the touchpoint on which the transaction was performed.|
|Cashier Name|The name of the cashier who performed the transaction.|
|User Name|The ID of the operator/cashier who performed the transaction.|
|Transaction Type Name|The transaction type name.<BR>For Retail transactions, the text ‘Retail’ is displayed for all transactions.<BR>For Control transactions, the name of the Control Transaction, e.g., Cashier Sign On, Z report is displayed.<BR>To filter transactions by the transaction type name, select ![Filter](/Images/Filter.png) . The filter is displayed.<BR>![Filter Name](/Images/FilterName.png)<BR>Select the checkbox of the transaction type name by which you want to filter and select **Apply**.|
|Total Amount|The total amount of the transaction retrieved.<BR>Not displayed for Control Transactions.|
|Transaction Details|The details of the selected transaction. To view the transaction details, select ![Blue Expand Arrows](/Images/BlueExpandArrows.png) . The Transaction Details pane expands to show the transaction details.|

#### Transaction Details

**Transaction Details** displays the details of the transaction retrieved in the Electronic Journal.

The following screen displays Retail transactions.

![Retail Transaction Details Screen](/Images/RetailTransactionDetailsScreen.png)

The following screen displays Control transactions.

![Control Transaction Details Screen](/Images/ControlTransactionDetailsScreen.png)

|**Field**|**Description**|
|---------|----------|
|**General**||
|Control Transaction Type|The name of the Control transaction.<BR>This is only displayed in Control transactions.|
|Start Date/Time|The date and time the transaction started.|
|End Date/Time|The date and time the transaction was completed.|
|Store Name|The name of the store in which the transaction was performed.<br>This is not displayed in Control transactions.|
|Touchpoint ID|The ID of the touch point on which the transaction was performed.|
|Transaction Number|The ID number of the transaction.|
|Total Sales|The total amount of items sold in the transaction.<BR>This is not displayed in Control transactions.|
|Operator Name|The name of the user who performed the transaction.|
|User Name|The user ID the user who performed the transaction uses to log in.|
|Reason|The reason the transaction was voided.<br>This is not displayed in Control transactions.|
|Customer Name|The name of the customer.<br>This is not displayed in Control transactions.|
|Sold Item Count|The number of items sold in the transaction.<br>This is not displayed in Control transactions.|
|Returned Item Count|The number of items returned in the transaction.<br>This is not displayed in Control transactions.|
|Total Tax Inclusive|The total amount of taxes included in the item price.<br>This is not displayed in Control transactions.|
|Total Tax Exclusive|The total amount of taxes not included in the item price, and is added to the price during the sales transaction.<br>This is not displayed in Control transactions.|
|Total Savings|The total amount saved by the customer in the transaction.<br>This is not displayed in Control transactions.|
|Total Tip Amount|The total amount of tips included in sales transactions.<br>This is not displayed in Control transactions.|
|Total Amount|The total transaction amount.<br>This is not displayed in Control transactions.|
|**Detailed tab**|Not relevant for Control Transactions.|
|**Items**|![Items](/Images/items.png)|
|Dept ID|The Id of the department linked to the item.|
|Item ID|The item code of the item sold in the transaction.|
|Description|The name of the item sold in the transaction.|
|Status|Indicates if the item is a sale or return item.|
|Unit Price|The cost of each item unit in the transaction.| 
|Actual Unit Price|The actual cost of each item unit at the time the transaction was performed.|
|Units|The number of units of each item sold in the transaction.|
|Quantity|The item quantity sold in the transaction.|
|UOM|The unit of measure in which the item in the transaction was sold.|
|Amount|The value of the item sold in the transaction.|
|**Fuel Items**|![Fuel Items](/Images/fuelitems.png)|
|Item ID|The code of item sold in the transaction.|
|Description|The name of the fuel item.|
|Unit Price|The item price per unit sold.|
|Actual Unit Price|The actual cost of the fuel item when sold.|
|Units|The number of units of the fuel item sold in the transaction.|
|Quantity|The fuel quantity sold in the transaction.|
|UOM|The unit of measure by which the fuel item is sold.|
|Amount|The value of the fuel item sold in the transaction.|
|**Tenders**|![Tenders](/Images/tenders.png)|
|Name|The name of the tender used to pay for the transaction.|
|Amount|The amount tendered in the transaction with the tender.|
|Original Amount|The amount originally paid in the transaction.|
|Exchange Rate|The exchange rate used when a foreign currency is used to pay for the transaction.|
|Abandoned Void|Indicates if the item was included in an abandoned transaction that was automatically voided by the system.<BR>The options are:<BR><BR>**Yes** - indicates the transaction was automatically voided.<BR>**No** - indicates the transaction was not voided.|
|**Taxes**|![Taxes](/Images/taxes.png)|
|Imposition|The imposition assigned to the tax rate. Impositions are placeholders for sets of tax rules that are shared according to the type of tax and/or jurisdictional grouping. The Imposition name identifies the tax type imposed for the transaction.|
|Description|A description of the tax applied in the transaction.|
|Included|Indicates if the applied tax is Inclusive or Exclusive.<BR>The options are:<BR><BR>**No** - the tax value is not included in the item price and is added to the price during the sales transaction<br>**Yes** - the tax value is included in the item price|
|Tax Rate|The Tax rate applied in the transaction.|
|Amount|The actual tax amount added to the transaction.|
|**Tips**|![Taxes](/Images/tips.png)|
|Tender|The payment type by which the tip was paid.|
|Authorization Number|The authorization number of the original payment.|
|Tip Amount|The tip amount after applying any exchange rate (if necessary).|
|Original Tip Amount|The tip amount in the original tender|
|Exchange Rate|The rate of exchange, relevant to tips in foreign currencies.|
|Updated By|The name of the person who last adjusted the tip. (if relevant)|
|Update Date|The date on which the tip was last adjusted.|
|**Promotions**|![Promotions](/Images/promotions.png)|
|Promotion ID|The promotion ID number.|
|Description|The promotion name.|
|Reward Type|The reward issued in the promotion. The reward options are:<BR><BR>**Monetary** – indicates that a monetary discount was issued, e.g.,  Amount Off, % off, Free Item. New Price, Gift Card<BR>**Member Account** – indicates that points were added to a member account<BR>**Message** – indicates that a target message was displayed, e.g., On Your Next purchase Get 10% Off<BR>**Tender** – indicates that a tender triggered the promotion, e.g., Pay with Cash, Get 5% Off.<BR>**Coupon** – indicates that a coupon was issued|
|Reward Amount|The monetary or points amount rewarded in the promotion.|
|**Receipt**|**Note:** Only Z-Report control transactions are displayed in the receipt tab.<BR>The image of the transaction receipt.<BR>![Promotions](/Receipt Image/receiptimage.png)|
|**Signature**|An image of the customer’s signature is displayed. The signature is displayed in the actual signature size.<BR>This is not displayed in Control transactions.|
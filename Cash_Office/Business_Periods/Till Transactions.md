### Till Transactions

Till Transactions is used to view all cash office activities performed on a selected touchpoint in a business period. The activities are displayed in categories. The total number of activities performed, the total amount recorded for each activity and drill down to view the actual transaction is displayed.

**Reference Path:** *Cash Office/Business Periods/Till/Cashier Pending Periods/Till Transactions*

![Till Transactions Form](/Images/TillTransactionsForm.png)

|**Field**|**Description**|
|---------|----------|
|**Open Amount**|The initial balance in the till at the beginning of the business period.|
|**Total In**|The total amount received in the Till Account for all the Cash Office Activities during the business period.<br>**Note**: If the Cash tender is configured as Auto Reconcile, the value of the Cash back is added to the auto reconcile account. For example, in an EFT payment which includes a Cash back, the Total In amount is increased by the payment, including the Cash back amount.|
|**Total Out**|The total amount withdrawn from the Till Account for all the Cash Office Activities during the business period.<BR>When the Cash Tender auto reconciled and defined as the Cashback tender, the Cashback amount is displayed on a separate line in the Total Out section.|
|**Expected Amount**|The system generated amount for the selected account.|
|**Actual Amount**|The actual amount recorded for the selected account.|
|**Over / Short**|The options are:<BR><BR>**Over** - The declared Tender is more than the calculated value. Over amounts are a positive number and Over is displayed next to the amount.<BR>**Short** - The declared Tender is less than the calculated value. Short amounts are a negative number and Short is displayed next to the amount.|
|**Transaction List**|A summary of the cash office activities that took place on the till.|
|View Transactions|Click to display the details of the Activities and Tenders in the business period.<BR>The View Transaction field is only enabled when an activity is selected in the Transaction List. See also: [Transaction List](<../../Cash_Office/Business_Periods/Transaction List.md>)|
|Balancing Counters|The cash office activity that generated the transactions.|
|Activity Count|A count of the times the selected activity was performed on the till.|
|Total Amount|The total amount in the transactions.|
|**Tender List**|A list of the tenders used in the selected activity. The fields in the grid are customizable.|
|Customize Columns|Enables you to select the columns displayed in the Tender List grid. To select the column, click ![Down arrow icon](/Images/downarrowicon.png) . A list of the available columns is displayed. Select the columns you want to display in the grid.|
|Tender ID|The ID of the Tender recorded in the transaction.|
|Tender|Name of the tender. For definitions see Organization/Operational Entities/Tender.|
|Amount|The tender amount in the base currency, e.g., the currency from which you converting.|
|Converted Rate|The converted tender amount.|
|Over / Short|The Over/Short amount recorded for the tender.|
|Over / Short Converted Rate|The converted Over/Short amount.|
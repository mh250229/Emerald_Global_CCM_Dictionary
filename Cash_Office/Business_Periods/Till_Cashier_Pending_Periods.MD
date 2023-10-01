## Till/Cashier Pending Periods

**Till/Cashier Pending Periods** display the Till and Cashier Business Periods that have not been approved.

Once the system identifies cash office activities were performed between the various cash office accounts, e.g., an opening fund issued to all POS terminals, pickups where cash was removed from the POS terminals, Pay In or Pay outs, etc., a till business period is created.

Stores can have several pending business periods simultaneously, and you can modify and view each business period if required. Cash Office activities can be settled, and the business period saved and approved later.

Business Periods are approved only once the accounts are balanced or the management are satisfied with the 'Over' or 'Short' amount generated after the last declaration was performed.

**Reference Path:** *Cash Office/Business Periods/Till/Cashier Pending Periods*

![Till Cashier Pending Periods Screen](/Images/TillCashierPendingPeriodsScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Store**|The store in which to view a Till Business period.|
|**Business Periods**||
|Add Activity|Click to add a Cash Office Activity to the Business period. When clicked, the Activities screen is displayed, and you can select an activity, enter the relevant details, and add the activity to the Business period.<BR>**Note**: The **Add Activity** and **Declare** links are disabled for users assigned to a role prohibited from performing Cash Office Activities on a past date.<BR>The Roles prohibited from performing Cash Office Activities on a past date are configured via the ProhibitedRolesForPastDatesInCashOfficeActivities parameter in the OfficeBusinessConfigurationMaintenanceRequest RTI.|
|Declare|Click to declare the undeclared accounts in the Business Period. When selected, the Activities/Till Declaration form is displayed. You can declare the account as required.|
|Approve All|Click to approve all the balanced accounts in the selected Business Period.|
|Settle|Click to settle the selected Business Period.|
|Approved|Indicates that the Business Period was approved.|
|Started|The date from which the Business Period started. The date is a hyperlink which opens the Edit Till/Cashier Business Period depending on the accountability method used in the store.|
|End by|The date on which the Business Period ended.|
|Unbalanced accounts|The number of **unbalanced accounts** out of the **total number of accounts** in the Business Period. Unbalanced accounts have either an over or short amount.<BR>An **over amount** means that the declared Tender is greater than the calculated value, it is reflected as Over with a positive value<BR>A **short amount** means that the declared Tender is less than the expected value, it is reflected as Short with a negative value<BR>Only active accounts, i.e., accounts linked to active Account Profiles are included in the number of Unbalanced Accounts.<BR>**Note:** Account history for the periods during which the Cash Office Account was active can be viewed even if the Account is currently linked to an inactive Account Profile.|
|Undeclared accounts|The number of undeclared accounts in the Business Periods.<BR>Only active accounts, i.e., accounts linked to active Account Profiles are included in the number of Undeclared Accounts.|

### Till Business Period

**Till Business Periods** (edit) is used to view, modify, approve, and settle the accounts in a Business period in a store operating in Till Accountability.

**Note:** In Cashier Accountability, the Cashier Business Period is displayed.

**Reference Path:** *Cash Office/Business Periods/Till/Cashier Pending Periods/Edit*

![Till Business Period Screen](/Images/TillBusinessPeriodScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Store**|The store for which the Till Business period is shown.|
|**Started**|The date from which the Business Period started.|
|**End by**|The date on which the Business Period ended.|
|**Business Periods**||
|Account|The touchpoint account in the Touchpoint Group. The hyperlink opens the Till Transactions. See also: Till Transaction.|
|Opening Amount|The money that came in from sales, loans, Paid-in's, etc.|
|Expected Amount|The money that was taken out of the touchpoint by pickups, paid-out, etc.|
|Over / Short|The actual over/short amount in each touch point account. For example:<BR>Over amounts have a red up arrow ![Red Up Arrow](/Images/reduparrow.png) and a positive number with the text “(Over)” next to the amount.<BR>	Short amounts have a red down arrow ![Red Down Arrow](/Images/reddownarrow.png) and a negative number with the text “(Short)” next to the amount.<BR>Balanced accounts have the text “Balanced” in green.
|Approve|Indicates that the account is approved. Accounts are approved only when balanced or when the Over/Short amount has been approved. When approving an Over/Short amount, a reason must be given. Once an account is approved, the user can perform a settlement to balance the period.|
|Reason|The reason for the over/short amount. A reason must be entered before a short or over business period can be approved.

### Till Transactions

Till Transactions is used to view all cash office activities performed on a selected touchpoint in a business period. The activities are displayed in categories. The total number of activities performed, the total amount recorded for each activity and drill down to view the actual transaction is displayed.

**Reference Path:** *Cash Office/Business Periods/Till/Cashier Pending Periods/Till Transactions*

![Till Transactions Form](/Images/TillTransactionsForm.png)

|**Field**|**Description**|
|---------|----------|
|**Open Amount**|The initial balance in the till at the beginning of the business period.|
|**Total In**|The total amount received in the Till Account for all the Cash Office Activities during the business period.<br>Note: If the Cash tender is configured as Auto Reconcile, the value of the Cash back is added to the auto reconcile account. For example, in an EFT payment which includes a Cash back, the Total In amount is increased by the payment, including the Cash back amount.|
|**Total Out**|The total amount withdrawn from the Till Account for all the Cash Office Activities during the business period.<BR>When the Cash Tender auto reconciled and defined as the Cashback tender, the Cashback amount is displayed on a separate line in the Total Out section.|
|**Expected Amount**|The system generated amount for the selected account.|
|**Actual Amount**|The actual amount recorded for the selected account.|
|**Over / Short**|The options are:<BR><BR>**Over** - The declared Tender is more than the calculated value. Over amounts are a positive number and Over is displayed next to the amount.<BR>**Short** - The declared Tender is less than the calculated value. Short amounts are a negative number and Short is displayed next to the amount.|
|**Transaction List**|A summary of the cash office activities that took place on the till.|
|View Transactions|Click to display the details of the Activities and Tenders in the business period.<BR>The View Transaction field is only enabled when an activity is selected in the Transaction List. See also: Transaction List|
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

### Transaction List

**Transaction List** is used to view the details of the Cash Office activities performed in the selected business period. The Transaction List is displayed on selecting the Cash Office Activity in the Till Transaction Screen and clicking the blue View Transaction link.

**Reference Path:** *Cash Office/Business Periods/Till/Cashier Pending Periods/Till Transactions/Transaction List*

![Down arrow icon](/Images/transactionlistscreen2.png)

|**Field**|**Description**|
|---------|----------|
|**Store**|The store in which the activity was performed.|
|**Activity Name**|The name of the cash office activity.|
|**Account**|The touchpoint account in which the activity was performed.|
|**User**|The name of user who performed the transaction.|
|**Start Business Date**|The start date of the business period in which the activity was performed.|
|**End Business Date**|The end date of the business period in which the activity was performed.|
|**Monetary Adjusted Transactions Only**|Indicates that only Cash office activities in which at least one adjustment was performed are retrieved and displayed in the Cash Office Activities Log grid.|
|**Activities**||
|Transaction Date|The date and time the Cash Office Activity was performed.|
|Id|The ID of the Cash Office Activity.|
|User|The name of the user who performed the activity.|
|Reference|The reference to the Cash Office Activity defined when performing the activity, e.g., an invoice number.<BR>The reference text can be adjusted based on the IsReferenceAdjustable parameter configuration in the ActivityReferenceConfigurationMaintenanceRequest RTI.<BR>When the parameter is set to True, the **Reference** field can be adjusted.<BR>**Note**: The **Reference** field cannot be adjusted for Cash Office Activities in settled Business Periods.|
|Activity Name|The name of the Cash Office Activity.|
|From Account|The account from which money for the defined activity is transferred.|
|To Account|The account to which money for the defined activity is transferred.|
|Total Amount|The total amount in the transactions.|
|Tax Amount|The tax amount applied in the Paid In or Paid Out Cash Office Activity.<BR>If the Tax Amount is a fixed amount, the field is read only and cannot be modified.<BR>If the Tax Amount is based on a Tax Rate, an ![Tax rate icon](/Images/taxrateicon.png) icon is displayed in the field. On clicking the icon, the Tax Rates screen is displayed showing the updated tax amount per tax rate. See also: Tax Rates<BR>**Note**: The **Tax Amount** field is only displayed for Paid In and Paid Out Cash Office Activities.|
|Over / Short|The over/short amount declared for the activity.<BR>The options are:<BR>* **Over** - The declared Tender is more than the calculated value. Over amounts are a positive number and Over is displayed next to the amount.<BR>* **Short** - The declared Tender is less than the calculated value. Short amounts are a negative number and Short is displayed next to the amount.|
|**Tenders**||
|Customize Columns|Enables you to select the columns displayed in the Tenders grid. To select the column, click ![Down arrow icon](/Images/downarrowicon.png) . A list of the available columns is displayed. Select the columns you want to display in the grid.|
|Tender ID|The ID of the tender recorded in the activity.|
|Tender Name|The name of the tender.|
|Original Amount|The amount originally paid in the transaction.|
|Original Converted Rate|The tender amount in the base currency, e.g., the currency from which you are converting.|
|Total Amount|The total tender amount for the activity.|
|Amount|The converted tender amount.|
|Converted Rate|The currency exchange rate.|
|Reason|The reason for the over/short amount, if the amount is not balanced.|
|Over / Short|The over or short amount declared for the activity.|
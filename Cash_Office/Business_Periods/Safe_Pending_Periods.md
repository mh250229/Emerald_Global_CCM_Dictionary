## Safe Pending Periods

**Safe Pending Period** displays Safe Business Periods that have not been approved. Stores can have several pending business periods simultaneously and you can modify and view each business period if required.

Business Periods are approved after the accounts are balanced or the management are satisfied with the 'Over' or 'Short' amount generated after the last declaration was performed.

**Reference Path:** *Cash Office/Business Periods/Safe Pending Periods*

![Safe Pending Periods Screen](/Images/SafePendingPeriodsScreen.png)

|**Field**|**Description**|
|---------|----------|
|Store|The store in which to view a Safe Business period.|
|**Business Periods**||
|Add Activity|Click to add a Cash Office Activity to the Business period. When clicked, the Activities screen is displayed, and you can select an activity, enter the relevant details, and add the activity to the Business period.<BR>**Note**: The **Add Activity** and **Declare** links are disabled for users assigned to a role prohibited from performing Cash Office Activities on a past date.<br><BR>The Roles prohibited from performing Cash Office Activities on a past date are configured via the ProhibitedRolesForPastDatesInCashOfficeActivities parameter in the OfficeBusinessConfigurationMaintenanceRequest RTI.|
|Declare|Click to declare the undeclared accounts in the Business Period. When selected, the Activities/Till Declaration form is displayed. You can declare the account as required.|
|Approve All|Click to approve all the balanced accounts in the selected Business Period.|
|Settle|Click to settle the selected Business Period.|
|Approved|Indicates that the Safe Business Period is approved.|
|Started|The date from which the Business Period started. The link is a hyperlink which displays the Safe Pending Period.|
|End by|The date on which the Business Period ended.|
|Unbalanced accounts|The number of unbalanced accounts out of the total number of accounts in the Business Period. Unbalanced accounts have either an over or short amount.<BR>An over amount means that the declared Tender is greater than the calculated value, it is reflected as Over with a positive value<BR>A short amount means that the declared Tender is less than the expected value, it is reflected as Short with a negative value<BR>Only active accounts, i.e., accounts linked to active Account Profiles are included in the number of Unbalanced Accounts.<BR>**Note:** Account history for the periods during which the Cash Office Account was active can be viewed even if the Account is currently linked to an inactive Account Profile.|
|Undeclared accounts|The number of undeclared accounts in the Business Periods.<BR>Only active accounts, i.e., accounts linked to active Account Profiles are included in the number of Undeclared Accounts.|

### Safe Business Period

**Safe Business Periods** is used to create, edit or view settlement periods for safe accounts. Safe Balancing can be performed for the entire Touchpoint Group or for a single account in the group.

**Reference Path:** *Cash Office/Business Periods/Safe Pending Periods/Edit*

![Safe Business Period Form](/Images/SafeBusinessPeriodForm.png)

|**Field**|**Description**|
|---------|----------|
|**Store**|The store for which the Safe Business period is shown.
|**Started**|The date from which the Business Period started.|
|**End by**|The date on which the Business Period ended.|
|**Accounts**||
|Account|The name of the active touchpoint account in the Touchpoint Group.|
|Opening Amount|The money that came in from sales, loans, Paid-in's, etc.|
|Expected Amount|The money that was taken out of the touchpoint by pickups, paid-out, etc.|
|Declaration|The actual amount of money counted that currently resides in the safe.|
|Over / Short|The actual over/short amount in each touch point account. For example:<BR>Over amounts have a red up arrow ![Red Up Arrow](/Images/RedUpArrow.png) and a positive number with the text “(Over)” next to the amount.<BR>Short amounts have a red down arrow ![Red Down Arrow](/Images/RedDownArrow.png) and a negative number with the text “(Short)” next to the amount.<BR>Balanced accounts have the text “Balanced” in green.|
|Approve|Indicates that the account is approved. Accounts are approved only when balanced or when the Over/Short amount has been approved. When approving an Over/Short amount, a reason must be given. Once an account is approved, the user can perform a settlement to balance the period.
|Reason|The reason for the over/short amount. A reason must be entered before a short or over business period can be approved.|

### Safe Transactions

**Safe Transactions** is used to view the cash office activities performed on a selected safe in a business period. The activities are displayed in categories. You can view the total number of activities performed as well as the total amount recorded for each activity. In addition, you can drill down to view the actual transaction.

**Reference Path:** *Cash Office/Business Periods/Safe Pending Periods/Safe Transactions*

![Safe Transactions Screen](/Images/SafeTransactionsScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Open Amount**|The initial balance in the Safe account at the beginning of the business period.|
|**Total In**|The total amount received in the Safe Account for all the Cash Office Activities during the business period.|
|**Total Out**|The total amount withdrawn from the Safe Account for all the Cash Office Activities during the business period.|
|**Expected Amount**|The system generated amount for the selected account.|
|**Over / Short**|The options are:<BR><BR>* **Over** - The declared Tender is more than the calculated value. Over amounts are displayed in red as a positive number, and Over is displayed next to the amount.<br>* **Short** - The declared Tender is less than the calculated value. Short amounts are displayed in red as a negative number, and Short is displayed next to the amount.|
|**Transaction List**|A breakdown of each transaction recorded for the selected activity|
|Balancing Counters|The cash office activity that generated the transactions.|
|Activity Count|The total number of the selected activity performed in the business period.|
|Total Amount|The total amount in the transactions.|
|**Tender List**|A list of the tenders used in the selected activity.|
|Tender ID|The ID of the Tender recorded in the transaction.|
|Tender|The name of the tender.|
|Amount|The tender amount in the base currency, e.g., the currency from which you converting.|
|Converted Rate|The converted tender amount.|

### Transaction List

**Transaction List** is used to view the details of the Cash Office activities performed in the selected Safe business period. The Transaction List is displayed on selecting the Cash Office Activity in the Safe Transactions screen and clicking the View Transaction link.

**Reference Path:** *Cash Office/Business Periods/Safe Pending Periods/Safe Transactions/Transaction List*

![Transaction List Screen](/Images/TransactionListScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Store**|The store in which the activity was performed.|
|**Activity Name**|The name of the cash office activity.|
|**Account**|The touchpoint account in which the activity was performed.|
|**User**|The name of user who performed the transaction.|
|**Start Business Date**|The start date of the business period in which the activity was performed.|
|**End Business Date**|The end date of the business period in which the activity was performed.|
|**Monetary Adjusted Transactions Only**|Indicates that only Cash office activities in which at least one adjustment was performed are retrieved and displayed in the Cash Office Activities Log grid.|
|**Activities**|
|Cancel|Click to cancel all the adjustments performed for the Cash Office Activity. Once cancelled, the original values are redisplayed.|
|Save|Click to save all the adjustments performed for the Cash Office Activity, e.g., such as the Reference, Tax Amount and Tender Amount.|
|Transaction Date|The date and time the Cash Office Activity was performed.|
|ID|The ID of the Cash Office Activity.|
|User|The name of the user who performed the activity.|
|Reference|The reference to the Cash Office Activity defined when performing the activity, e.g., an invoice number.<BR>The reference text can be adjusted based on the IsReferenceAdjustable parameter configuration in the ActivityReferenceConfigurationMaintenanceRequest RTI.<BR> When the parameter is set to True, the **Reference** field can be adjusted.<BR>**Note**: The **Reference** field cannot be adjusted for Cash Office Activities in settled Business Periods.|
|Activity Name|The name of the Cash Office Activity.|
|From Account|The account from which money for the defined activity is transferred.|
|To Account|The account to which money for the defined activity is transferred.|
|Total Amount|The total amount in the transactions.|
|Tax Amount|The tax amount applied in the Paid In or Paid Out Cash Office Activity.<BR>If the Tax Amount is a fixed amount, the field is read only and cannot be modified.<BR>If the Tax Amount is based on a Tax Rate, an ![Tax Rate icon](/Images/taxrateicon.png) icon is displayed in the field. On clicking the icon, the **Tax Rates** screen is displayed showing the updated tax amount per tax rate. See also: Tax Rates<BR>**Note**: The **Tax Amount** field is only displayed for Paid In and Paid Out Cash Office Activities.|
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

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
|Add Activity|Click to add a Cash Office Activity to the Business period. When clicked, the Activities screen is displayed, and you can select an activity, enter the relevant details, and add the activity to the Business period.<BR>**Note**: The **Add Activity** and **Declare** links are disabled for users assigned to a role prohibited from performing Cash Office Activities on a past date.<br><BR>The Roles prohibited from performing Cash Office Activities on a past date are configured via the ProhibitedRolesForPastDatesInCashOfficeActivities parameter in the OfficeBusinessConfigurationMaintenanceRequest RTI.|
|Declare|Click to declare the undeclared accounts in the Business Period. When selected, the Activities/Till Declaration form is displayed. You can declare the account as required.|
|Approve All|Click to approve all the balanced accounts in the selected Business Period.|
|Settle|Click to settle the selected Business Period.|
|Approved|Indicates that the Business Period was approved.|
|Started|The date from which the Business Period started. The date is a hyperlink which opens the Edit Till/Cashier Business Period depending on the accountability method used in the store.|
|End by|The date on which the Business Period ended.|
|Unbalanced accounts|The number of **unbalanced accounts** out of the **total number of accounts** in the Business Period. Unbalanced accounts have either an over or short amount.<BR>An **over amount** means that the declared Tender is greater than the calculated value, it is reflected as Over with a positive value<BR>A **short amount** means that the declared Tender is less than the expected value, it is reflected as Short with a negative value<BR>Only active accounts, i.e., accounts linked to active Account Profiles are included in the number of Unbalanced Accounts.<BR>**Note:** Account history for the periods during which the Cash Office Account was active can be viewed even if the Account is currently linked to an inactive Account Profile.|
|Undeclared accounts|The number of undeclared accounts in the Business Periods.<BR>Only active accounts, i.e., accounts linked to active Account Profiles are included in the number of Undeclared Accounts.|
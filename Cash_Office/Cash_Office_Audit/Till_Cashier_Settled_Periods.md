## Till/Cashier Settled Periods

**Till/Cashier Settled Periods** displays the till and cashier settlements in a selected Business Period. Till Settlements are performed after a Till Pending period is approved. Cashier Settlements are performed after a Cashier Pending period is approved. This is the final step within the Till/Cashier Balancing process. Once a Till/Cashier Settlement is performed, the accountability of the money is transferred from the Till/Cashier to the Safe.

**Reference Path:** *Cash Office/Cash Office Audit/Till/Cashier Settled Periods*

![Till/Cashier Settled Periods Screen](/Images/TillCashierSettledPeriodsScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Store**|The store in which to view settled Till/Cashier Business Periods.|
|**Started**|The date and time from which you want to view settled Business Periods.|
|**End By**|The date and time up to which you want to view settled Business Periods.|
|**Business Periods**||
|Approved|Indicates that the business period is approved.|
|Started|The Business Period starting date. The date is a hyperlink which opens the Till Business Period or Cashier Business Period depending on the accountability method used in the store.|
|End By|The date the Business Period ended.|
|Settlement Date|The date and time at which a business period was settled.|
|Unbalanced accounts|The number of unbalanced accounts from the total number of accounts in the Business Period. Unbalanced accounts have either an over or short amount.<BR>For example:<BR>**Over** – indicates that the declared Tender is greater than the calculated value, it is reflected as Over with a positive value<BR>**Short** – indicates that the declared Tender is less than the expected value, it is reflected as Short with a negative value|
|Undeclared accounts|The number of undeclared accounts from the total number of accounts in the Business Period.|

### View Till Business Period

View Till Business Period is used to view the approved Till/Cashier settled Business Periods.

**Reference Path:** *Cash Office/Cash Office Audit/Till/Cashier Settled Periods/Till/Cashier*

|**Field**|**Description**|
|---------|----------|
|**Store**|The store for which the Till Business period was performed.|
|**Started**|The date from which the Business Period started.|
|**End by**|The date on which the Business Period ended.|
|**Business Periods**||
|Account|The touchpoint account in the Touchpoint Group.  The hyperlink opens the Till Transactions. See also: Till Transaction.|
|Opening Amount|The money that came in from sales, loans, Paid-in's, etc.|
|Expected Amount|The money that was taken out of the touchpoint by pickups, paid-out, etc.|
|Declaration|The actual amount of money counted that currently resides in the till.<br>**Note:** The Description column can be hidden based can be hidden/displayed by configuration via the OfficeBusinessConfigurationMaintenance RTI.|
|Over / Short|The actual over/short amount in each touch point account. For example:<BR>Over amounts have a red up arrow ![Red Up Arrow](/Images/reduparrow.png) and a positive number with the text “(Over)” next to the amount.<BR>Short amounts have a red down arrow ![Red Down Arrow](/Images/reddownarrow.png) and a negative number with the text “(Short)” next to the amount.<BR>Balanced accounts have the text “Balanced” in green.|
|Approve|Indicates that the account is approved. Accounts are approved only when balanced or when the Over/Short amount has been approved. When approving an Over/Short amount, a reason must be given. Once an account is approved, the user can perform a settlement to balance the period.|
|Reason|The reason for the over/short amount. A reason must be entered before a short or over business period can be approved.|
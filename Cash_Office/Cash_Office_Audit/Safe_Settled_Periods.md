## Safe Settled Periods

**Safe Settled Periods** display the safe settlements in a selected Business Period. Safe Settlements are performed after a Safe Pending period is approved and is the final step within the Safe Balancing process.

**Reference Path:** *Cash Office/Cash Office Audit/Safe Settled Periods*

![Safe Settled Periods Screen](/Images/SafeSettledPeriodsScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Store**|The store in which to view settled Till/Cashier Business Periods.|
|**Started**|The date and time from which you want to view settled Business Periods.|
|**End By**|The date and time up to which you want to view settled Business Periods.|
|**Business Periods**||
|Approved|Indicates that the Business period is approved.|
|Started|The Business Period starting date. The date is a hyperlink which opens the View Safe Business Period depending on the accountability method used in the store. See also: View Safe Business Period.|
|End By|The date the Business Period ended.|
|Settlement Date|The date and time the business period was settled.|
|Unbalanced accounts|The number of unbalanced accounts from the total number of accounts in the Business Period. Unbalanced accounts have either an over or short amount.<BR>For example:<BR>**Over** - Declared amount is greater than the calculated value, shown as positive.<BR>**Short** - Declared amount is less than the expected value, shown as negative.|
|Undeclared accounts|The number of undeclared accounts from the total number of accounts in the Business Period.|

### View Safe Business Period

Settlement periods for safe accounts. Safe Balancing can be performed for the entire Touchpoint Group or for a single account in the group.

**Reference Path:** *Cash Office/Cash Office Audit/Safe Settled Periods/Safe Settled Periods*

|**Field**|**Description**|
|---------|----------|
|**Store**|The store for which the Till Business period is shown.|
|**Started**|The date from which the Business Period started.|
|**End by**|The date on which the Business Period ended.|
|**Accounts**||
|Account|The Safe account. The date is a hyperlink which opens Safe Transactions to view the details of the accounts in the Business Period. See also: Safe Transaction.|
|Opening Amount|The money that came in from Tender pickup, Paid in, Bank receipts etc.|
|Expected Amount|The money that was taken out of the safe by pickups, paid-out, etc.|
|Declaration|The actual amount of money counted that currently resides in the safe.<BR>**Note:** The Description column can be hidden based can be hidden/displayed by configuration via the OfficeBusinessConfigurationMaintenance RTI.|
|Over / Short|The actual over/short amount in each safe account. For example:<BR>Over amounts have a red up arrow ![Red Up Arrow](/Images/reduparrow.png) and a positive number with the text “(Over)” next to the amount.<BR>Short amounts have a red down arrow ![Red Down Arrow](/Images/reddownarrow.png) and a negative number with the text “(Short)” next to the amount.<BR>Balanced accounts have the text “Balanced” in green.|
|Approve|Indicates that the account is approved. Accounts are approved only when balanced or when the Over/Short amount has been approved. When approving an Over/Short amount, a reason must be given. Once an account is approved, the user can perform a settlement to balance the period.|
|Reason|The reason for the over/short amount. A reason must be entered before a short or over business period can be approved.|

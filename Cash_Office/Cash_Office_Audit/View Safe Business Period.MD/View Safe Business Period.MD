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
|Over / Short|The actual over/short amount in each safe account. For example:<BR>* Over amounts have a red up arrow ![Red Up Arrow](/Images/reduparrow.png) and a positive number with the text “(Over)” next to the amount.<BR>* Short amounts have a red down arrow ![Red Down Arrow](/Images/reddownarrow.png) and a negative number with the text “(Short)” next to the amount.<BR>* Balanced accounts have the text “Balanced” in green.|
|Approve|Indicates that the account is approved. Accounts are approved only when balanced or when the Over/Short amount has been approved. When approving an Over/Short amount, a reason must be given. Once an account is approved, the user can perform a settlement to balance the period.|
|Reason|The reason for the over/short amount. A reason must be entered before a short or over business period can be approved.|

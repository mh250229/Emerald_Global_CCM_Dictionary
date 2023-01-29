## Manual Approvals

**Manual Approvals** allows cashiers to manually postpone the EOD (end of day) process for 24-hour stores. This is for situations in which EOD is about to start and there are still customers waiting in the queue, or when EOD starts and the cashier is in the middle of a transaction.

To include the transactions in the current business day or not keep a customer waiting, the cashier can postpone the EOD process up to a defined number of minutes, after which a timeout is triggered enabling the cashier to complete the transaction. Once the timeout is reached, the EOD process is automatically executed.

You can define the touchpoint groups from which manual approval is allowed, as well as the timeout to indicate that after a defined number of minutes, EOD automatically starts.

**Reference Path:** *Financial/Business Day/Manual Approvals*

![Manual Approvals Screen](/Images/ManualApprovalsScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Location**|The store in which you allow the option of manually postponing an EOD process.|
|**Touchpoint Groups**|The touchpoint group from which manual approval is allowed.|
|**Timeout Duration (minutes)**|The number of minutes after which a timeout is reached and EOD automatically starts. Once the defined period is reached EOD is automatically executed.|
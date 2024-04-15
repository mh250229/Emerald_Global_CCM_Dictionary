## Business Day Scheduler

**Business Day Scheduler** schedules the EOD (end of day) process. EOD schedules specify the weekdays and times on which EOD is executed, giving the retailer the flexibility to run EOD daily, on specific days, or once a week etc. In addition, cashiers can manually postpone the EOD process when the EOD is about to be executed and there are still customers waiting. To include transactions from the current business day, the cashier can postpone the EOD process up to a defined number of minutes, after which a timeout is triggered.

The End of Day (EOD) process closes the business day or business period.  EOD is automatically executed according to the business period configured. A 24-hour business period is according to the business period configuration.

**Scenario:**

The store has 10 touchpoints (POS terminals).

EOD is defined to be executed daily at 11.59 pm on all touchpoints.

A manual approval timeout period of 30 minutes is defined for the Touchpoint Group linked to touchpoint # 10.

**POS Flow:**

* EOD is executed at 11.59.
* Touchpoints 1 to 9 are not active and EOD is executed.
* On touchpoint 10, the cashier is in the middle of a transaction. At the end of the transaction, a message is displayed, prompting the cashier to approve the EOD that is about to run.
* The cashier has 2 customers waiting in the queue and selects to postpone the EOD procedure.
* At the end of the next transaction, the message is prompted again. The cashier still has a customer in the queue, and again selects to postpone the EOD process.
* At the end of the next transaction, the message is prompted again. It has only been 15 minutes since the first message.

The cashier approves the message and EOD starts.

Once the EOD process was executed, the following activities take place:

* The next business date is set.
* A record of the date and time on which EOD was run is written to the Tlog.

**Reference Path:** *Financial/Business Day/Business Day Scheduler*

![Business Day Scheduler Screen](/Images/BusinessDaySchedulerScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Location**|The store for which the EOD schedule is defined.|
|**Exceptions**|The exceptions defined for the End of Day schedule.|

**Reference Path:** *Financial/Business Day/Business Day Scheduler/Add New*

![Business Day Scheduler Form](/Images/BusinessDaySchedulerForm.png)

|**Field**|**Description**|
|---------|----------|
|**Location**|The store or location for which the EOD schedule is located.|
|**Business Period Configuration section**|Defines the Till and Safe Business periods are defined according to the EOD Schedule.|
|Mode|To specify if the Till and Safe business periods are linked to the defined EOD Schedule.<BR>The options are:<BR><BR>* **Manual** - indicates that the Till and/or Safe business periods are not linked to the defined EOD Schedule, and are manually defined.<BR>* **Linked to EOD** - indicates that Till and/or Safe balancing is performed according to the defined EOD Schedule. When creating a new business period in the Cash Office module, the End Date field is populated with the date and time of the last scheduled EOD linked to the business period.|
|Reoccurrence Pattern|The days and times on which EOD is scheduled to be performed.
|Days of the week (Monday-Sunday)|The day and time of the week on EOD is run. From the drop-down list next to the day, select the time on which EOD runs on the specified day.<BR>For example, if you want EOD to run on Monday, from the drop-down list, select the time at which EOD starts.<BR>**Note:** The selected date and time defines when the business period begins, however, the business period opens only after the first transaction is performed. For example, if a business period begins on Monday at 11.00, and the cashier performed the first transaction only at 12.00, the business period opens at 12.00.<br><BR>If no transactions were performed during an entire business period, for example, the store was closed on Sunday 2.2.2014, but EOD was run and a business period created, and the first transaction was only performed on Monday 2.3.2014, then the two business periods are combined.<BR>On viewing the pending business periods, one pending business period is displayed. The Start Date is 2.2.2014 and the End Date is 3.2.2014.|
|**Next Day**|Indicates that the selected EOD only runs at the defined time the next day. If your store runs EOD daily and the store closes after midnight, you will need to select the Next Day checkbox for each day on which EOD is run.|
|**Action**|Indicates if the EOD is run or not. The options are:<BR><BR>**Execute** - to specify that EOD is to be run on the defined day<BR>**Ignore** - to specify that EOD is not run on the defined day|
|**Business Period Schedule**|The business periods linked to the defined EOD schedule.<BR>The options are:<BR><BR>**Till** – specifies that a Business period is automatically created only for Tills, and the safe business period continues to be maintained manually.  A Till Business Period can only be linked to a day that has an active EOD execute. The Till Business period is created and saved automatically when EOD is executed.<BR>**Till & Safe** – specifies that a business period is created for both Tills and Safes. A Safe business period can only be created when a Till business period is created. The scope of the collected data for a business period ranges from the first transaction created after the previous business period’s end date and time, to the last completed transaction before the current EOD actually runs<BR>**Note:**  The Business Period Schedule area is enabled only when the Linked to EOD option is selected.|
|**Current Exceptions section**|Defines the exceptions to the EOD Schedule defined in the Reoccurrence Pattern. This enables the store to specify that EOD will/will not run on a specific day/s and times.<BR>For example, EOD is scheduled to take place at 24:00. You can define an exception so that EOD will not run on a specific day or will run at another time on the specified day.|
|Date|The date on which you want to make an exception in the EOD Schedule. For example, if EOD is scheduled to run every day and you do not want the EOD to run on a specific day or you want to run EOD at a different time.<BR>Use **Recurring** to have the exception reoccur annually.|
|Recurring|Indicates that exception is reoccurs on the selected date.|
|End-of-Day New Time|The time the EOD will run on the selected date.|
|Next Day|Indicates that the selected EOD only runs at the defined time the next day.<BR>The Next Day option provides the ability to include the full business date’s transactions in the EOD, even if transactions are performed in consecutive system dates. For example, your store operates from 08:00am to 01:00am, and EOD is set to run on Monday at 01:00, and the Next Day checkbox is selected. In this scenario EOD is executed on Tuesday at 01:00 for Monday’s business date’s transactions. If the Next Day checkbox was not selected, EOD would be executed on Monday at 01:00, which means no transactions were yet performed on the Monday. If your store runs EOD on a daily basis, and the store closes after midnight, you would need to select the Next Day checkbox for each day on which EOD is run.|
|Execute / Ignore|Indicates if the EOD is run or not.<BR>The options are:<BR><BR>**Execute** - to specify that EOD is to be run on the defined day.<BR>**Ignore** - to specify that EOD is not run on the defined day.|
## Update Till/Cashier Period End Date

**Update Till/Cashier Period End Date** enables retailers to manually close a business period without affecting the original business schedule.  
For example, the store business period is scheduled to run between Monday to Friday. The EOD process is scheduled to run at 22.00 on Friday.

![grid screen](/Images/UpdateTillCashierPeriodEndDategridscreen.png)

* Due to an operations issue, the retailer decides to manually close the business period at 17.00 on Wednesday. 
* For that week only there will be two business periods- one from Friday -Wednesday, and one from Thursday to Friday.

The following week, the business periods are still closed according to the original business schedule.

**Reference Path:** *Cash Office/Business Periods/ Update Till/Cashier Period End Date*

![Update Till/Cashier Period End Date screen](/Images/UpdateTillCashierPeriodEndDatescreen.png)

|**Field**|**Description**|
|---------|----------|
|**Store**|The store in which the Business period is manually closed|
|**Default Date**|The date on which the business period was due to close defined in business day scheduler|
|**Current Till Closing Date**|The date on which the business period is manually closed.<BR>The Till Closing Date is set between the current date and the Default Date.<BR>In the Business Day Scheduler module, if the Action set for the Business period is set to ‘Ignore’ and an ‘Execute’ exception is defined for that date, the current date can be selected if the EOD has not yet run.<BR>The Till Closing Date cannot be set to:<BR>* A past date (before the current system date)<BR>* After the current defined business period date (Default date)<BR>* A date on which an EOD is not linked, including dates on which the linked EOD is set to ‘Ignore’.<BR>The date manually selected in the **Current Till Closing Date** field can be changed back to the original till scheduled date.|

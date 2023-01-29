### Alerts Monitoring

**Alerts Monitoring** monitors the alerts that were triggered at the touchpoint. You can monitor alerts in specific stores, alert groups, and time periods.

**Alerts Monitoring** enables you to view the touchpoint on which the alert was triggered, the user who triggered the alert, the message prompted when the alert is triggered, as well as the date and time the alert was triggered and more.

The system enables you to receive notification regarding any alert, either manually triggered at the POS, or automatically triggered by the system.

In addition, the following specific peripheral devices alerts may be sent:

* Printer:
    * Out of paper
    * Almost out of paper

* Scale:
    * Overweight
    * Underweight

However, a generic error is sent for the MSR/Drawer/Scanner

Each alert has a code which can be recorded, documented and monitored. Users must be assigned to user roles with permissions to maintain and monitor alerts.

The Alerts Monitoring screen is associated with the business activity. Only users with the permission to modify alerts can edit or delete alerts.

**Note:** The system records all alerts in the database. On deleting an alert from the Alerts Monitoring screen, the alert is not deleted from the database. This can be used for reporting or monitoring reasons.

**Reference Path:** *Monitoring/System Monitoring/Alerts Monitoring*

![Alerts Monitoring Screen](/Images/AlertsMonitoringScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Business Unit**|The Business Unit where the alert was triggered.|
|**Touchpoint**|The touch points for which you want to view alerts.|
|**State**|The alert status: The options are:<BR><BR><BR><BR>**New** – indicates that the Alert was sent but not yet handled.<BR>**In Process** - indicates that the alert is being dealt with but not yet closed.<BR>**Closed** - indicates that the alert was resolved and closed.<BR>**Cancelled** - indicates that the alert was cancelled.|
|**Group**|The Alert Group to which the alert belongs.|
|**Severity**|The severity level of the alert.<BR>Alerts are prioritized according to the severity level to minimize the impact on the store operations. The severity level of each alert is assigned when the alert is created. Severity levels range from critical to no immediate impact|
|**From**|The date and time from which you want to view alerts that were triggered.|
|**To**|The date and time up to which you want to view alerts that were triggered.
|**User ID**|The ID of the user who handled the alert.|
|**Free Text filter**|To search for alerts using a full or partial description of the device ID, device type, alert description, message header or body.|
|**Alerts**||
|Business Unit|The Business Unit where the alert was triggered.|
|Description|The name of the alert.|
|Group|The Alert Group to which the alert is linked. The options are:<BR><BR>**Business Alerts** – Automatically triggered alerts, for example when a promotion fails to load on the POS.<BR>**Peripheral Device** - Alerts triggered by a touchpoint’s peripheral device, for example when a printer runs out of paper.<BR>**POS Manual Alerts** - Alerts manually triggered at the POS by the cashier, for example Cashier needs a break.|
|Severity|The severity level of the alert.  Alerts are prioritized according to the severity level assigned when the alert is created. Severity levels range from critical to no immediate impact.|
|Date|The date and time the alert was triggered.|
|State|The alert status: The options are:<BR><BR>**New** – indicates that the Alert was sent but not yet handled.<BR>**In Process** - indicates that the alert is being dealt with but not yet closed.<BR>**Closed** - indicates that the alert was resolved and closed.<BR>**Cancelled** - indicates that the alert was cancelled.|
### Alert Template Setup

**Alert Template Setup** defines the templates for alerts which are manually triggered at the POS terminal.

An Alert Template is a set of predefined fields, which defines the severity level, the message displayed and the Alert Group.

For example, you can set up an alert template for when the cashier wishes to take a break from the POS terminal. When the alert is triggered at the POS terminal, the supervisor can view the alert in the Store Manager, and then handle the alert accordingly.

The Alert Template defines the alert severity level, as well as define the message displayed when the alert is triggered. The message is displayed in the language linked to the culture assigned in the Store Manager. For example, if the Store Manager is linked to the US Eng culture, the message is displayed in English, even when the POS the message was sent from is assigned to a different culture.

**Reference Path:** *Monitoring/System Monitoring/Alert Template Setup*

![Alert Template Setup Screen](/Images/AlertTemplateSetupScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Id**|The Alert template ID number.|
|**Group**|The Alert Group to which the alert is linked. Each Alert Group contains similar types of alerts.|
|**Severity**|The severity level of the alert. The severity level prioritizes the alerts.|
|**Grid**||
|Id|The alert ID number.|
|Description|The name/description of the alert.|
|Group|The alert group to which the alert is linked. The options are:<BR><BR>**Business Alerts** - Automatically triggered alerts, for example, when a promotion fails to load on the POS.<BR>**Peripheral Device** - Alerts triggered by a device linked to a touchpoint, e.g., when the printer runs out of paper.<BR>**POS Manual Alerts** - Alerts manually triggered at the POS by the cashier, e.g., Cashier needs a break.|
|Severity|The severity level. Alerts are prioritized according to the severity level assigned when the alert is created. Severity levels range from critical to no immediate impact.|
|Message|The message displayed when the alert is triggered.|
|Status|The status of the Alert Template. The options are:<BR><BR>**Active** – The template can be selected and applied to an alert.<BR>**Inactive** - The alert template cannot be applied to an alert.<BR>Alert Templates cannot be deleted. If you do not want to use a specific template, you must change the status to Inactive.|

**Reference Path:** *Monitoring/System Monitoring/Alert Template Setup/Add New*

![Alert Template Setup Form](/Images/AlertTemplateSetupForm.png)

|**Field**|**Description**|
|---------|----------|
|**Group**|The alert group to which the alert is linked. The options are:<BR><BR>**Business Alerts** - Automatically triggered alerts, for example, when a promotion fails to load on the POS.<BR>**Peripheral Device** - Alerts triggered by a device linked to a touchpoint, e.g., when the printer runs out of paper.<BR>**POS Manual Alerts** - Alerts manually triggered at the POS by the cashier, e.g., Cashier needs a break.|
|**Severity**|The severity level. Alerts are prioritized according to the severity level assigned when the alert is created. Severity levels range from critical to no immediate impact.|
|**Message**|The message displayed when the alert is triggered.|
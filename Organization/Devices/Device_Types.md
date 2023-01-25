## Device Types

**Device Types** categorize devices according to types.  Each device type includes error codes and the correlated alert template that is triggered on each device, as well as the methods used to handle the alert.

Once the Device Type is linked to a device, the defined attributes are automatically applied to the device. This enables retailers to apply the relevant alerts to similar type devices without configuring the alerts for each specific device.

**Reference Path:** *Organization/Devices/Device Types*

![Device Types Screen](/Images/DeviceTypesScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Name**|The name of each device type.|

**Reference Path:** *Organization/Devices/Device Types/Add New*

![Device Types Form](/Images/DeviceTypesForm.png)

|**Field**|**Description**|
|---------|----------|
|**Name**|The name of the device type (e.g. printer).|
|**Error Code**|The error code number. Error codes are numerical codes applied to specific hardware issues or device problems. For example, Error Code 1234 may indicate a Printer Out of Paper error.|
|**Alert Template Id**|The name of the Alert Template displayed when an error is triggered.<br>The Alert Template includes the message displayed when the error is triggered, as well as the severity.<br>When Error Codes are assigned to an Alert Template, an alert is raised in the **Alert Monitoring** screen when an error occurs. The alert includes the error code, device type, and device name.<br>**Note:** Error codes not assigned to an Alert Template, do not raise an alert when the error occurs.|
|**Allow Duplicate**|Indicates that a duplicated alert is raised even though the same alert was previously displayed and not yet resolved. For example, an alert was raised indicating the printer has run out of paper. If the check box is selected, an alert is raised each time the user attempts to use the printer until paper is added to the printer, and the alert is resolved and closed.<br>If the checkbox is not selected, the alert is displayed only once regardless of whether or not it is raised again.<br>**Note:** Only open alerts can be duplicated. If an alert that was Closed is raised again the alert is always displayed.|
|**Closing Method**|The method used to close the alert when the error is fixed.<br>The options are:<BR><BR>**Manual** - The error must be manually closed after it is resolved. For example, if a ‘Printer Out of Paper’ error is raised. After paper has been inserted into the printer, the alert must be manually closed.<BR>**Automatic** - Once the error is resolved, the alert is automatically closed. For example, if a ‘Printer Out of Paper’ error is raised. After paper has been inserted into the printer, the alert closes automatically.<BR><BR>**Note:** When an alert is defined to automatically close by the device and the error is resolved while the device is down, the error is automatically closed when the device is restarted.|
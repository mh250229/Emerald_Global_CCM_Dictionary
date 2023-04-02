## User Notifications

**User Notifications** are messages that notify employees in a store of important events or information.

For example, wish employees a good morning, inform cashiers of special promotions or that overtime hours are available.

The messages are displayed every time the user signs in. After reading the message, the cashier must acknowledge the message.

Messages are displayed in order of their activation period. Messages with an earlier activation period are displayed first.

User Notification messages are supported on the POS, Keyboard POS, QSR POS, and Fuel POS, and are displayed in both Selling and Training modes.

**Reference Path:** *Presentation/Store Communication/User Notifications*

![User Notifications Screen](/Images/UserNotificationsScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Name**|The name of the user notification message|
|**Business Unit**|The locations in which the user notification is displayed.|
|**Touchpoint Group**|The Touchpoint Groups in which the user notification message is displayed.|
|**Activation Period From**|The date and time from which the user notification message is displayed.|
|**To**|The date and time up to which the user notification message is displayed.|
|**Appear On**|Indicates when the user notification message is displayed at the touchpoint.<BR>The options are:<BR><BR>Sign On - the user notification message is displayed when the cashier signs on to the touchpoint.<BR>No sale mode - the message is sent at the earliest available time when the POS is not in an active transaction.|
|**User Notifications Grid**||
|Name|The name of the user notification message|
|Business Unit|The locations in which the user notification is displayed.|
|Touchpoint Group|The Touchpoint Groups in which the user notification message is displayed.|
|Activation Period|The date and time period during which the user notification message is displayed.|

**Reference Path:** *Operations/Security/User Notifications/Add New*

![User Notifications Form](/Images/UserNotificationsForm.png)

|**Field**|**Description**|
|---------|----------|
|**Name**|The name of the user notification message|
|**Store**|The locations where the user notification is displayed.
|**Touchpoint Group**|The Touchpoint Groups in which the user notification message is displayed.|
|**Appear On**|Indicates when the user notification message is displayed at the touchpoint.<BR>The options are:<BR><BR>Sign On - the user notification message is displayed when the cashier signs on to the touchpoint.<BR>No sale mode - the message is sent at the earliest available time when the POS is not in an active transaction|
|**Recurrence**|Specifies if the User Notification message is displayed each time the user signs in to the touchpoint or only one a day.<BR>The options are:<BR><BR>**Always** – the message is prompted the first time the user logs in each day<BR>**Daily** – the message is prompted each time the user logs in|
|Activation Period<BR>From  / To|The date and time period during which the user notification message is displayed.|
|Notification Header|The title of the user notification message.|
|Notification Body|The actual text displayed in the notification message. The message text can contain up to 200 characters. This field is mandatory.<BR>The notification displays up to 12 rows without a header and 10 rows with a header. Additional lines will be trimmed when displaying the message.<BR>The number of characters used in the text and the maximum number of characters allowed is displayed under the field.|
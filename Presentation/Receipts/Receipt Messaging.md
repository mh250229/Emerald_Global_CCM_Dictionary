## Receipts/Receipt Messaging

**Receipt Messaging** is used to define and format the message printed in the receipt footer. You can print free text messages, such as announcements, store opening hours, and any other communication messages relevant to the store, in the receipt footer. Different messages can be configured for different Locations and Touchpoint Groups (Primary/Secondary).

**Reference Path:** *Rules & Policies/Receipts/Receipt Messaging*
![Receipt Messaging Screen](/Images/receiptmessagingscreen.png)

|**Field**|**Description**|
|---------|----------|
|**Store**|The store in which the message is printed on the receipt.<br>On accessing the module, the ‘Customize Receipt Footer’ screen is displayed.<br>The screen includes the following fields:<br>* Store – the store in which the message is printed on the receipt.<br> * Touchpoint Type – the touchpoint type on which the transaction was performed.<br>* Touchpoint Group – the touchpoint group containing the touchpoint on which the transaction was performed.<br>* Receipt Message – the message text printed in the receipt footer. Each line in the message can contain up to 42 characters per line. There is no limit on the number of lines in the message.<br> The following formatting options are available:<br>* Bold<br>* Italics <br>* Underline<br>* Alignment|
|**Touchpoint Type**|The touchpoint type on which the transaction was performed.
|**Touchpoint Group Type**|The touchpoint group containing the touchpoint on which the transaction was performed.|
|**Receipt Message**|The message text printed in the receipt footer. Each line in the message can contain up to 42 characters per line. There is no limit on the number of lines in the message.<br>The following formatting options are available:<br>* Bold<br>* Italics<br>* Underline<br>* Alignment|
|**Clear Message**|Click to erase the message text displayed in the Receipt Message text box. The option is enabled only after text is entered in the Receipt Message text box.|
|**Save**|Click to save the message. The button is enabled when an existing message is updated. The updated message overrides the existing message in the selected Location and Touchpoint Group.|
|**Delete**|Click to delete the message. The button is enabled only if a message is defined. Once the message content is deleted, the screen remains displayed with the same Location and Touchpoint Group TPG with a blank message text box.|
|**Cancel**|Click to cancel the message. Once selected, the previously saved message is reloaded.|

## Receipts/Receipt Settings

**Receipt Settings** is used to define general receipt settings to determine how receipts are organized and printed. For example, items can be organized on the receipt according to item hierarchies, or according to the order in which items are scanned. Same items can be aggregated into line, or printed separately per line, etc.  

In addition, the receipt settings can be customized and applied to different Business Units and Touchpoint Groups.  

**Reference Path:** *Rules & Policies/Receipts/Receipt Settings*
![Receipt Settings Screen](/Images/receiptsettingsscreen.png)

|**Field**|**Description**|
|---------|----------|
|**General section**| ![Receipt Settings General Section Screen](/Images/ReceiptSettingsGeneralSectionScreen.png)|
|Offer Digital Receipt|Specifies the options to send digital receipt to the customer.<br>The options are:<br>* Never - Default value<br>* By Email<br>* By SMS<br>* By Email and SMS|
|Consider Loyalty customer printing preferences|Indicates if the cashier is prompted to ask loyalty customers their preferences to receive the receipt, e.g., Print / On demand/ E-receipt/ Text message. This enables loyalty customers to be offered an e-Receipt, even if the Offer Digital Receipt parameter is set to Never.<br>For example:<br>If there is a loyalty customer added to the transaction and the parameter is set to Yes, the system takes the customer’s preferred method of printing receipts from the Customer data. See also: Personal Details Tab.<br>If the loyalty customer is added to the transaction and the parameter is set to No, then the loyalty customer preferences are not going to be considered by the system, and the printing behavior will be as for all other customers as defined in the receipt settings.<br>When set to on, if the loyalty customer's receipt preferences are configured in the customer personal details in the Customer module, the customer is asked at the end of the transaction how they want to receive their receipt<br>When set to No, if the loyalty customer did not indicate how they want to receive the receipt, the system applies the default setting defined in the Offer Digital Receipt.|
|Empty line after each section|Indicates that a blank line is inserted between each receipt section in the receipt.|
|'Copy Receipt' Text Location|To define where the Copy Receipt text is printed on a receipt that is reprinted.<br>The options are:<br>* Header -Default<br>* Footer|
|**Items section**| ![Receipt Settings Items Section Screen](/Images/ReceiptSettingsItemsSection.png)|
|Consolidate same sale items|Indicates that the same items sold in a transaction are aggregated into one line on the receipt.|
|Consolidate same item returns|Indicates that the same items which are returned in a transaction are aggregated into one line or section on the receipt.|
|Print voided items|Indicates that items voided in a transaction are printed on the receipt.|
|Item Sorting|Specifies the order in which the items are printed on the receipt.<br>The options are:<br>* Alphabetical Order – in alphabetical order according to the item name.<BR>* Sale Order – in the order the items are sold in the transaction.|
|Item Grouping|Specifies that items are printed on the receipt grouped according to the hierarchy in which the item belongs. For example, if you have a Dairy, Fruit, Vegetables, and Grocery department. All Dairy items are printed in the Dairy group on the receipt, etc.<br>From the drop-down list, select the specific item hierarchies in each item group printed on the receipt. For example, if you have 10 item hierarchies and you want to print the items according to their assign item hierarchy, select each relevant item hierarchy.|
|**Tenders section**|![Receipt Settings Items Section Screen](/Images/ReceiptSettingsTendersSection.png)|
|Print voided tenders|Indicates that tenders voided in a transaction are printed on the receipt.|
|Print EFT payments details as a separate slip|Indicates that the details of EFT payments in the transaction are printed on a separate slip, in addition to the main printed receipt.|
|Print EFT details from third-party providers|Indicates that the EFT tender details printed on the receipt are retrieved as parameters from the third-party provider. The printed details include EFT information provided by the provider.|
|**Slip Printing section**|

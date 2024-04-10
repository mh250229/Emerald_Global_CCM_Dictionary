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
|**Slip Printing section**|![Slip Printing Section Screen](/Images/SlipPrintingSectionScreen.png)|
|Print ‘Balance Inquiry’ slip|Indicates that the system verifies the balance of the online purchase item (such as gift card) and prints the balance on the receipt. This enables customers to know the available balance on the pre-paid card before using the card as a tender.|
|Print 'Online items decline' slip|Indicates that a receipt is printed when an online item in the transaction is declined by the payment provider.|
|Print 'Item not found' slip|Indicates that a receipt slip is printed when an item is not found.<br>Items not found are sold as Department Sales, and the details are printed on the receipt. A receipt is not printed when an item is not found, and not sold in a Department sale.<br>If the system is not configured to allow the cashier to manually perform a Department Sale as a POS function, the cashier can select Department Sale from the Item Not Found screen.<br>An Unknown Item slip is always printed when configured, irrespective of if the main sale receipt printing option is configured to Never or On Demand.|
|Print 'Void transaction' slip|Indicates that a slip is printed after a transaction is voided.|
|Print 'Personal Account drawer' slip|Indicates that a slip is printed when money is deposited into a personal account.|
|Print 'Personal Account Void transaction' slip|Indicates that a slip is printed when a transaction in which money is deposited into a personal account is voided.|
|**Printing Options section**|![Slip Printing Section Screen](/Images/PrintingOptionsScreen.png)|
|Sale Transactions|Specifies if the printing options for sales transactions.<br>The options are:<br>* Aways – a sales receipt is always printed.<br>* Never – a sales receipt is never printed.<br>* On Demand – a sales receipt is printed only if the customer requests to receive a receipt.|
|Return Transactions|Specifies if the printing options for return transactions.<br>The options are:<br>* Aways – a return receipt is always printed.<br>* Never – a return receipt is never printed.<br>* On Demand – a return receipt is printed only if the customer requests to receive a receipt.|
|![+ Custom Settings](/Images/addcustomsettingsbutton.png)|Click to define receipt settings for different Business Units and Touchpoint Groups.<br>When selected the Custom Settings screen is displayed. See Custom Settings Screen<br>![Custom Settings screen](/Images/customsettingsscreen.png)

### Custom Settings Screen

The Custom Settings screen enables users to define receipt settings for specific Business Units and Touchpoint Groups.

**Reference Path:** *Rules & Policies/Receipts/Receipt Settings/+ Custom Settings*
![Custom Settings screen](/Images/customsettingsscreen.png)

On selecting, ![Custom Settings screen](/Images/plusaddcustomsettingsbutton.png), the following fields are displayed:

 ![Add Custom Settings screen](/Images/newcustomsettingsscreen.png)

 View the fields as follows:

|**Field**|**Description**|
|---------|----------|
|**Name**|The name of the receipt settings customized for the selected Business Unit.|
|**Location**|The Business Unit the receipt settings are defined for.
|**Touchpoint Group**|The Touchpoint Group the receipt settings are defined for.|
|**Customized Settings**|Displays a list of the receipt setting parameters that can be customized for the selected Business Units.<br>Only the following parameters can be customized:<br>* **General** - Consider Loyalty customer printing preferences, ‘Copy Receipt’ text location.<br>* **Items** – Consolidate same sale items, Consolidate same item returns, Print voided items.<br>* **Slip Printing** – Print 'Void transaction' slip<br>* **Printing Receipt Options** – Sales Transactions, Return Transactions<br><br>From the drop-down list, select the relevant parameter. The parameter is displayed in the Customized Settings field. On closing the drop-down list, the selected parameters are displayed. The user can then configure the parameters as required.<br>For example, on selecting the General checkbox, the parameters in the General section are displayed as follows<BR>![Custom Settings General checkbox](/Images/CustomSettingsGeneralSection.png)<br>On saving the parameter configuration, the receipt settings are only applied to the selected Business Unit and Touchpoint Group, (if selected).|
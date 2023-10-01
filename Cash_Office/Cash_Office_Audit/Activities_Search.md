## Activities Search

**Activities Search** monitors cash office activities between accounts for specific stores and Cash Office activities. The module includes a enhanced search function, enabling you to retrieve a log of cash office activities performed in a specific store, during a defined period, and then drill down to view the details of each activity.

**Reference Path:** *Cash Office/Cash Office Audit/Activities Search*

![Cash Office Activities Search Screen](/Images/CashOfficeActivitiesSearchScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Store**|The store in which you want to search for the cash office activity.|
|**Activity Name**|The cash office activities you want to view. By default all the activities are selected. If the search results exceed 300 transactions, a message to narrow down the search criteria is displayed.|
|**Account**|The cash office account in which the activity is performed. Only active accounts, i.e., accounts linked to active Account Profiles can be selected|.
|**User**|The user who performed the activity.|
|**Touchpoint ID**|The touchpoint whose activities you want to view.|
|**Start Business Date**|The date from which you want to view the cash office activity.|
|**End Business Date**|The date up to which you want to view the cash office activity.|
|**Monetary Adjusted Transactions Only**|Indicates that only Cash office activities in which at least one adjustment was performed are retrieved and displayed in the Cash Office Activities Log grid.|
|**Cash Office Activities Log**||
|Transaction Date|The date and time the cash office transaction was performed.|
|ID|The ID of the cash office activity transaction. The ID is a hyperlink that opens a the general and tender details of the cash office activity.|
|User|The name of the user who performed the transaction.|
|Reference|The activity reference defined when performing the activity.|
|Activity Name|The name of the cash office activity.|
|From Account|The account from which money for the defined activity is transferred.|
|To Account|The account to which money for the defined activity is transferred.|
|Total Amount|The amount recorded in the cash office activity.|
|Over / Short|The over or short amount declared for the activity.|

**Reference Path:** *Cash Office/Cash Office Audit/Activities Search/ Cash Office Activities Log/Id*

![Cash Office Activities Log Id Screen](/Images/CashOfficeActivitiesLogIdScreen.png)

|**Field**|**Description**|
|---------|----------|
|**General**||
|Store|The name of the store in which the cash office activity was performed.|
|Activity Name|The name of the cash office activity.|\
|Id|The ID of the cash office transaction.|
|From Account|The account from which money was transferred.|
|To Account|The account to which money was transferred.|
|Business Date|The business date the transaction was performed on.|
|Total Converted Amount|The total amount of money (foreign currency) after the amount is converted into the local currency for the activity.|
|Reference|The activity reference defined when performing the activity.|
|Tax Amount|The tax amount applied in the Cash Office Activity.<BR>If the Tax Amount is based on a Tax Rate, the  ![Tax rate icon](/Images/taxrateicon.png) icon is displayed.<BR>On clicking the icon, the Tax Rates screen is displayed. See also: Tax Rates.|
|**Additional Info**|Displays additional information relevant to Cash Office Activities, for example, the name of a second cashier who counted the Safe amounts in a Bank Deposit.<BR>This field is displayed based on the configuration of the **AdditionalInfo** parameter in the CashOfficeActivityConfigurationMaintenanceRequest RTI.<BR>The configuration options are:<BR>* Optional – the Additional Info field is displayed as optional.<BR>* Mandatory - the Additional Info field is displayed as mandatory.<BR>* Not Required - the Additional Info field is not displayed.|
|**Tenders**||
|Transaction Date|The date on which the transaction was performed.|
|User Name||The name of the user who performed the transaction.|
|Total Amount|The total amount of each denomination type recorded in the Cash Office Activity.|
|Amount|The amount recorded in the transaction.|
|Adjusted|Indicates if the tender amount recorded was adjusted. For example, in order to balance the business period or if the wrong amount was keyed in.<BR>**Note:** Only the amounts for Tender Loan, Tender Pickup, Paid In, and Paid Out activities can be adjusted.|
|Reason|The reason the cash office activity was adjusted.|
|**Denominations**||
|Type|The list of banknotes and coins issued for the selected currency.|
|Denomination|The value of each banknote and coin.|
|Units|The number of each denomination type recorded in the Cash Office Activity.|
|Total amount|The total amount of each denomination type recorded in the Cash Office Activity.|
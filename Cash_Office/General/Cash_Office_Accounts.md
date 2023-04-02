## Cash Office Accounts

**Cash Office Accounts** is used to set up a list of accounts used to perform activities with the different media that is transferred in or out of the store, and within the store.  This option enables the user to reference the source and target of the cash office activities being performed.

Each account can be linked to a selected account profile, which includes the permitted cash office activities, and the locations in which the defined account is active.

For example, the Store Safe account can be used as the target and source for all activities, except for Till/POS Declarations, whereas the Bank account can only be used for Bank Deposits or Bank Receipts.
In addition, you can map a touchpoint group to a Safe Account, specifying that all money received and removed from the touchpoints in the associated Touchpoint group is transferred to and from a specific safe.

**Reference Path:** *Cash Office/General/Cash Office Accounts*

![Cash Office Accounts Screen](/Images/CashOfficeAccountsScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Name**|The name of the cash office account, e.g., Income 23. The account name must be unique, however you can define the same account name in different stores for the same account profile.<BR>**Note:** When defining the name of a Cash Office Till account, the Till number is included in the name. This enables users to easily locate a Till by the Till ID number, and not the actual computer name.<br>Till numbers must be unique per store, in order to apply the same Till number in different stores.<BR>Example: A Till touchpoint is defined for Store A.<BR>The Till number is 12. When creating a new Cash Office Account for the Till, the Account Name is Till 12.|
|**Account Profile**|The cash office account profile defining the cash office activities which can be performed with this cash office account and the locations where it is active.<BR>**Note:** Account Profiles are mandatory when creating a new Cash Office Account. 
|**Tender Loan Mapping**|The touchpoint group linked or mapped to the safe account. Each safe account is linked to a profile, either Main Safe or Change Safe. On performing the Cash Office Activity defined in the safe profile, the selected touchpoint group receives and transfers money only to the mapped safe.<br>For example, the Change Safe is used to transfer Tender Loan amounts, and the Till Touch Point group is mapped to the Change Safe.  All tender loan amounts added to the Tills are transferred to and from the Change Safe.|
|**Tender Pickup Mapping**|The touchpoint group linked or mapped to the safe account. Each safe account is linked to a profile, either Main Safe or Change Safe. On performing a tender pickup, the selected touchpoint group transfers money only to the mapped safe.<br>For example, the Change Safe is used to transfer Tender Pickup amounts, and the Till Touchpoint group is mapped to the Change Safe. All tender pickup amounts received from the Tills are transferred to the Change Safe.<br>When mapping a touchpoint group to a Safe Account, you can map the account to a Primary and Secondary touchpoint group.|
|**Open Loan Mapping**|The touchpoint group linked or mapped to the safe account. Each safe account is linked to a profile, either Main Safe or Change Safe. On performing an open loan, the selected touchpoint group receives money only from the mapped safe.<br>For example, the Change Safe is used to transfer Open Loan amounts, and the Till Touchpoint group is mapped to the Change Safe.  All open loan amounts added to the Tills are transferred from the Change Safe.<br>Cash Office activities can only be mapped to one touchpoint group, if no mapping is defined for a certain combination of transaction types and touchpoint groups, by default, the first safe is selected for the touchpoint group.|
|**System Pickup Mapping**|The touchpoint group linked or mapped to the safe account. Each safe account is linked to a profile, either Main Safe or Change Safe. On performing a system pickup, the selected touchpoint group transfers money only from the mapped safe.<BR>For example, the Change Safe is used to transfer system pickup amounts, and the Till Touchpoint group is mapped to the Change Safe.  All system pickup amounts received from the Tills are transferred from the Change Safe.<BR>Cash Office activities can only be mapped to one touchpoint group, if no mapping is defined for a certain combination of transaction types and touchpoint groups, by default, the first safe is selected for the touchpoint group.|
|**Description**|A description of the cash office account, e.g., Income account.|
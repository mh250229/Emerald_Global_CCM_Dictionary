## Tender Rounding Rules

**Tender Rounding Rules** configure rounding rules used to round tender amounts to the nearest multiple of the minimum currency unit defined for the tender, i.e., the lowest currency denominator.

Rounding up or down is determined by the Rounding Threshold. If the remainder exceeds the rounding threshold, the amount is rounded up to the nearest lowest currency unit. If not, the amount is rounded down.

For example, rounding rules are defined for the Cash tender as follows:

* The lowest currency denomination is $0.05.
* The Round-down threshold is $0.03.  
If the last digit in the cent amount after the decimal point is less than or equal to 3, the cash amount is rounded down.  
If the last digit in the cent amount after the decimal point is more than 3, the amount is rounded up.  
If the customer purchases items for $15.43, the system rounds the amount up to $15.40.

Rounding rules are connected to a tender. Each rounding rule is associated to a Rounding type tender, which defines the rule’s currency and stores the rounding amount calculated by the rounding rule.

Rounding tenders are recorded in Tlog, and displayed on the receipt, POS screens and in the Electronic Journal.

Different rounding rules can be defined for the same tender in different business units and touchpoint groups

**Reference Path:** *Financial/Tendering/Tender Rounding Rules*

![Tender Rounding Rules Screen](/Images/TenderRoundingRulesScreen.png)

|**Field**|**Description**|
|---------|----------|
|Rule Name|The rounding rule name.|
|Rounding Tender|The name of the rounding tender used to accumulate the rounding amount calculated by the rounding rule.  For example, if the sale balance due is $99.99 and the customer pays $100.00, the rounding tender will hold the single cent which is not given as change.|
|Lowest Currency Denominator|The lowest denomination of the tender.|
|Round Down Threshold|The amount up to which the tender is rounded down to the nearest lowest currency denomination.|
|Different For Refund|Indicates if the rounding rules applied to the tender when refunding the tender to a customer.<BR>The options are:<BR><BR>Yes – indicates the same rounding rule configuration is applied in refund transactions.<BR>No – indicates that different rounding rules are applied in refund transactions.|
|Refund Denominator|The lowest denomination of the tender when refunding the tender.|
|Refund Threshold|The amount up to which the tender is rounded down to the nearest lowest currency denomination when refunding the tender.|
|Enforce in Cash Office Activities|Specifies if the rounding rules are applied on amounts manually entered in Cash Office activities on both the POS and in the Store Office, e.g., Till/Cashier Declarations, Paid in/Out, Tender Loan/Pickup, Bank Deposit/Receipt, Safe Transfer/Declaration are enforced.<BR>The options are:<BR><BR>Yes – indicates that the cash amount manually entered must comply with the rounding rules. The system validates the amount, and if the amount does not comply an error is prompted.<BR>No – indicates that the rounding rules are not applied. The system accepts any amount entered. This is the default value.
|Enforce On Sales/Refund Activities|Specifies if the rounding rules on amounts manually entered in Sales and Return transactions on both the POS and in the Store Office, are applied.<BR>The options are:<BR><BR>Yes – indicates that the amount manually entered must comply with the rounding rules. The system validates the amount, and if the amount does not comply an error is prompted.<BR>No – indicates that the rounding rules are not applied. The system accepts any amount entered. This is the default value.|
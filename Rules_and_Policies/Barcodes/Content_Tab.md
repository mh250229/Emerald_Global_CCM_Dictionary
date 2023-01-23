## Content Tab

The Content tab defines the parameters for the selected data pattern type. The parameters and fields in the Content tab are dynamic and display only parameters relevant for the selected data pattern type.

**Note:** The Content tab is blank until a data pattern type is selected from the Type drop-down list.

**Reference Path:** *Rules & Policies/Barcodes/Data Patterns/Add New Data Pattern/Content Tab*

![Content Tab](/Images/ContentTab.png)

|**Field**|**Description**|
|---------|----------|
|**Parameters**|The parameters that are configured for the selected data pattern type. Once selected, the parameter fields are displayed in the right pane.<BR>Once a parameter is selected, the parameter name is grayed out.|
|**Right pane**|The attributes relevant to the selected parameter.|

### Item Data Pattern Type

The **Item** data pattern type enables you to configure the item selling information that is retrieved from the Data Pattern when scanned at the POS touchpoint.

![Item Data Patterns Screen](/Images/ItemDataPatternsScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Item Code**|The item code number.<br>**Fixed** Defines a specific item code in the data pattern. Fixed is the default value.<BR>*Fixed Value* - The item code number<BR>**Position Length** The position and length of the item code in the data pattern.<BR>*Position* - The position in the data pattern from which the item code begins in the data pattern.<BR>*Length* - The length of the item code.<BR>*Strip Leading Zeros* - Indicates that leading zeros in the item code are not considered in the validation, and the system validates the item number without the zeros.<BR>**Manipulated** Redefines an item code in a data pattern to enable the system to identify and match the item scanned in the data pattern with those defined in the Item Catalog database.<BR>For example, barcodes created by retailers, which do not comply with the Barcode Unified Standards.<BR>**Prefix** - The defined prefix to identify an Item Code.<BR>**Position** -The position in the data pattern from which the item code begins in the data pattern.<BR>**Length** -The length of the item code.<BR>**Suffix** - The defined suffix at the end of the data pattern used to identify an Item Code.<BR>**Check Digit Algorithm** -The algorithm used to calculate the Price Check Digit.<BR>The options are:<BR>UPC - the Universal Product Code. All UPC barcodes include a check digit. The UPC check digit is the 12th digit in the lower-right corner of the barcode.<BR>LUHN - the Luhn algorithm is a simple checksum formula used to validate a variety of identification numbers, such as credit card numbers.<BR>NAPCD - (North American Price Check Digit) - North American POS Product Sold by Weight/Measure) – used in North America to calculate the check digit for products sold by weight/measure. These products are identified with VMN-12 where the U.P.C. Prefix is 2. The check digit is calculated using the last 4 digits of the item price.<BR>PCDV5 -(Price Check Digit Variation (Version5) - calculates the check digit using the last 5 digits of the product's price.<BR>SSCC – (Serial Shipping Container Code) - is used throughout the supply chain as an entity identifier for item tracing and internal control. The SSCC contains 18 digits starting with an extension digit and ending with a check digit. The check digit is calculated according to the GS1 mod10 algorithm for validation. The SSCC-18 check digit algorithm is used to ensure that the data is entered correctly. It is part of the data encoded into the barcode.<BR>**Note:**The SSCC is specifically used to support an item type data pattern with both the amount and quantity/weight embedded in the barcode.<BR>For example:<BR>FF CCLLL QQQQQ PPPPP X<BR>Where:<BR>FF – the barcode prefix<BR>CCLLL - the item ID<BR>QQQQQ - the item quantity in weight or units. For example, 99.999 kg. The first two digits are always KG, decimal point is before the last 3 digits (99.999 or 1000 (01000) for 1 item, 02000 for 2 items and so on.<BR>PPPPP - the item amount (limited to maximum of $999.99)<BR>X - the check digit – (SSCC Check Digit)<BR>On scanning an item at the POS with an amount/quantity embedded barcode, the POS displays the following in the Action window and EJ:<BR>-Actual Sales Unit Price (calculated from the barcode)<BR>-Extended Amount (from the barcode)<BR>-Quantity - Units (from the barcode)<BR>-Quantity - UOM (from the catalog)<BR>**Strip Leading Zeros** - Indicates that leading zeros in the item code are not considered in the validation, and the system validates the item number without the zeros.<BR>For example: If an item code is 0000123456789 and the cashier enters 123456789 at the POS terminal, the correct data of the item code is extracted by the data pattern.|
|**Item Expiration Date**|The date and time from which the item is no longer sold.<BR>**Position** The position in the data pattern from which the expiration date begins in the data pattern.<BR> **Type** The date format type used to enter the expiration date and time.|
|**Vendor Item Code**|The item code defined by the supplier.<BR>**Fixed** Defines a specific vendor item code in the data pattern. Fixed is the default value.<BR>*Fixed Value* - The vendor item code.<BR>**Position Length** The position and length of the vendor item code in the data pattern.<br>*Position* - The position in the data pattern from which the vendor item code begins in the data pattern.<BR>*Length* - The length of the vendor item code.<br>*Strip Leading Zeros* - Indicates that leading zeros in the vendor item code are not considered in the validation, and the system validates the item number without the zeros.|
|**Item Price**|The item price.<br>**Fixed** Defines the item price in the data pattern. Fixed is the default value.<br>*Fixed Value* - The item price.<br>**Position Length Decimal**<br>The position and length of the item price in the data pattern.<br>*Position* - The position in the data pattern from which the item price begins in the data pattern.<br>*Length* - The number of digits in the item price.<br>*Decimals* - The number of decimal digits in the item price.|
|**Item Amount**|The actual selling amount of the item. The item is sold based on the amount defined in the barcode, and the unit price is calculated based on the division of the amount by the quantity sold.<br>**Fixed** The item amount in the data pattern. Fixed is the default value.<BR>*Fixed Value* - The item amount.<BR>**Position Length Decimal**<br>The position and length of the item amount in the data pattern.<BR>*Position* - The position in the data pattern from which the item amount begins in the data pattern.<BR>*Length* - The number of digits in the item amount.<BR>*Decimals* - The number of decimal digits in the item amount.|
|**Item Override Amount**|The reduced item price the item is sold for after a Price Override.<br>**Fixed** The reduced item price in the data pattern. Fixed is the default value.<br>*Fixed Value* - The reduced item price.<BR>**Position Length Decimal**<br>The position and length of the reduced item price in the data pattern.<br>*Position* - The position in the data pattern from which the reduced item price begins in the data pattern.<br>*Length* - The number of digits in the reduced item price.<br>*Decimals* - The number of decimal digits in the reduced item price.|
|**Item Quantity**|The item quantity.<BR>**Fixed** The item quantity in the data pattern. Fixed is the default value.<BR>*Fixed Value* - The item quantity.<br>**Position Length Decimal**<br>The position and length of the item quantity in the data pattern.<br>*Position* - The position in the data pattern from which the reduced item quantity begins in the data pattern.<br>*Length* - The number of digits in the item quantity.<BR>*Decimals* - The number of decimal digits in the item quantity.|
|**Unit of Measure**|The Unit of Measure (UOM) by which the item is sold.<br>**Fixed** The item UOM in the data pattern. Fixed is the default value.<br>*Fixed Value* - The item UOM.<br>The values are:<br>1 (or if a value was not defined) - indicates that the UOM is Each.<br>2 - indicates that the UOM is kilogram (kg).<br>3 - indicates that the UOM is grams (gm).<br>4 - indicates that the UOM is pounds (lb).<br>5 - indicates that the UOM is liter (Ltr).<br>6 - indicates that the UOM is Imperial Gallon (UK) (imp gal.).)<br>7 - indicates that the UOM is Liquid Gallon (US) (gal.)<br>For example, when configuring a Quantity Data Pattern type, if the Fixed Value for the Unit of Measure is 2, then the item is weighed and sold per kilogram.<BR>**Position Length**<br>The position and length of the item UOM in the data pattern.<BR>*Position* - The position in the data pattern from which the item UOM begins in the data pattern.<BR>*Length* - The number of digits in the item UOM.<BR>*Strip Leading Zeros* - Indicates that leading zeros in the item UOM are not considered in the validation, and the system validates the item number without the zeros.|
|**Manufacturer ID**|The ID of the manufacturer.<BR>**Fixed** The manufacturer ID in the data pattern. Fixed is the default value.<BR>*Fixed Value* - The item quantity.<BR>**Position Length**<BR>The position and length of the manufacturer’s ID in the data pattern.<BR>*Position* - The position in the data pattern from which the manufacturer ID begins in the data pattern.<BR>*Length* - The number of digits in the manufacturer ID.<BR>*Strip Leading Zeros* - Indicates that leading zeros in the Manufacturer ID are not considered in the validation, and the system validates the item number without the zeros.|
|**Manipulated**|Redefines a manufacturer ID in a data pattern to enable the system to identify and match the manufacturer ID scanned in the data pattern with those defined in the database.<BR>**Prefix** - The defined prefix to identify a manufacturer ID.<BR>**Position** -The position in the data pattern from which the manufacturer ID begins in the data pattern.<BR>**Length** -The length of the manufacturer ID.<BR>**Suffix** - The defined suffix at the end of the data pattern used to identify a manufacturer ID.<BR>**Check Digit Algorithm** -The algorithm used to calculate the Price Check Digit.<BR>The options are:<BR>UPC - the Universal Product Code. All UPC barcodes include a check digit. The UPC check digit is the 12th digit in the lower-right corner of the barcode.<BR>LUHN - the Luhn algorithm is a simple checksum formula used to validate a variety of identification numbers, such as credit card numbers.<BR>NAPCD - (North American Price Check Digit) - North American POS Product Sold by Weight/Measure) – used in North America to calculate the check digit for products sold by weight/measure. These products are identified with VMN-12 where the U.P.C. Prefix is 2. The check digit is calculated using the last 4 digits of the item price.<BR>PCDV5 -(Price Check Digit Variation (Version5) - calculates the check digit using the last 5 digits of the product's price.<BR>**Strip Leading Zeros** - Indicate that leading zeros in the manufacturer ID are not considered in the validation, and the system validates the manufacturer ID without the zeros.<BR>For example: If a manufacturer ID is 0000123456789 and the cashier enters 123456789 at the POS terminal, the correct data of the manufacturer ID is extracted by the data pattern.|
|**Price Change Reason Code**|	The ID of the Reason Code specifying the reason the item's price was changed.
Field	Description
Fixed	The item quantity in the data pattern. Fixed is the default value.
Fixed Value - The reason code number used to indicate the reason for the price change.
Position
Length	The position and length of the Reason Code ID in the data pattern. 
Position - The position in the data pattern from which the Reason Code ID begins in the data pattern.
Length - The number of digits in the Reason Code ID.
Strip Leading Zeros - Indicates that leading zeros in the Reason Code ID are not considered in the validation, and the system validates the Reason Code ID without the zeros.
For example: If a Reason Code ID is 00234 and the cashier enters 234 at the POS terminal, the correct data of the Reason Code ID is extracted by the data pattern.

Authorization External ID	The Authorization ID received from an external provider for the item.
Field	Description
Fixed	The Authorization ID in the data pattern. Fixed is the default value.
Fixed Value - The Authorization ID.
Position
Length	The position and length of the Authorization ID in the data pattern. 
Position - The position in the data pattern from which the Authorization ID begins in the data pattern.
Length - The number of digits in the Authorization ID.
Strip Leading Zeros - Indicates that leading zeros in the Authorization External ID are not considered in the validation, and the system validates the Reason Code ID without the zeros.
Manipulated	Redefines an Authorization ID in a data pattern to enable the system to identify and match the Authorization ID scanned in the data pattern with those defined in the database. 
Prefix - The defined prefix to identify an Authorization ID.
Position -The position in the data pattern from which the Authorization ID begins in the data pattern.
Length -The length of the Authorization ID.
Suffix - The defined suffix at the end of the data pattern used to identify an Authorization ID.
Check Digit Algorithm -The algorithm used to calculate the Price Check Digit.
The options are:
	UPC - the Universal Product Code. All UPC barcodes include a check digit. The UPC check digit is the 12th digit in the lower-right corner of the barcode.
	LUHN - the Luhn algorithm is a simple checksum formula used to validate a variety of identification numbers, such as credit card numbers.
	NAPCD - (North American Price Check Digit) - North American POS Product Sold by Weight/Measure) – used in North America to calculate the check digit for products sold by weight/measure. These products are identified with VMN-12 where the U.P.C. Prefix is 2. The check digit is calculated using the last 4 digits of the item price.
	PCDV5 -(Price Check Digit Variation (Version5) - calculates the check digit using the last 5 digits of the product's price.
Strip Leading Zeros - Indicate that leading zeros in the Authorization External ID are not considered in the validation, and the system validates the manufacturer ID without the zeros.
For example: If a manufacturer ID is 000012345 and the cashier enters 12345 at the POS terminal, the correct data of the manufacturer ID is extracted by the data pattern.

Rx Number	The RX item number used to identify the item as a prescription item.
Field	Description
Fixed	The RX number in the data pattern. Fixed is the default value.
Fixed Value - The RX number.
Position
Length	The position and length of the RX number in the data pattern. 
Position - The position in the data pattern from which the RX number begins in the data pattern.
Length - The number of digits in the RX number.
Strip Leading Zeros - Indicates that leading zeros in the RX number are not considered in the validation, and the system validates the RX number without the zeros.
For example: If a RX number is 001234 and the cashier enters 1234 at the POS terminal, the correct data of the RX number is extracted by the data pattern.


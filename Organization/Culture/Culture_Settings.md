## Culture Settings

*Culture Settings* define the language, currency, date format and weights and measures used in a region or country. Different settings can be configured for different cultures. For example, the date format for English (United Kingdom) is different to the date format used by English (United States).

Once you define the culture settings, if you have a Resource file translated into the language of the defined culture, the system applies the relevant language defined in the Resource file.

Touchpoints connected to the Emerald Global Server inherit the culture settings for their specific region or country.

For example, the default language for stores in Montreal is French, and the stores are linked to the Canada(FR) culture. In addition to the language, you can specify the date format, currency, and weights and measures settings relevant to the Canada(FR) culture. The settings will be applied to each store linked to the Canada(FR) culture.

Culture settings are distributed through the system using Emerald Global’s DMS (data management services).

**Note:** Culture Settings must be defined before a store is opened. Once the store is live, Culture Settings cannot be defined.

**Reference Path:** *Organization/Culture/Culture Settings*

![Culture Settings Screen](/Images/CultureSettingsScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Business Unit**|The Business Unit to which the defined culture is assigned. If the selected Business Unit is a regional one, then all the store business units underneath it will inherit its settings, unless a store specific definition exists.|
|**Culture**|The culture assigned to the Business Unit. A culture represents the language, currency, date format, and weights and measures used in a specific region or country. On selecting a culture all the defined settings are applied.<BR>Note: Once the culture is selected, the Culture Code, and Local Currency fields are automatically populated.|
|**Culture Code**|The unique ID code for each culture. The code is a combination of an ISO 639 two-letter lowercase culture code associated with a language and an ISO 3166 two-letter uppercase subculture code associated with a country or region.|
|**Local Currency**|The name and symbol of the currency used in the selected culture.|

**Reference Path:** *Organization/Culture/Culture Settings/Add New*

![Culture Setting Form](/Images/CultureSettingForm.png)

|**Field**|**Description**|
|---------|----------|
|**Business Unit**|The Business Unit to which the defined culture is assigned. If the selected Business Unit is a regional one, then all the store business units underneath it will inherit its settings, unless a store specific definition exists.|
|**Culture**|The culture assigned to the Business Unit. A culture represents the language, currency, date format, and weights and measures used in a specific region or country.|
|**Additional Language**|The languages the cashier can select when signing in the POS in which to display the POS and Customer Displays.<br>The drop-down list displays a list of all the available languages configured in the CCM, in addition to the system default language.<br>On signing into the POS, the selected languages can be selected from the POS Login screen.<br>The system default language cannot be selected. If selected, an error is prompted.<br>If the Additional Languages are configured via RTI, they are automatically displayed in the Additional Languages field.|
|**Culture Code**|The code of the selected culture. On selecting a culture in the **Culture** field, the **Culture Code** is automatically populated and cannot be modified.|
|**Local Currency**|The local currency linked to the Culture. On selecting a culture in the Culture field, the local currency of the selected culture is automatically populated in the Local Currency field and cannot be modified.|
|**Short Date Format**|The format used to display the date. The options are:<br><br>M/d/yyyy<BR>MM/dd/yyyy<BR>d/M/yyyy<BR>dd/MM/yyyy<BR>yyyy/M/d<BR>yyyy/MM/dd<BR>yyyy/d/M<BR>yyyy/dd//MM<BR>For example, select dd/MM/yyyy to display 14 June 2012 as 14/06/2012.<BR>**Note:** When only one letter is defined in a date format for the month or day, the system does not display the leading zero, however two digit date or month values are displayed. For example, 14 June 2012 is displayed as 14/6/2012 when the d/M/yyyy format is selected.|
|**Short Time Format**|The format used to display the time. The options are:<BR>hh:mm tt - 06:30 am<BR>HH:mm - 06:30|
|**Currency Positive Pattern**|Position of the currency sign when the amount displayed is a positive value.<BR>The options are:<BR><BR>\$n<BR>n\$<BR>\$ n<BR>n \$.<BR><BR>Where $ is the currency sign and n is the amount displayed.
|Currency Negative Pattern|The position of the currency sign when the amount displayed is a negative value.<BR>The options are:<BR><BR>(\$n)<BR>-\$n<BR>\$-n<BR>\$n-<BR>(n\$)<BR>-n\$<BR>n-\$<BR>n\$-<BR>-n \$<BR>-\$ n<BR>n \$-<BR>\$ n-<BR>\$ -n<BR>n- \$<BR>(\$ n)<BR>(n \$).<BR><BR>Where $ is the currency sign and n is the amount displayed.|
|**Currency Decimal Separator**|The convention used to indicate the decimal point. Different cultures use different symbols for the decimal mark.<BR>The options are:<BR><BR>. - $10.50<BR>, - $10,50.|
|**Currency Group Separator**|The convention used to separate the numbers in groups of thousands before the decimal point.  Different cultures use different symbols for the currency group separator. In addition, you can select a convention for the Currency Group Separator that is different to the Currency Decimal Separator.<BR>The options are:<BR><br>MBR>. - 1.000.000<BR>, - 1,000,000.|
|**Volume UOM**|The unit of measure (UOM) used when selling items in the store by volume.  UOMs follow the metric or imperial system depending on the culture. When a culture is selected, all UOMs are displayed in the measuring system defined for the culture.<BR>The options are:<BR><BR>**Liter** - indicates that UOMs are based on the metric system<BR>**Gallon** - Imperial - indicates that the volume UOMs are based on the imperial (British)system<BR>**Gallon** - Liquid - indicates that the volume UOMs are based on the US customary system.<BR><BR>**Note:** Only items measured in the selected Volume UOM can be sold. For example, if Liter is selected, items measured in gallons cannot be sold.|
|**Volume UOM Precision**|Specifies the number of digits displayed after the decimal point for the Volume UOM value to indicate the volume precision level.<BR>For example, 2 indicates that the volume amount is displayed with 2 digits after the decimal point.|
|**Volume Price Precision**|Specifies the number of digits displayed after the decimal point in the price of products sold by volume to indicate the price precision level.<BR>For example, 2 indicates that the price is displayed with 2 digits after the decimal point.|
|**Temperature**|The scale used to display the temperature measurements. When a culture is selected, all temperatures are displayed in the scale defined for the culture.<BR>The options are<BR><BR>Celsius<BR>Fahrenheit|
|**Length UOM**|The unit of measure used to sell product by length. When a culture is selected, all UOMs are displayed in the measuring system defined for the culture.<BR>The options are:<br><BR>Centimeters<BR>Inches|
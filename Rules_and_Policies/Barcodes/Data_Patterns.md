## Data Patterns

**Data Patterns** define numeric patterns for the different types of **barcodes** used in items, tenders etc.

Data Patterns enable identification of any input accepted at a touch point, (e.g., a POS terminal, by scanning, swiping, or keying-in alpha-numeric characters) through any POS input peripheral (scanner, MSR, keyboard) with a specific business entity, so that the entity related business process is activated automatically.

Data Pattern functionality is provided by a layer within the Emerald Global server that supports defining metadata. The metadata is a template defining the data pattern’s content and defines the mandatory and optional fields for each data pattern type. For example, on creating a data pattern of type 'Item', if the item code is a mandatory field, this is defined in the metadata maintained in the Emerald Global server.

Emerald Global supports recognizing data patterns either by the prefix length or by a regular expression (Regex):

* Prefix Length - Identify a data pattern by the prefix length. You can define a fixed prefix or a prefix length range. After the Prefix length is defined, you specify if the data pattern is decoded, encoded, or both:

    * Encoding - defines data patterns in which the system encodes information into the data pattern, for example, a self-weight barcode printed at the customer scale. The system encodes the item’s weight when placed on the scale into the barcode. The encoding process is responsible for generating the specific barcode following a request from a specific service.

    * Decoding - defines data patterns from which information is extracted. For example, item price embedded data patterns. When an item barcode is scanned, the data such as the price, description, etc., can be identified. The decoding process is responsible for identifying the relevant business entity and forward all extracted properties to it.

* Regex - Regular Expressions (Regex) is a sequence of characters that form a search pattern. Data patterns based on Regex are recognized by a wider set of rules based on Regex standards and are used for more complex scenarios.

A data pattern includes a predefined number of digits. Each set of digits is a field that includes data with specific information. There may be more than one data pattern with the same data pattern length and the same data pattern type.

Each data pattern is set up with a validation code, identifier, and a set of fields that start in set positions within the data pattern. The data pattern recognizer can be a prefix and length or a regular expression.

Data patterns can be created with prefix ranges, and then linked to existing data patterns. For example, the Store Manager can specify that all item barcodes start with the prefix 22 and end with the prefix 23. You also have the option to group several data ranges into one pattern, avoiding multiple definitions.

Data Pattern Examples:

* Scan an item’s barcode at the POS terminal, the item is sold
* Key in the item’s barcode at the POS terminal, the item is sold
* Scan a voucher at the POS terminal, the voucher’s face value is used as a tender to pay for items
* Swipe a tender voucher / coupon during any retail transaction, the tender amount is automatically reduced from the ticket’s balance
* Swipe a credit card as payment and the ticket total is reduced by the credit card amount
* Scan a loyalty card at any stage during sale activities, the customer can be identified, and the customer details are added to the ticket enabling them to earn benefits

**Reference Path:** *Rules & Policies/Barcodes/Data Patterns*

![Data Patterns Screen](/Images/DataPatternsScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Prefix**|The data pattern prefix used to identify the data pattern.|
|**Length**|The number of digits in the data pattern.|
|**Type**|The data pattern’s type, e.g., Item, Tender, etc.|
|**Location**|The store hierarchy to which the data pattern is linked.|
|**Barcode**|The specific data pattern string.|
|**Data Patterns**||
|ID|The data pattern’s unique ID number in the system.|
|Description|The name of the data pattern.|
|Type|The data pattern’s type (item, tender etc).|
|Length|The number of digits in the data pattern.|
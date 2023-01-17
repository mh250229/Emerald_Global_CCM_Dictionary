## UPC5 Value Codes

**UPC5 Value Codes** display the predefined codes for redemption values in UPC5 coupons. UPC5 Coupons are also known as vendor coupons. On scanning a UPC5 coupon, a tender is automatically added to the transaction, which has a value according to the UPC Coupon value code. The reward is retrieved from the coupon, reducing the ticket balance accordingly. UPC5 coupons represent a promotion type. The coupon reduction amount is treated as a tender.

**UPC5 coupon barcode structure:**

* **Prefix** – Always 5 (UPC5)    [**5**] 12345 87890 4
* **Manufacturer Number** - identifies the manufacturer of the item linked to the coupon. In item UPCs, the same 5 digits reflect the manufacturer of the item. 5[**12345**] 87890 4
* **Family Code** – this is a type of item reference number assigned by the manufacturer, to group products together within a family. For example, same size items but with different flavors e.g., flavored mineral water. The Family Code is added as an attribute to a product, and once assigned, remains the same through the lifetime of that product. 5 12345 [**878**]90 4
* **Value Code** – redemption value of the coupon based on a predefined value code table. This code table is created and distributed by a joint industry coupon committee. 5 12345 878[**90**] 4

For example: Value Code 05 represents $1.40 Off, Value Code 07 represents Buy 3 or more get $1.50 Off.

**Reference Path:** *Catalog, Promotions & Marketing/Promotions/UPC5 Value Codes*


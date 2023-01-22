## Own Bag Policies

**Own Bag Policies** configures the store policy that allows customers to bring their own bags to the store and use them when checking out. An incentive discount is rewarded to the customer for each own bag they use promoting a green environment.

The Own Bag policy can be linked to a specific touchpoint group and touchpoint type. It is also linked to a non-merchandise item, which is linked to a promotion that gives the reward for own bags used by the shoppers. It can be configured to be available along the whole sale process or as a popup when moving to tender mode. In both options, during the flow on the self checkout, the shopper can enter the number of own bags they are using. Each own bag is recorded in the transaction as the non-merchandise item with the zero price. This item is linked to a promotion, which triggers the own bag discount rewarded.

In addition, within the policy, the option to specify the maximum number of own bags used is available, and this prevents fraud scenarios, where the shopper enters many bags to get a big discount. In such a scenario, an intervention is prompted.

**Reference Path:** *Rules & Policies/Rules/Own Bag Policies*

![Own Bag Policies Screen](/Images/OwnBagPoliciesScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Touchpoint Group**|The touchpoint group the Own Bag policy is applied to.|
|**Touchpoint Type**|The touchpoint group the Own Bag policy is applied to.|
|**Method of Work**|The method by which the Own Bag policy is implemented on the touchpoint. The options are:<BR>**Along the whole sale process** - The own bag functionality can be invoked at any time during the transaction, whether on a self-checkout or by the cashier on a POS touchpoint.<BR>**As a pop up when moving to Tender mode** - On moving to Tender mode, the system automatically prompts to enter the number of own bags used, or to indicate no own bags.|
|**Intervention from**|	The maximum number of re-usable bags beyond which an intervention is triggered. This value is defined in the **Intervention appears when exceeding x bags** field in the Own Bag Policy form.|
|*Enabled**|Indicates that the Own Bag functionality is enabled.|

**Reference Path:** *Rules & Policies/Rules/Own Bag Policies/Add New*

![Own Bag Policy Form](/Images/OwnBagPolicyForm.png)

|**Field**|**Description**|
|---------|----------|
|**Touchpoint Group**|The touchpoint group the Own Bag policy is applied to.|
|**Touchpoint Type**|The touchpoint type the Own Bag policy is applied to.|
|**Enable Own Bag Functionality**|Indicates that the Own Bag functionality is enabled for the selected touchpoint groups and types.|
|**Appears as product (item)**|The own bag product which is linked to a promotion. The promotion gives the reward for own bags used by the shoppers as an incentive to encourage shoppers to user their own bags.<BR>The product must be set up as a non-stock product and the price is always 0.|
|**Additional Code**|The additional item code used to sell the product. Additional codes are used when the item code at the POS is different from the product code in the Emerald Global Store Office, making it impossible to sell the item at the POS.|
|**Method of work**|The method by which the Own Bag policy is implemented on the touchpoint. The options are:<BR><BR>**Along the whole sale process** – On a POS touchpoint, the cashier can invoke the own bag functionality at any time during the transaction.<BR>On a Self Checkout touchpoint, there are two buttons called **With Own Bag** and **No Own Bag**. The transaction is started by selecting one of the options. If With Own Bag option is selected, the system prompts the shopper to enter the number of own bags at the beginning of the transaction. If No Own Bag option is selected, the shopper can continue to shop and if they decide during the transaction to use their own bags, they still have the option to select the own bag option and enter the number of shopping bags.<BR><BR>**As a pop-up when moving to Tender mode** – On a POS touchpoint, the prompt is displayed once the cashier selects OK to move to Tender mode.<BR>On the Self Checkout touchpoint, the shopper starts their transaction as a regular transaction and on moving to Tender mode, the system prompts the shopper to enter the number of own bags used, or to indicate no own bags.|
|**Intervention appears when exceeding bags**|The maximum number of bags allowed at the touchpoint. If the number of bags entered exceeds this value, an intervention is triggered.|
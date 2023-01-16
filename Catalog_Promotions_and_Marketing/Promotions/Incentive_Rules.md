## Incentive Rules

**Incentive Rules** are the rules that trigger Incentive Messages, informing the customers they are about to reach a promotion's threshold and could receive a reward if they meet the promotion conditions.

Each Incentive Rule has a threshold percentage or quantity completion condition which triggers the incentive message. For example, if the threshold is defined as 80%, on reaching 80% of the promotion condition threshold, the incentive message is displayed or printed.

For example, if the promotion Spend $50.00 and Get $10.00 Off the total ticket is defined with an incentive message, and the completion threshold is 80%, the incentive engine will trigger the message when the customer has spent $40.00 informing them that if they spend an additional $10.00, a reward is issued.

Incentive messages are used at convenience stores or at the touchpoint where the retailer wants to offer promotions, and for continuity purposes, e.g., spend $500.00 during July and get a reward. The messages are triggered when the cashier totals the ticket.

Incentive messages can only be defined for POS and self-checkout touchpoints.

Incentive Rules are only applied to promotions which are configured with an Incentive Message reward. Once the Incentive rules are identified by the Incentive Engine and validated, the incentive message is displayed.

The Incentive Message engine validates that all the rules that trigger the message are met and handles optimization. For example, the engine validates the percentage of the threshold that was met to trigger the promotion and the incentive message.

**Reference Path:** *Catalog, Promotions & Marketing/Promotions/Incentive Rules*

![Incentive Rules Screen](/Images/IncentiveRulesScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Name**|The name of the incentive rule.|
|**Locations**|The store or business unit the incentive rule is applied to.|
|**Touchpoint groups**|The touchpoint group the incentive rule is applied to.|

**Reference Path:** *Catalog, Promotions & Marketing/Promotions/Incentive Rules/Add New*

![Incentive Rules Form](/Images/IncentiveRulesForm.png)

|**Field**|**Description**|
|---------|----------|
|Name|The name of the rule.|
|Message|The Incentive Message displayed when the conditions defined in the Incentive Rule are met. Incentive Messages are linked as rewards to promotions. When the customer purchases products linked to a promotion, the Incentive Engine validates the rules linked to the message, and if the rules are met, triggers the message.|
|Location|The store or business unit the incentive rule is applied to.|
|Touchpoint group|The touchpoint group the incentive rule is applied to.
|**Conditions**||
|Define rule on threshold percentage completion of:|Indicates if a percentage of items linked to the promotion must be purchased to trigger the Incentive Message. For example, in a Buy 5 bottles of Coke, Get 1 Free promotion, if the threshold percentage is 80, then once the customer purchases 4 bottles of Coke, an Incentive message is triggered to notify the customer that if they purchase another Coke, they will receive one free Coke.<br>The percentage is defined in the Threshold Percentage field.|
|Define rule on units purchased, based on the following:|Indicates if rules defining the number of items out of the promotion threshold that must be purchased to trigger the Incentive Message. There can be different incentive thresholds for different promotion thresholds.<br>The options are:<br>**Incentive threshold** - The number of items which must be purchased by the customer to trigger the Incentive Message, in promotions in which the promotion threshold is the same as the threshold defined in the Promotion threshold field.<br>**Promotion threshold** - The number of items which must be purchased to trigger the promotions. The promotion threshold is defined when setting up a promotion.<br>For example, if the promotion threshold is 3, and the incentive threshold is 2, then the Incentive message is triggered once the customer purchases 2 items. If the promotion threshold is 4, and the incentive threshold is 3, then the Incentive message is triggered once the customer purchases 3 items.|
|**Limits section**||
|Message Limit|The maximum number of incentive messages prompted to the customer in a transaction. If the message limit is less than the actual number of incentive messages to be prompted, the system optimizes the messages as follows:<br>When there are both spend and unit promotion messages, the messages relevant to the unit promotions are prompted first.<br>When there are only spend promotion messages, the messages relevant to the highest completion percentage are prompted first.<br>For example, the following promotions are linked to incentive messages:<br>Promotion 1 - Buy 5 cans of Coke, Get 1 Free. The customer purchased 3 cans of Coke (Each Coke cost $3.00.)<br>Promotion 2 – Buy Electronics items for $100.00, Get 10% off the purchases. The customer spent $80.00.<br>Promotion 3 – Buy 4 kg Bananas, Get $5.00 Off. The customer bought 3 kg.<br>The Message Limit is 2.<br>The customer purchases:<br>3 cans of Coke $9.00<br>Radio             $80.00<br>3 kg Bananas<br>Incentive Messages are displayed for Promotion 1 and Promotion 3.|
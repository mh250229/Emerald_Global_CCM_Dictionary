### Auto-Skipped Tokens

**Auto-Skipped Tokens** shows a list of the store servers with tokens that were stuck during download and automatically skipped enabling the download to continue. For example, skip a stuck message that is preventing data from being downloaded to the store and could cause data differences.

Emerald Global defines a list of the entities for which an automatic skip stuck token is applied. If the system performs an automatic skip, a notification is raised. When the stuck token includes more than one entity, if all the entities are part of the list, automatic skip is applied. If one of the entities is not in the list, automatic skip is not applied.

The list of auto-skipped entities may include core and/or extension entities.

**Reference Path:** *Monitoring/System Monitoring/Auto-Skipped Tokens*

![Auto Skipped Tokens Screen](/Images/AutoSkippedTokensScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Business Unit**|The business unit in the store hierarchy.|
|**From Date**|The date from which the system retrieves the auto-skipped tokens.|
|**To Date**|The date up to which the system retrieves the auto-skipped tokens.|
|**Entity**|The Entity Types (using OR operation), entities must be defined to allow auto-skipping.|
|**Servers with Auto-Skipped Tokens**|The list of store servers with the auto-skipped tokens that meet the filter criteria. The list of servers is sorted by the Last Skip Date/Time in descending order and Server Name.|
|Server Name|The server on which the auto-skipped token was retrieved.|
|Business Unit|The business unit from which the auto-skipped token was retrieved.|
|Auto-Skipped Tokens|The list displays the servers where the Auto-Skipped Tokens count is more than 0.<BR>To view a list of the Auto skipped tokens for a specific server, select the row of the server, and click the value in the Auto-Skipped Tokens column.|
|Last Skip Date/Time|The latest update date/time from all auto-skipped tokens that met the filter criteria.|

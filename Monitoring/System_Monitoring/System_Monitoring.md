### System Monitoring

**System Monitoring** is used to displays the status for each server installed on the retailer's network. You can view the servers according to the health status of the server and Business Unit.

On selecting a node in the Business Unit Hierarchy tree, the servers linked to the selected node are displayed in the grid. You can then monitor and correct problematic servers.

**Reference Path:** *Monitoring/System Monitoring/System Monitoring*

![System Monitoring Screen](/Images/SystemMonitoringScreen.png)

View the fields as follows:

|**Field**|**Description**|
|---------|----------|
|**Business Unit**|Displays the store hierarchy. Once a node is selected, the aggregated server status information for the servers linked to the selected node is displayed in the grid in the right pane. The number of servers linked to the node is displayed next to the Node name in the hierarchy.<BR>**Note:** The server data is displayed according the store hierarchy, regardless of the actual location in the Retalix10 network. This provides a business oriented view of the network.|
|**Health Status**|The health status of the servers you want to monitor. For example, you can filter the server tree for all nodes with errors and identify the exact business units that did not receive all transactions. When the monitoring screen is loaded, the default filtering criteria is **With Errors**. The options are:<BR><BR>**With Errors** - to view the servers with at least one update error, not including error messages that are manually skipped and ignored. An error indicates that the DMS is not synchronizing data, and all data is stuck in the queue due to stuck tokens. Servers with errors are marked with a yellow flag near the server name. This indication will also bubble up to all hierarchies above this server.<BR>**Offline and Outdated** - to view the servers that are offline and/or are no longer connected. An offline or outdated server is marked with a red flag near the server name. This indication will also bubble up to all hierarchies above this server.<BR>**Offline** – indicates no communication between the DMS Agents, i.e., the parent server did not get a preconfigured number of heartbeats from the child node.<BR>**Outdated** – indicates that the number of days since the server was last connected exceeded the defined number of days defined in the DMS Configuration parameters. For example, a POS terminal that was used during the Christmas period and then disconnected for a period of time.<BR>**Online** - to view all the servers that are currently online<BR>**All** - to view all the servers in the system
|**Grid**|
|Status|The status of the servers linked to a store in the store hierarchy, enabling users to monitor the number of servers with and without errors.|
|Server Name|The name of the server.|
|Business Unit|The business unit the server is linked to.|
|Pending Apply|The number of tokens in the server inbox that are waiting to be applied. This includes both upload and download tokens.|
|Pending Upload|The number of tokens waiting to be sent and uploaded from this server ('Upload outbox') including the tokens that failed to be published to the upload outbox queue and are in the backup table.|
|Has Errors|Indicates if there are errors in the server, either download or upload. The options are:<BR><BR>**Yes** - indicates that there are errors<BR>**No** - indicates that there are no errors|
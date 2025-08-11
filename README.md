# ua-smartsheets

ConnectALL SmartSheets Adapter is developed as an extension to the Universal Adapter capability of ConnectALL. The adapter specifications will let the user sync a rows in a SmartSheet sheete to another endpoint using the ConnectALL Integration Hub. A common use is that an ITSM application (like JIRA) will be used to manage the sprint that consist of the features created in the smart sheet. As the feature is worked on any changes to status, priority, etc. can be synched back to the smart sheet.

Please refer to https://wiki.connectall.com/ca/latest/adapters/universal-adapter for more information

# How to use

## Import specifications
* Import smartsheets_config.zip into ConnectALL using "Install custom adapter" feature.

## Define application links
* Create an application link in ConnectALL between SmartSheets and another application of your choice.
* Navigate to `Configuration -> Connections` screen and create a new connection to SmartSheets using your SmartSheets personal access token.
* In the Entity mapping tab under Advanced Properties choose "Sync Type" as POLL
* In the field mapping tab add the field that you want to sync between the applications.

> In order to use the SmartSheets adapter you will need to get the license from ConnectALL sales team. Please reach out to sales@connectall.com for licenses and quotes.


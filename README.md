
# ua-smartsheets

The ConnectALL Smartsheets Universal Adapter is developed as an extension to the universal adapter capability of ConnectALL. This adapter will allow the user to use Smartsheets with ConnectALL. Current capabilities and limitations will be defined below.

Please refer to the [ConnectALL Tech Docs](https://techdocs.broadcom.com/us/en/ca-enterprise-software/valueops/connectall/3-5/adapters/universal-adapter.html) for more information.

If you are an existing SaaS customer, please contact Broadcom Support to enable the adapter in your environment. If you are using ConnectALL On-Premise, you may download and install this adapter in your environment. If you are not yet a customer, [please reach out to learn more](https://enterprise-software.broadcom.com/contact-us).

# Setup

## Supported Entities

This Universal Adapter currently supports the following entities:
* Sheets (Project field representation)
* Rows (Objects that are created/synced)

*Note: This Universal Adapter is provided as-is. It is tested and validated using the entities and configurations as defined. Any additional customizations are not supported and should be made at your own discretion.*

## Connection Details

* **Connection Name:** Smartsheets
* **Application Type:** Smartsheets
* **URL:** https://api.smartsheet.com *(Note: this is a different URL from app.smartsheets.com)*
* **User Name:** N/A
* **Password:** N/A
* **Application Category:** *Pick from dropdown list*
* **Time Zone:** UTC
* **Select Group:** *Set if neccessary*
* **Authentication Type:** *Pick from dropdown list*
* **API Key:** Authorization
* **API Value:** Bearer api-key-value *(Note: there is a space between Bearer and your API key)*

## Flow Filters

*If applicable enter examples for a Flow Filter*

## Example Automation

Utilize a spreadsheet in Smartsheets to track new feature requests, which can then be synced to your developers ALM (Application Lifecycle Management) tool of choice, such as Rally or Jira, as a new feature.

# Known Limitations

Field values/ids are unique to the sheet that the adapter that is configured in the automation. If you are planning to sync multiple sheets, you'll need to ensure you're mapping the correct fields for each automation. It is recommended to utilize the "User Fields" functionality within ConnectALL to have a base generic adapter (the one in this repo) that has just the needed fields for a successful initial sync, with the user adding fields as needed, per use case via the User Fields function which is accessed via the admin menu.

The concept of "Templates" are available in Smartsheets and may be worth considering creating. This would allow you to create an automation per template, so you can configure or add additional fields as needed for each template you may have users interacting with.

Not a limitation, but something to note: Pagination is not used within a single spreadsheet. This has been tested with over 1000 rows, but be aware that the spreadsheet by ID response will return all rows in a single call.

**Warning/Note:** Smartsheets has a auto-save function which can make it seem like an automation is not running, as there is a delay  before a sheet saves. You must either disable this, or know your current settings about auto-save timer/page activity to know how long it takes for a page to save and the automation to then see a record has been modified. More information here: [Smartsheets Account Settings](https://help.smartsheet.com/articles/796268-adjusting-personal-settings)

# Supporting Documentation

Third Party API Documentation: [Link to API Documentation](https://developers.smartsheet.com/)


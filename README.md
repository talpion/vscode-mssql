[![Gitter](https://img.shields.io/badge/chat-on%20gitter-blue.svg)](https://gitter.im/Microsoft/mssql)

# mssql for Visual Studio Code

Welcome to **mssql** <sup>preview</sup> for Visual Studio Code! An extension for developing Microsoft SQL Server, Azure SQL databases and data warehouses everywhere with a rich set of functionalities, including:

* Connect to Microsoft SQL Server, Azure SQL databases and data warehouses.
* Create and manage connection profiles and most recently used connections.
* Write T-SQL script with IntelliSense, T-SQL snippets, syntax colorizations, T-SQL error validations and ```GO``` batch separator.
* Execute the script.
* View the result in a slick grid.
* Save the result to json or csv file format and view in the editor.
* Customizable extension options including command shortcuts and more.

    <img src="./images/mssql-demo.gif" alt="feature demo" style="width: 640px;" />

## Using
See [the mssql extension tutorial] for the step by step guide.
* First, install [Visual Studio Code] then install **mssql** extension by pressing **f1** or **cmd+shift+p** to open command palette, select **Install Extenion** and type **mssql**.
    * For macOS, you will need to install OpenSSL. Follow the install pre-requisite steps from [DotNet Core instruction].
* Open existing file with a .sql file extenion or open a new text file (**cmd+n**) and change the language mode to SQL by pressing **cmd+k,m** and select **SQL**'. **mssql** commands and funtionalities are enabled in the 'SQL' language mode in Visual Studioc Code editor.
* Create a new connection profile using command palette by pressing **f1**, type **sqlman** to run **MS SQL: Manage Connection Profile** command. Select **Create**. See [manage connection profiles] for more information about how to create and edit connection profiles in User Settings (settings.json) file.
* Connect to a database by pressing **f1** and type **sqlcon** to run **MS SQL: Connnect** command, then select a connection profile. You can also use a shortcut (**cmd+shift+c**).
* Write T-SQL sript in the editor using IntelliSense and Snippets. Type **sql** in the editor to list T-SQL Snippets.
* Execute T-SQL script or selection of statements in the sciprt by pressing **f1** and type **sqlex** to run **MS SQL: Execute Query** command. You can also use a shortcut (**cmd+shift+e**). See [customize shortcuts] to learn about change shortcut key bindings to **mssql** commands.
* View the T-SQL script execution results and messages in result view.

## Commands
The extension provides several commands in the Command Palette for working with ```.sql``` files:
* **MS SQL: Connect** to SQL Server, Azure SQL Databases or Data Warehouse using connection profiles or recent connections.
* **MS SQL: Disconnect** from SQL Server, Azure SQL Databases or Data Warehouse in the editor session.
* **MS SQL: Use Database** to switch the database connection to another database within the same connected server in the editor session.
* **MS SQL: Execute Query** script, T-SQL statements or batches in the editor.
* **MS SQL: Cancel Query** execution in progress in the editor session.
* **MS SQL: Manage Connection Profiles**
    * **Create** a new connection profile using command palette's step-by-step UI guide.
    * **Edit** user settings file (settings.json) in the editor to manually create, edit or remove connection profiles.
    * **Remove** an existing connection profile using command palette's step-by-step UI guide.
    * **Clear Recent Connection List** to clear the history of recent connections.

## Options
The following Visual Studio Code settings are available for the mssql extension. These can be set in user preferences (cmd+,) or workspace settings ```(.vscode/settings.json)```.
See [customize options] and [manage connection profiles] for more detail.

```javascript
{
    "mssql.maxRecentConnections": 5```
    "mssql.connections":[]
    "mssql.shortcuts": {
        "event.toggleResultPane": "ctrl+alt+r",
        "event.toggleMessagePane": "ctrl+alt+y",
        "event.prevGrid": "ctrl+up",
        "event.nextGrid": "ctrl+down",
        "event.copySelection": "ctrl+c",
        `"event.toggleMagnify": "",
        "event.selectAll": "",
        "event.saveAsJSON": "",
        "event.saveAsCSV": ""
        }
    "mssql.messagesDefaultOpen": false,
    "mssql.logDebugInfo": false,
    "mssql.saveAsCSV": {
        "includeHeaders": true
        }
    "mssql.enableIntelliSense": "true",
	"mssql.intelliSense.enableDiagnostics": "true",
	"mssql.intelliSense.enableSuggestions": "true",
	"mssql.intelliSense.enableQuickInfo": "true",
    "mssql.intelliSense.lowerCaseSuggestions": "false"
}
```
## Change Log
The current version is ```0.1.5```. See the [change log] for more detail.

## Support
Support for this extension is provided on our [GitHub Issue Tracker]. You can submit a [bug report], a [feature suggestion] or participate in [discussions].

## Contributing to the Extension
See the [developer documentation] for details on how to contribute to this extension.

## Privacy Statement
The [Microsoft Enterprise and Developer Privacy Statement] describes the privacy statement of this software.

## License
This extension is [licensed under the MIT License]. Please see the [third-party notices]file for additional copyright notices and license terms applicable to portions of the software.

[the mssql extension tutorial]:https://github.com/Microsoft/vscode-mssql/wiki/getting-started
[Visual Studio Code]: https://code.visualstudio.com/#alt-downloads
[DotNet Core instruction]:https://www.microsoft.com/net/core#macos
[manage connection profiles]:https://github.com/Microsoft/vscode-mssql/wiki/manage-connection-profiles
[customize shortcuts]:https://github.com/Microsoft/vscode-mssql/wiki/customize-shortcuts
[customize options]:https://github.com/Microsoft/vscode-mssql/wiki/customize-options
[change log]: ./ChangeLog.md
[GitHub Issue Tracker]:https://github.com/Microsoft/vscode-mssql/issues
[bug report]:https://github.com/Microsoft/vscode-mssql/issues/new
[feature suggestion]:https://github.com/Microsoft/vscode-mssql/issues/new
[developer documentation]:https://github.com/Microsoft/vscode-mssql/wiki/contributing
[Microsoft Enterprise and Developer Privacy Statement]:https://go.microsoft.com/fwlink/?LinkId=786907&lang=en7
[licensed under the MIT License]:./LICENSE.txt
[third-party notices]:ThirdPartyNotices.txt

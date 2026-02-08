# Script Editor

## Overview
The Script Editor provides a comprehensive environment for writing, managing, and executing JavaScript tool scripts within the MCPStudio platform. The interface features a file browser on the left and a powerful editor on the right, allowing users to efficiently develop and test custom tools.

## Interface Components

### File Browser (Left Panel)
The file browser displays the hierarchical structure of your selected folder.

### Editor (Right Panel)
The main editing area where you can write and modify JavaScript code. The editor includes syntax highlighting, line numbers, and a clean theme for comfortable coding.

### Toolbar (Top Bar)
From left to right, the toolbar provides essential functionality:

1. **Show/Hide File Browser**: Toggle the visibility of the file browser panel on the left.
2. **New Script**: Create a new JavaScript script file.
3. **Save File**: Save the currently edited script file.
4. **Search/Replace**: Search for text within the script or replace text across the document.
5. **Run Script**: Execute the currently open script.
6. **Show/Hide Log View**: Toggle the visibility of the log output panel.
7. **Export Custom Tool SDK**: Export the current tool as a custom SDK package.
8. **Settings**: Access application settings and preferences.

## Working with Scripts

### Creating a New Script
1. Click the "New Script" button in the toolbar
2. Select the appropriate script type (e.g., tool script, data pipeline script)
3. Name your script and click "Create"
4. Start coding in the editor

### Managing Scripts
- Use the file browser to navigate through your scripts
- Click on any script file to open it in the editor
- Organize scripts into logical directories within the file browser
- Use the "Save File" button to save changes to your script

### Writing Scripts
The editor supports JavaScript syntax with features like:
- Line numbers for easy navigation
- Syntax highlighting for better code readability
- Support for JavaScript tool script functions like `toolEntry()`
- Built-in support for JSON parsing and handling

### Example Script Structure
```javascript
// Example JavaScript Tool Script for MCPStudio
/**
 * Entry point for all script tool calls
 * @param {string} sid - Session identifier
 * @param {string} handlerName - Method/handler name to execute
 * @param {string} jsonParams - JSON string with parameters
 * @returns {string} JSON result or plain text
 */
function toolEntry(sid, handlerName, jsonParams) {
    console.log("Script started - SID: " + sid + ", Handler: " + handlerName + ", JSON: " + jsonParams);
    try {
        // Parse input parameters
        var params = JSON.parse(jsonParams);
        
        // Route to appropriate handler
        switch (handlerName) {
            case "processFile":
                return processFile(params);
            case "analyzeDirectory":
                return analyzeDirectory(params);
            case "createReport":
                return createReport(params);
            case "transformData":
                return transformData(params);
            default:
                return JSON.stringify({error: "Unknown handler"}); 
        }
    } catch (e) {
        return JSON.stringify({error: e.message});
    }
}
```

### Running Scripts
1. Write your script in the editor
2. Click the "Run Script" button in the toolbar
3. The script executes with the specified parameters
4. View output in the log view (toggle with "Show/Hide Log View")

### Exporting Tools
1. For developing native tools, click "Export Custom Tool SDK"
2. Choose destination
3. The SDK package will be installed on your desired location with a subfolder **ToolSDK**

## Tips
- Use the file browser to organize your scripts logically
- Always save your work using the "Save File" button
- Utilize the search functionality to quickly locate code snippets
- Check the log view after running scripts to verify output and debug errors
- Use the settings menu to customize your editing experience

This Script Editor provides a robust environment for developing and managing JavaScript tool scripts within the MCPStudio ecosystem.

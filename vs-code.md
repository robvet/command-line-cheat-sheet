# VS Code Command Line Cheat-Sheet

## Open VS code from command line in current directory
```
code .
```
## Open VS code insiders edition from command line in current directory
```
code-i .
code-insiders .
```

##  Open VS code from command line in current directory -r option opens the folder without launching a new Visual Studio Code window
```
code . -r
```

## Reopen VS Code from current directory
```
code -r .
```

## Kill all processes in VS Code
```
taskkill /F /IM dotnet.execode -r .
```

## Add Packages
https://bobbyhadz.com/blog/vscode-install-nuget-package
```
dotnet add package <package fully qualified name> --version <version number>
```

## Build to Target Framework Version
https://learn.microsoft.com/en-us/dotnet/standard/frameworks
```
dotnet -f net6.0
```

## Create new .net app
https://learn.microsoft.com/en-us/dotnet/core/tutorials/with-visual-studio-code?pivots=dotnet-7-0
```
dotnet new console --framework <version, such as: net7.0>C:\_vet\_vetDemos\_complete\ai\rag\StepToubRag\chatapp\chatapp.csproj
```

## Add use secrets
```
dotnet user-secrets set "<key>" "<value>"
```

## VSC keyboard shortcuts
```
# Open the search bar at the top of the editor
<command> <P>

# Open left-hand bar
<command> <B>

# Open terminal window
<command> <J>

# Search with a file
<command> <F>

# Search within a project
<command> <shift> <F>

# Navigate through tabs
<command> <tab>

```

## VSCode IDE Color and Size Settings
```
# settings.json
{
    "@azure.argTenant": "72f988bf-86f1-41af-91ab-2d7cd011db47",
    "github.copilot.chat.codeGeneration.instructions": [
        {
            "text": "- @azure Rule - Use Azure Best Practices: When generating code for Azure, running terminal commands for Azure, or performing operations related to Azure, invoke your `azure_development-get_best_practices` tool if available."
        }
    ],
    "workbench.colorTheme": "Visual Studio Dark",
    "editor.fontSize": 18,
    "terminal.integrated.mouseWheelZoom": true,
    "terminal.integrated.fontSize": 30,
    "workbench.colorCustomizations": {
        "editor.background": "#002b00", // "#06402B" // Change this hex code to your preferred dark green
        "sideBar.background": "#001a00",
        "activityBar.background": "#001a00",
        "titleBar.activeBackground": "#001a00",

        // Tab Customizations
        "tab.activeBackground": "#003300",
        "tab.inactiveBackground": "#001a00",
        "tab.activeForeground": "#ffffff",
        "tab.inactiveForeground": "#cccccc",
        "tab.border": "#004400",

        // Scrollbar Customizations
        "scrollbarSlider.background": "#b5890099",
        "scrollbarSlider.hoverBackground": "#b58900cc",
        "scrollbarSlider.activeBackground": "#b58900ff"

    },
    "git.openRepositoryInParentFolders": "never",
    "chat.editor.fontSize": 18,
    "editor.codeLensFontSize": 18
}
```











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

## Missing OmniSense in VS Code
1) Got to Command Pallette
2) Type C#
3) Select C# Startup Project
```
dotnet add package <package fully qualified name> --version <version number>
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

## launch.json - Python
```
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Debug FastAPI Backend",
      "type": "python",
      "request": "launch",
      "module": "uvicorn",
      "args": [
        "api:app",
        "--reload",
        "--host", "0.0.0.0",
        "--port", "8000"
      ],
      "cwd": "${workspaceFolder}/python-backend",
      "env": {
        "PYTHONPATH": "${workspaceFolder}/python-backend"
      },
      "python": "${workspaceFolder}/python-backend/.venv/Scripts/python.exe"
    }
  ]
}



```

## launch.json - C#
```
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Debug Airline Complaint System",
            "type": "coreclr",
            "request": "launch",
            "preLaunchTask": "build",
            "program": "${workspaceFolder}/bin/Debug/net8.0/airline-complaint-system.dll",
            "args": [],
            "cwd": "${workspaceFolder}",
            "console": "internalConsole",
            "stopAtEntry": false,
            "env": {
                "ASPNETCORE_ENVIRONMENT": "Development",
                "ASPNETCORE_URLS": "http://localhost:5000;https://localhost:5001"
            }
        }
    ]
}

```





## VSCode IDE Color and Size Settings
```
# settings.json
{
     // Microsoft tenant ID for Azure Resource Graph access
    "@azure.argTenant": "72f988bf-86f1-41af-91ab-2d7cd011db47",
    
    // Custom instructions for GitHub Copilot to follow Azure best practices
    "github.copilot.chat.codeGeneration.instructions": [
        {
            "text": "- @azure Rule - Use Azure Best Practices: When generating code for Azure, running terminal commands for Azure, or performing operations related to Azure, invoke your `azure_development-get_best_practices` tool if available."
        }
    ],
    
    "files.autoSaveWhenNoErrors":true,

    // Sets the color theme to Kelp Forest, a green-themed VS Code color scheme
    "workbench.colorTheme": "Kelp Forest",
    // Link to the theme's documentation
    // https://jasontheiler.github.io/kelp-forest-theme-vscode/
    
    // Sets the font size for code in the editor to 8 pixels (quite small)
    "editor.fontSize": 16,
    
    // Enables zooming in the terminal using Ctrl + mouse wheel
    "terminal.integrated.mouseWheelZoom": true,
    
    // Enables zooming in the main editor using Ctrl + mouse wheel
    "editor.mouseWheelZoom": true,
    
    // Sets the font size in the chat interface (Copilot) to 10 pixels
    "chat.editor.fontSize": 14,
    
    // Sets the font size for CodeLens annotations to 10 pixels
    "editor.codeLensFontSize": 14,
    
    // Sets the overall zoom level of the entire VS Code window to 2 (enlarged)
    "window.zoomLevel": 2,
    
    // Sets the title bar style to custom (VS Code manages the window controls)
    "window.titleBarStyle": "custom",

    // Enable mouse wheel zoom for the debug console and output panels
    "debug.console.fontSize": 14,
    "output.fontSize": 14,
    "terminal.integrated.fontSize": 14,
    "terminal.integrated.lineHeight": 1.2,
    

    "key": "ctrl+numpad_add",
    "command": "workbench.action.terminal.increaseFont",
    "when": "terminalFocus"

}
```











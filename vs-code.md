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

## Open the search bar at the top of the editor
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

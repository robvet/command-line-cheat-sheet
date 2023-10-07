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
dotnet new console --framework <version, such as: net7.0>
```

## Add use secrets
```
dotnet user-secrets set "<key>" "<value>"
```

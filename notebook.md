# Jupyter Notebook Cheat-Sheet

Quick reference for Jupyter Notebooks

## C-Sharp
### Login into an Azure Tenant
```
PolyGlot Noteboks Extension
https://newdevsguide.com/2022/12/14/polyglot-notebooks-csharp/
https://github.com/dotnet/interactive/blob/main/docs/NotebookswithJupyter.md

In Command Palette, type 'Polyglot'
  - Create new blank notebook
.ipynb
C#



az account show --query tenantId -o tsv

```

## AZ CLI - Login/Account

### Login with web (interactively)
```
az login
az login -u myemail@address.com
az login -t <AAD tenant Id>
```
### Show current AAD User
```
az ad signed-in-user show
```
### List accounts
```
az account list --output table
```

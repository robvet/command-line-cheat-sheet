# Jupyter Notebook Cheat-Sheet

Quick reference for Jupyter Notebooks

### Create Notebook
```

# Plumbing: Create new virtual environment
python -m venv .venv<projectname>

# Activate it
.\.venv\Scripts\activate

# Install ipykernel using PIP
 - Enables Jupyter notebook support - Without ipykernel, you can't run Python code in Jupyter notebooks
 - Registers the Python environment - Makes your current Python environment available as a kernel option in Jupyter
 - Provides interactive features - Enables features like code completion, introspection, and rich output display
 - VS Code integration - Allows VS Code to run Jupyter noteboo
pip install ipykernel

# Install Jupyter notebook support
pip install jupyter

# Register your venv as a Jupyter kernel:
 - Registers existing venv as a Jupyter kernel so notebooks can use it.
python -m ipykernel install --user --name=your_project_name # replace projectname with what you want to call the kernel

# Create new notebook (.ipynb file)
Command Palette: Ctrl+Shift+P → type "Create: New Jupyter Notebook"
From 'Select Kernel' dropdown on right-hand side, select Python Environment, and find your current venv (it should be the default selection)

# Select your kernel in the notebook
Click kernel selector (top right) → choose your registered kernel name

# Test Notebook
Input into notebook to test:
 print("Hello from notebook!")
 import sys
 print(f"Python: {sys.executable}")

# Go to town!

```




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

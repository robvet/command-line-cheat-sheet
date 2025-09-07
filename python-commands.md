# Python Commands Cheat-Sheet

## Environments

### Actviate\Deactivate Environment
```
# from PowerShell
.venv\Scripts\activate.ps1

# Other
.\.venv\Scripts\activate

# Steps to Change the Python Environment:
 - Open the Command Palette: Press Ctrl+Shift+P (Windows/Linux) or Cmd+Shift+P (macOS).
 - Search for "Python: Select Interpreter": Begin typing "Python: Select Interpreter" into the Command Palette search bar and select the corresponding option when it appears.

# Deactivate
deactivate
```

### Python Virutal Environments
```
# Create new virtual environment
python -m venv .venv<projectname>

# Create venv with specific version of Python
python -3.12 -m venv .venv

# Note: The virtual environment (.venv) will be created using the Python interpreter referenced by the python command.
# If 'python --version' shows 3.13.4, then .venv will use Python 3.13.4 automatically.

# Activate virtual environment

###You have multiple ways to activate environments:
 - Method 1: VS Code Python Interpreter
 - Open new terminal (Ctrl+Shift+`)
 - Select interpreter 
Easiest for development

Method 2: Manual activation
# Windows
.\.venv\Scripts\activate

# conda
- conda activate apiweaver (not .venv command - that's different)
- Useful for command line work outside VS Code

Method 3: Anaconda Prompt
 - Always works, good fallback

# Steps to Change the Python Environment:
 - Open the Command Palette: Press Ctrl+Shift+P (Windows/Linux) or Cmd+Shift+P (macOS).
 - Search for "Python: Select Interpreter": Begin typing "Python: Select Interpreter" into the Command Palette search bar and select the corresponding option when it appears.

# Deactivate
deactivate


# Linux/MacOS
source venv/bin/activate
source .venv/Scripts/activate

# Install packages from requirements.txt
pip install -r requirements.txt

```


### Create Notebook
```
# Create new virtual environment
python -m venv .venv<projectname>

# Activate it
.\.venv\Scripts\activate

# Install ipykernel using PIP
pip install ipykernel

# Install a new Kernel
ipython kernel install --user --name=.venv<projectname>

# Start Juypter
VS Code
Set Environment

# Install pacakges
pip install -r requirements.txt

```
### Associate venv with app
```
python -m ipykernel install --user --name=obv-env --display-name "Python (obv-env)"
```

### Python Versions
```
# Determine if and what version of a Python runtime is installed
python -<version> --version
# Example:
py -3.12 --version  
```

### Python and OpenAPI
```
# run API and suffix url with \docs
\docs
```

### Packages
```
# Install pacakges
pip install -r requirements.txt

# install packages
pip install --force-reinstall -r requirements.txt

# Is a package installed
pip show <package name>

# list all packages in an environment
pip list

Check for requirements.txt in project
# Windows

# Linux
cat requirements.txt
type requirements.txt

# find version of packages:
pip list | grep -E 'fastapi|uvicorn'

# Query for released versions of Python packages
pip index version <name of package>

```

### Display packages in tree format with dependencies
```
pipdeptree
```

### Uninstall packages, venv or python fodler
```
pip uninstall <mkdocs mkdocs-material> <package name>
```

### Obtain deeper diagnostic for a packge
```
python -X importtime -c "import <package name>"
```

### FastAPI: Check if port 8000 (default port) is free
```
netstat -ano | findstr :8000
#Kill process if necessary
taskkill /PID <PID> /F
```

### Reinstall dependencies to ensure consistency
```
# Unintall depedencies
# Clear cahced pacakges to ensure you're installing new packages
pip cache purge
# Freeze to generate a new list of currently installed packages with thier versions
# this will overwirte the old file
pip freeze > requirements.txt
```
### Start Fastapi 
```
uvicorn main:app --reload
```

### Show Conda (non-venv) Environments

```
conda env list
```


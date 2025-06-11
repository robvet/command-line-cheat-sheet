# Python Commands Cheat-Sheet

## Environments

### Actviate Environment
```
# from PowerShell
.venv\Scripts\activate.ps1

# Other
.\.venv\Scripts\activate
```

### Python Virutal Environments
```
# Create new virtual environment
python -m venv .venv<projectname>

# Note: The virtual environment (.venv) will be created using the Python interpreter referenced by the python command.
# If 'python --version' shows 3.13.4, then .venv will use Python 3.13.4 automatically.

# Activate virtual environment
.\.venv\Scripts\activate

or...
source .venv/Scripts/activate

or...
. .venv/Scripts/activate

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

### Packages
```
# Install pacakges
pip install -r requirements.txt

# install packages
pip install --force-reinstall -r requirements.txt

# Is a package installed
pip show <package name>

# list all packages
pip list

# find version of packages:
pip list | grep -E 'fastapi|uvicorn'

# Query for released versions of Python packages
pip index version <name of package>

```

### Display packages in tree format with dependencies
```
pipdeptree
```

### OBtain deeper diagnostic for a packge
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


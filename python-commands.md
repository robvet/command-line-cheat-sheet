# Python Commands Cheat-Sheet

## Run/Debug

### Run/Debug

```
### To Debug: <F5>
### To Run: <Ctrl><F5>
```

## Socket in Use
```
netstat -ano | findstr :8000
taskkill /F /PID 44744
```

## Terminal Stuck in KeyboradInterrupt
```
Try <ctrl><z>

Soft interrupt: press Ctrl+C once (may require focus on terminal). If the shell shows another prompt or the Python REPL returns, you're done.
If you see a partial traceback or a second-level KeyboardInterrupt, press Enter, then Ctrl+C again.
If you're inside Python REPL, exit cleanly:
Press Ctrl+D (EOF) or type exit() and press Enter.
### Open the Command Palette (Ctrl+Shift+P on Windows/Linux or Cmd+Shift+P on macOS).

```

## List 

## Scafold Enviroment (VS Code)

### Scafold Python Project from Command Palette

```
### Install the 'Python Environments' extension in Vs Code.
```

```
### Open the Command Palette (Ctrl+Shift+P on Windows/Linux or Cmd+Shift+P on macOS).

### Search for and select Python Envs: Create Project from Template.

### Choose your template:
 - Package: Scaffolds a complete Python package with a pyproject.toml, src directory, and boilerplate files.
 - Script: Creates a single Python script with boilerplate code.

###Follow the prompts to name your project and, for a package, to automatically create a virtual environment inside your workspace. 

```

## Create Python Virtual Environment (VS Code)

### One-shot fast-ramp for venv
```
# Create new virtual environment
python -m venv .venv

## Steps to Change the Python Environment:
 - Open the Command Palette: Press Ctrl+Shift+P (Windows/Linux) or Cmd+Shift+P (macOS).
 - Search for "Python: Select Interpreter": Begin typing
 - "Python: Select Interpreter" into the Command Palette search bar and select the corresponding option when it appears.

# activate environment
## from PowerShell
.venv5\Scripts\activate.ps1

## from Other
.\.venv\Scripts\activate

# Install packages
## MAKE SURE YOU POINTING to your virtual environment 
pip install -r requirements.txt

```

### Explicit Instructions for venv
```
# Create new virtual environment
python -m venv .venv<projectname>

# Create venv with specific version of Python
python -3.12 -m venv .venv

# Note: The virtual environment (.venv) will be created using the Python interpreter referenced by the python command.
# If 'python --version' shows 3.13.4, then .venv will use Python 3.13.4 automatically.

# Activate virtual environment

###You have multiple ways to activate virutal environments:
 - Method 1: VS Code Python Interpreter
 - Open new terminal (Ctrl+Shift+`)
 - Select interpreter  
Easiest for development

Method 2: Manual activation
# Windows
.\.venv\Scripts\activate

Method #3: Few Shot Testing
.\.venv\Scripts\python.exe -c "from app.main import app"

# Why the full path works
When you run .\.venv\Scripts\python.exe, it:
Uses the Python interpreter from that venv
Automatically uses packages installed in that venv
Doesn't require activation



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

## Manage Virtual Environments

### Actviate\Deactivate Environment
```
# from PowerShell
.venv\Scripts\activate.ps1

# Linix
source .venv-mcp-postgres/Scripts/activate

# Other
.\.venv\Scripts\activate

# Steps to Change the Python Environment:
 - Open the Command Palette: Press Ctrl+Shift+P (Windows/Linux) or Cmd+Shift+P (macOS).
 - Search for "Python: Select Interpreter": Begin typing "Python: Select Interpreter" into the Command Palette search bar and select the corresponding option when it appears.

# Deactivate
deactivate
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

## Packages

### List Packages in VENV
```
# activate venv

 - PowerShell
.\venv\Scripts\Activate.ps1

- bash
.\venv\Scripts\Activate.ps1

# list packages in venv
pip list
```

### List Packages in root python folder
```
# deactivage venv, if necessary:
deactivate

# determine location of root python folder
# First, try:
& "C:\Program Files\Python311\python.exe" -m pip list

# if not correct, then find python root folder:
 - Find Python executable path
   where python
 - Or get detailed info
   python -c "import sys; print(sys.executable)"

# List packages in root Python
& "<root python folder>" -m pip list
```

### Install Packages
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

# View packages installed in a root python environment (powershell)
& "C:\Program Files\Python311\python.exe" -m pip list

# Compare packages from root environment to a vitural environment
# Global environment
& "C:\Program Files\Python311\python.exe" -m pip list > global.txt
# Project venv
.\.venv\Scripts\python.exe -m pip list > venv.txt
code -d global.txt venv.txt   # opens a side-by-side diff in VS Code

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

### Uninstall local (venv) packages, venv or python fodler
```
# activate venv

 - PowerShell
.\venv\Scripts\Activate.ps1

- bash
.\venv\Scripts\Activate.ps1

# list packages in venv
pip list

# uninstall package(2)
pip uninstall package1 package2 -y

# deactivage venv, if necessary
deactivate
```

### Uninstall root python folder packages 
```
# deactivage venv, if necessary:
deactivate

# determine location of root python folder
# First, try:
& "C:\Program Files\Python311\python.exe" -m pip list

# if not correct, then find python root folder:
 - Find Python executable path
   where python
 - Or get detailed info
   python -c "import sys; print(sys.executable)"

# List packages in root Python
& "<root python folder>" -m pip list

 Uninstall specific packages
& "C:\Program Files\Python311\python.exe" -m pip uninstall package1 package2 package3 -y

# Uninstall everything except pip and setuptools
& "C:\Program Files\Python311\python.exe" -m pip list --format=freeze | Where-Object {$_ -notmatch "^pip|^setuptools"} | ForEach-Object {& "C:\Program Files\Python311\python.exe" -m pip uninstall $_.Split("==")[0] -y}
```

### Show packages in root with installation date
```
pip list --format=freeze | ForEach-Object {
    $pkg = $_.Split("==")[0]
    $path = & python -c "import importlib.util; print(importlib.util.find_spec('$pkg').origin if importlib.util.find_spec('$pkg') else '')" 2>$null
    if ($path) {
        $time = (Get-Item $path).LastWriteTime
        [PSCustomObject]@{Package=$pkg; LastModified=$time}
    }
} | Format-Table -AutoSize
```

### Show Conda (non-venv) Environments

```
conda env list
```
### Display packages in tree format with dependencies
```
pipdeptree
```

### Obtain deeper diagnostic for a packge
```
python -X importtime -c "import <package name>"
```


# misc package code
```
pip uninstall <mkdocs mkdocs-material> <package name>

# what packages are installed in root:
& "C:\Program Files\Python311\python.exe" -m pip list
# only keep pip and setuptools, clear everything else
& "C:\Program Files\Python311\python.exe" -m pip uninstall greenlet lz4 playwright pycryptodomex pyee python-dotenv pywin32 shadowcopy typing_extensions WMI browser_cookie3 -y

pip uninstall <mkdocs mkdocs-material> <package name>

# what packages are installed in root:
& "C:\Program Files\Python311\python.exe" -m pip list
# only keep pip and setuptools, clear everything else
& "C:\Program Files\Python311\python.exe" -m pip uninstall greenlet lz4 playwright pycryptodomex pyee python-dotenv pywin32 shadowcopy typing_extensions WMI browser_cookie3 -y
```



## FastApi

### Start Fastapi 
```
uvicorn main:app --reload
uvicorn app.main:app --host 127.0.0.1 --port 8000 --reload
```

### FastAPI: Check if port 8000 (default port) is free
```
netstat -ano | findstr :8000
#Kill process if necessary
taskkill /PID <PID> /F
```

### Launch Browser at start of Python program
```
# add package
import asyncio
import webbrowser
from contextlib import asynccontextmanager

@asynccontextmanager
async def lifespan(app: FastAPI):
    # Startup: open browser after a short delay to ensure server is ready
    async def open_browser():
        await asyncio.sleep(1.5)  # Give server time to start
        webbrowser.open("http://127.0.0.1:8000/docs")
    
    asyncio.create_task(open_browser())
    yield
    # Shutdown (if needed)
app = FastAPI(title="rob-gpt", lifespan=lifespan)


netstat -ano | findstr :8000
#Kill process if necessary
taskkill /PID <PID> /F
```


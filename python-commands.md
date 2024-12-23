# Python Commands Cheat-Sheet

## Environments

### Actviate Environment
```
.\.venv\Scripts\activate
```

### Packages
```
# install packages
pip install --force-reinstall -r requirements.txt

# list all packages
pip list

# find version of packages:
pip list | grep -E 'fastapi|uvicorn'
```

### Reinstall depdendcies to ensure consistency
```

```
### Start Fastapi 
```
uvicorn main:app --reload
```

### Show Conda (non-venv) Environments

```
conda env list
```


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

### Display packages in tree format with dependencies
```
pipdeptree
```




### Reinstall depdendcies to ensure consistency
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


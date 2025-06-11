# Linux Command Line Cheat-Sheet

## Simple Delete a directory and all its content
```
rm -r <directory name>
rmdir <directory name>
/s flag that recursively deletes all files and subdirectories in the target directory
/q enables quite mode -- you're not prompted for confirmation

```

## Show what ports are running (useful for troubleshooting
```
sudi netstat -at | less
```

## Change volumes from Bash command line
```
# Change to F: drive
cd /f/

#Query volumes
cd /volumes
```
## Unpack Tar file
```
# Unpack
tar -xvf <filename.tar>
```

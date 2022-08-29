# Linux Cheatsheet For Beginners
This is a collection of commands that make navigating a command line more manageable. I'm making this for my girlfriend, but if anyone else finds this useful, let me know!

---
**LEGEND** \
[] - This parameter is optional. The command will work with or without it, although it will behave differently. \
<> - This parameter is specific to your scenario. This can be a filename, a directory path or an id. \
___

**_IMPORTANT:_** If a file or directory path has a space in it, you need to be careful that the command doesn't interpret this as a new parameter. To avoid this, you can surround the directory name in quotes, or use a `\` before the space. (`\` is called an escape character.) For examples of this, check out the mkdir section, where we make a directory named `Season 01`.
___

# Change Directory - cd
In my opinion, the most useful command. You use it to travel from directory to directory. 
## Syntax
``` bash
cd <DESIRED DIRECTORY>
```
## Examples
### Navigating up one directory
If you're in `/Users/admin/Document` and if you want to navigate to `/Users/admin/`
``` bash
cd ..
```
### Navigating up two directories
If you're in `/Users/admin/Document` and if you want to navigate to `/Users/`
``` bash
cd ../..
```
### Navigating to an absolute path
If you're in `/Users/admin/Document` and if you want to navigate to `/etc/bin/`
``` bash
cd /etc/bin
```
---
**NOTE**: Make sure you include the `/` at the beginning of the path if it's and absolute path. 

___


# List directory contents - ls
This lists all of the contents of a directory. 
## Syntax
``` bash
ls [-a] [-l] [<DESIRED DIRECTORY>]
```
## Examples
### List files in current directory
``` bash
ls
```

### List _all_ files in current directory (including `./`and `../`)
``` bash
ls -a
```

### List files in current directory, with the output in list format
``` bash
ls -l
```

### List files in a specific directory
``` bash
ls /etc/bin/
```

# Move file - mv
This command is used for moving files. It removes the file from its old location, and saves it to a location specified. It can also be used to rename files.
## Syntax
``` bash
mv <OLD FILENAME> <NEW FILENAME>
```

## Examples
### Moving a file named `Movie.mkv` up a directory.
``` bash
mv ./Movie.mkv ../Movie.mkv
```
### Moving _all_ files in `/Users/admin/Downloads` to `/Users/admin/Documents`
``` bash
mv /Users/admin/Downloads/* /Users/admin/Documents/
```

### Rename a file from `old.txt` to `new.txt`

``` bash 
mv ./old.txt ./new.txt
```

# Make a new directory - mkdir
**_USEFUL TIP FOR PLEX:_** Plex will pick up seasons if it's in a directory with the naming convention `<TV SHOW NAME>/Season 01`
## Syntax
``` bash 
mkdir <DIRECTORY NAME>
```

## Examples
### Creating a directory inside the current directory named `Season 01`
``` bash
# Using quotes because of the space
mkdir 'Season 01'
# Alternatively you can type:
mkdir Season\ 01
```

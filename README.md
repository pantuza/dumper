## DUMPER

### NAME
> ###### dumper
    
### DESCRIPTION

        A bash script to make mysql dump files from a production database
    server and import its files in the database at the development 
    enviroment computer/server

        It basically connects to the database server, makes a dump file of
    the database/table passed by argument to the script. Archive this dump
    file using tar utility program, then unarchive it on local directory.
    After that, import the file to the development database.

### USAGE

- Open the script file and setup the variables(server, user, database, etc)
- Place the script in a safe directory or in a public path like /usr/bin/
- Set the execution bit to the script file
- enjoy the script :)


###### Example:

- Dumps all the dev_db database
```bash 
$> dumper dev_db 
```

- Dumps only the dev_tb table from dev_db database
```bash
$> dumper dev_db dev_tb
```

### FILES
```bash
    $HOME/dumps/dump
        The target file for the dump files

    $HOME/dumps/dump_
        The backup file of the last dump created

    /usr/bin/dumper
        The recommended directory for the dumper script file
```

### AUTHOR
> ###### Written by Gustavo Pantuza

### REPORTING BUGS

> ###### Report dumper bugs to gustavopantuza@gmail.com


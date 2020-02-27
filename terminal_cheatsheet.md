# Terminal Cheatsheet
## Getting Help

    whatis cp
    > cp (1)               - copy files and directories

> one liner describing the command `cp`

    cp --help
    > 
> bring up the help listing for the command `cp`

    man cp
> bring up the full manual reference pages for the command `cp`

    apropos copy
> bring up a list of commands that have something to do with `copy`

## Navigating

    ls
> list files and folders in current directory. Does not show hidden files

    ls *.py
> list files and folders that match the pattern `*.py` where `*` can be any number of cahracters
> 
    ls test_??.py
> list files and folders that match the pattern `*.py` where `*` can be any number of cahracters

    ls /etc
> list files and folders in the directory `/etc`

    ls -lah
> list files and folders with the flags
> - `-l` long mode
> - `-a` all files including hidden files
> - `-h` human readable - convert to file size to kB, MB etc.

    pwd
> print name of current/working directory

    cd /etc/nginx
> navigate to folder `/etc/nginx`

    cd ~
> navigate to home folder (e.g. `/home/marlan`)

    cd ..
> navigate to parent directory

    popd
> navigate to previous directory (go down the directory history stack)

    pushd
> navigate to previous directory but add the current directlory to the directory history stack. This will allow a subsequent call to popd to return to the current directory. For example.
> - currently in location `/home/marlan`
> - issue the command `cd /etc`
> - issue the command `pushd` - you get taken back to `/home/marlan`
> - issue the command `popd` - you get taken back to `/etc`

    locate test
> locate all files containing the pattern `test`. This will be interpreted as `*test*`. The locate command looks in an indexed database of all files so new files may not appear if the database has not been indexed recently

    updatedb
> update teh indexed database used by the locate commnad. This might take a while... Normally the OS runs this on its own periodically when there are free resources

    find ~/projects '*.cfg'
> find all files that match the pattern `*.cfg` in the `~/projects` folder. This is not dependent on an indexed database and will search the given folder and all subfolders recursively
    
    which

## Files and Folder

    file name
> describe the type of file that `name` is
    
    mkdir folder
> create a directory inside the current directory called `folder`
    
    touch filename
> change the timestamp of `filename` to now without modifying any contents; creates empty text file `filename` if file doesn't exist
    
    cp source destination
> copy the file `source` into directory `destination`
    
    mv source destination
> move the file `source` into directory `destination`

    rm my_passwords
> deletes (unlinks) the file `my_passwords`
    
    rmdir
> deletes the directory `empty`, only if it is empty

    wildcards
> characters that can be used as a substitute for any of a class of characters in a search

    *temp*
> refers to anything whose name has `temp` anywhere in it
    
    temp*
> refers to anything whose name starts with `temp`
       
    *temp
> refers to anything whose name ends with `temp`
 
    `em?ty`
> refers to anything with one character separating the start `em` and the end `ty`
 
    recursive flag
    
    echo Hello World!
> prints `Hello World!`

    cat hello world
> concatenates the contents of the files `hello` and `world` and prints out the result.
> If given a single file, it prints the contents of the file
    
    head / tail
> view the top or bottom few lines of a file
    
    wc Remembrance_of_Things_Past
> prints line wount, word count, and byte count for the file `Remembrance_of_Things_Past`
    
    diff
    md5sum
    less
    jump
    search
    nano
    grep
    zip / unzip
    tar
    df
    du

## Running Commands

- options
- tab complete
- up arrow
- history
- reverse search
- pipes (redirection)
  - `|` puts the output of the function on the left of `|` into the function on the right
  - `>` (over)writes output on left into file on right
  - `>>` appends output on left to file on right
  - `2>` 
- return status
- environment variables
- variable substitution

## Users and permissions

    sudo
    sudo -s
    sudo -H
    su
    su -
    users
    id
    groups
    chmod
    s bit
    chown

## Network

    ssh
    ssh-keygen
    ssh-copy-id
    ~/.ssh/authorized_keys
    ~/.ssh/known_hosts
    ~/.ssh/config
    scp
    rsync
    ifconfig
    netstat
    wget
    curl



## Processes

    ps
    htop
    killing proceses
    ctrl+c
    ctrl+d
    ctrl+l
    kill / killall
    watch
    systemctl
    crontab

## Miscellaneous

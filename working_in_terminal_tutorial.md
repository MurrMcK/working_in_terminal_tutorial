# Working in Terminal

We have GUIs (Graphical User Interfaces) to do a lot of things these days. Why might we want to do something in the terminal instead?

1. We're connecting to a server (either at the office or remote) and that's the only way we can interact with it
2. We want to do something advanced or with more control than is available through a GUI
3. We want to do something programmatically so that it can be automated
4. We get so used to working in terminal that it actually becomes easier than using a GUI

For the purposes of this tutorial, we're going to assume that we're at the terminal connected to a Linux machine (specifically Ubuntu) using a bash shell (don't worry if you don't know what that means). Things may be slightly different on other Unix distributions like Mac OSX or a cousin like FreeBSD but once you're familiar with these basics, the same general principles apply. Windows users are also in luck because you can get a lot of the same functionality using Cmder (more on that later) or if you're into the dark arts then Windows PowerShell but I'm not going anywhere near that beast.

If you don't like reading, here's a nice video which covers most of the same material (I actually used it as a basis to make sure I was covering all the important stuff)

[![Joe Collins Beginner's Guide to bash](https://img.youtube.com/vi/oxuRxtrO2Ag/0.jpg)](https://www.youtube.com/watch?v=oxuRxtrO2Ag)

Our objective in this tutorial is to get familiar with working at a Unix terminal, learn the concepts and commands that we'll use most often for day-to-day work and know how to find out more when we need to. We will not get into more advanced bash functionality like `if` statements and `for`, commands like `sed` and `awk` which do text and file manipulation using regex or the type of commands mostly used by system administrators.

## Getting in

The first thing you'll need to do is actually get into the terminal. If you're on windows then you're probably using `putty` to connect to another server. I assume somebody's already set that up for you or you're familiar enough that you can set up your own connections so I won't get into that here.

I would recommend installing Cmder, specifically the full version that includes git bash. This will let you use many of the same linux commands to do things on your windows machine including ssh that you can manage exactly the same way that I describe below for Linux users. Plus, you get a sweet Quake style dropdown terminal, which I find super-convenient. loops which are really useful for writing bash scripts or more advanced 

If you're already on a linux machine you can generally launch a terminal with `ctrl+alt+t`. You can follow all the steps below on your local machine but to keep things consistent for everyone, we're going to log onto a remote machine with our first command.

```bash
ssh marlan@server.co.za
```

This will log me into the server located at `server.co.za` as the user `marlan`. You will probably be prompted for a password, which you can enter and then press `enter`. Note that in Linux, when you enter a password nothing will appear (for security reasons) not even `***`. The server location can be a url, an IP address (like `192.168.1.1`) or an alias like `localhost` (which actually points to the machine you're currently connected to)

you should then be greeted with a command prompt that looks like this:

```
marlan@server:~$
```

To quit the terminal session, type

```bash
exit
```

## Getting around

Let's look at that command prompt again. This shows that I'm logged in as the user `marlan`, the machine I'm connected to is called `server`. The bit after the `:` is the file system location that you're currently in. The tilda (`~`) is actually an alias for the home folder of your user. I can see this by typing in

```bash
pwd
```

which returns

```
/home/marlan
```

### Getting in

- putty
- cmder
- ssh
- bash
- exit

### Basic intro to the Unix directory stucture

- /
  - home
  - bin
  - etc
  - var
  - opt
  - dev
  - usr
  - lib
  - mnt
  - srv
  - sys

### Navigating

- ls
  - options
    - l
    - a
    - h
  - file types and extensions
    - hidden files
- paths
  - absolute and relative paths
  - escape characters
- pwd
- cd
- pushd and popd
- prompt
- file
- locate
  - sudo updatedb
- find
- which

### Working with files and folders

- mkdir
- touch
- cp
- mv
- rm
- rmdir
- wildcards
  - `*`
  - `?`
- recursive flag
- echo
- cat
- head / tail
- wc
- diff
- md5sum
- less
  - jump
  - search
- nano
- grep
- zip / unzip
- tar
- df
- du

### Running Commands

- help
  - whatis
  - man
  - --help
  - apropos
- options
- tab complete
- up arrow
- history
- reverse search
- pipes (redirection)
  - |
  - >
  - >>
  - 2> 
- return status
- environment variables
- variable substitution
  



## Linux Concepts

- Everything is a file
- imputs and outputs
- Customise everything
- sessions
- processes
- ports
- sockets

## Users
****
- Permissions
- sudo and su
  - flags
    - s
    - H
    - -
- users
- id
- groups
- chmod
  - s bit
- chown
- 

# Processes

- ps
- htop
- killing proceses
  - ctrl+c
  - ctrl+d
  - ctrl+l
- kill / killall
- watch
- systemctl
- crontab

# Network commands

- ssh
  - ssh-keygen
  - ssh-copy-id
  - ~/.ssh/authorized_keys
  - ~/.ssh/known_hosts
  - ~/.ssh/**config**
- scp
- rsync
- ifconfig
- netstat
- wget
- curl

## Screen

### Customising terminal

- ~/.bashrc

- color prompt
- other shells
  - zsh
  - fish

## Other useful commands

### Databases

- mysql
- vertica
- psql





## Appendix A: Cheatsheet


###
## Appendix A: Linux File System
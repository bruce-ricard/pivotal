# Pivotal login

## Description

If you work on common workstations and you often need to:
- use SSH keys (e.g. connect to remote git repos)
- use lastpass on the command line (e.g. update your concourse pipelines)

then this script is made for you.

`pivotal_login` allows you to connect to lastpass and add your SSH keys
in one short command.

## First timer user guide

Starting from the second time you use the command, you'll be able to run:
```
pivotal_login <initials>
```

and after entering your lastpass credentials, you'll be done.

The very first time you need to tell the program where your SSH private key is.
It will store it in lastpass for your convenience. You will need to run
something like this:
```
pivotal_login <your lastpass username> \
              -t <time to stay logged-in in hours> \
              --import-private-key <path to private key> \
              --save-alias <initials>
```

That's it! You are now all set to work with git and Concourse.

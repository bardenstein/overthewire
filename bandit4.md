# OverTheWire | Bandit

## Background 

The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

## Solution

1. We want to use the `file` command to see which files contain ASCII text (human readable), versus non-readable file types (like data, binary, etc.)
2. Because all of the filenames in the `inhere` directory start with `-`, we can't refer to them directly. 

Combining solutions from the previous Bandit exercises, we can see consolidate both of these goals into one succient command:

`file ./-*`   # Runs the file command on all files in the current directory (./) that start with `-`.

./-file00: data 
./-file01: data 
./-file02: data 
./-file03: data 
./-file04: data 
./-file05: data 
./-file06: data 
./-file07: ASCII text 
./-file08: data 
./-file09: data 

`cat ./-file07` 
koReBOKuIDDepwhWk7jZC0RTdopnAYKh 

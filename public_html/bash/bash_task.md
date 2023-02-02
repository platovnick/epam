**The tasks will be finally completed and published by February 11, 2022**
# Bash Scripting Tasks

## Create a data backup script that takes the following data as parameters:

1. Path to the syncing directory.
2. The path to the directory where the copies of the files will be stored.

In case of adding new or deleting old files, the script must add a corresponding entry to the log file indicating the time, type of operation and file name. [The command to run the script must be added to crontab with a run frequency of one minute]

``` sh
#! /bin/bash

case $1 in
   --all)
    echo "displays the IP addresses and symbolic names of all hosts in the current subnet" 
    sudo arp-scan --localnet | cut -f 1,3 
    ;;
  --target)
    echo "displays a list of open system TCP ports."
    ss -tlpn
    ;; 
  *)
  echo -e "The --all key displays the IP addresses and symbolic names of all hosts in the current subnet.\nThe --target key displays a list of open system TCP ports."
  ;;
  esac
```
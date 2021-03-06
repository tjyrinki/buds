# buds
Backup Ubuntu Devices Script

Backup Ubuntu based devices over ssh to a local directory.

## Features

 * No user interaction, just run it to kick off a backup
 * Checks for free space (roughly, 2x used space)
 * Compresses backup
 * Captures a list of installed clicks, for re-installation during device restoration
 * Uses device name and serial number in backup name, useful if you have multiple devices being backed up
 * Uses sudo to ensure all files in /home/phablet are backed up, no matter who owns them

## Pre-requisites

 * rsync & tee installed on host
 * ssh key installed on device ( I use phablet-shell to set this up)

## Running

`buds (ip address of device) (passphrase)`

e.g.

`buds 192.168.1.20 1234`

Backs up everything in `/home/phablet`, and creates a list of all click packages installed.

## TODO:

 * Restore script
 * Optionally grab click packages from store to stash in backup
 * Make it user friendly, so user doesn't have to know about ssh/keys etc
 * Make this all pretty with a GUI and stuff :)

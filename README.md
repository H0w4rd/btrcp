# BTRFS Recursive Copy Script
Recursively copies all files and directories and btrfs sends | receives all subvolumes.

This repository contains a Bash script designed to recursively copy a directory, taking into consideration BTRFS subvolumes. While tools like rsync are effective for most directories, BTRFS subvolumes can be a challenge to copy in a way that retains their structure and information. This script attempts to address that by:

1) Using rsync to handle the regular files and directories.
2) Detecting and then copying BTRFS subvolumes using the btrfs send and btrfs receive commands.

## Usage:
```
./btrcp <source_directory> <destination_directory>
```

Ensure that you have the necessary permissions to read from the source and write to the destination. Also, both source and destination directories should be on BTRFS file systems.

## Precautions
This script was written as a rapid solution to a specific use case. It's essential to test the script in a safe environment before using it on critical data.
Ensure backups of your data before attempting any kind of operation.

## Acknowledgments
Special thanks to ChatGPT from OpenAI for assistance in developing this script.

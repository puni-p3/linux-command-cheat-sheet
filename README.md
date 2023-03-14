# linux-command-cheat-sheet
Linux Command Cheat Sheet

### Show files & directories
`ls -a` # Lists all entries including those starting with a period (.).

`ls -l` # Displays permissions, links, owner, group, size, time, name.

`ls -R` # Lists subdirectories recursively.

### Sort all files & directories based on their size
`du -sh -- *  | sort -rh`  # Files and directories

`du -sh -- */ | sort -rh`  # Directories only

### Copy file/folder from remote to local using scp
`scp -i ec2key.pem username@ec2ip:/remote/path/to/file.az /local/path/to/`

#### Recursively download all files
`scp -ri ec2key.pem username@ec2ip:/remote/path /local/path/to/`

`man scp` # More info

https://stackoverflow.com/a/9441027

### Combine files
`cat *gz > final`
`mv final final.gz`

https://stackoverflow.com/a/40666202
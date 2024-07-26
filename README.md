# linux-command-cheat-sheet
Linux Command Cheat Sheet

### Show files & directories
`ls -a` # Lists all entries including those starting with a period (.).

`ls -l` # Displays permissions, links, owner, group, size, time, name.

`ls -R` # Lists subdirectories recursively.

### Sort all files & directories based on their size
`du -sh -- *  | sort -rh`  # Files and directories

`du -sh -- */ | sort -rh`  # Directories only

### System’s disk space usage.
`df -h` # Check Disk Space

### Copy file/folder from remote to local using scp
`scp -i ec2key.pem username@ec2ip:/remote/path/to/file.az /local/path/to/`

#### Recursively download all files
`scp -ri ec2key.pem username@ec2ip:/remote/path /local/path/to/`

#### Upload
`scp -i ec2key.pem /path/<file>.zip username@ec2ip:/remote/path`


`man scp` # More info

https://stackoverflow.com/a/9441027

### Combine files
`cat *gz > final`
`mv final final.gz`

https://stackoverflow.com/a/40666202

### SSH

`ssh -i private.pem user@ip` # ssh connect

#### Generate public key from private key
`ssh-keygen -f private.pem -y > public.pub`

#### AWS specific

Add public key

`vim .ssh/authorized_keys`

In case permission denied

`chmod go-w /home/ec2-user`

`chmod 700 /home/ec2-user/.ssh`

`chmod 600 /home/ec2-user/.ssh/authorized_keys`

### PORT (Find node process)

`ps aux | grep node`  # All node processes

`lsof -n -i:3005` # Specific port

### Certbot

`sudo certbot --nginx`

`sudo certbot certificates`


### Zip
`zip -r <file-name>.zip /<path-to-zip>`

`unzip -o <file-name>.zip -d /path/`
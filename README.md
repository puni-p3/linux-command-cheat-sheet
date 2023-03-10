# linux-command-cheat-sheet
Linux Command Cheat Sheet

### Show files & directories
`ls -a` # Lists all entries including those starting with a period (.).

`ls -l` # Displays permissions, links, owner, group, size, time, name.

`ls -R` # Lists subdirectories recursively.

### Sort all files & directories based on their size
`du -sh -- *  | sort -rh`  # Files and directories

`du -sh -- */ | sort -rh`  # Directories only
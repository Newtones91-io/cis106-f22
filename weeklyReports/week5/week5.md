---
Name: Isaac Oquendo
Class: cis106
Semester: Spring 2022
---

# Week Report 5

### Managing files and directories
**Commands**
| Definition | Usage | Example |
|-----|-----|-----|
|`mkdir` is a command used for creating a single directories or multiple directories.| To create a directory with `mkdir` type: `mkdir` + **the name of the directory** | `mkdir` `-p` `website/assets/{img,videos,music}`|
| `touch` is a command used to create files and updates the given file's timestamp. If the file does not exit, it creates a new file | To create a file type:`touch` + **the name of the file** | `touch` `shopping_lists.txt `|
| `rm` is a command to used remove files. `rm` by default does not remove directories. To remove a directory use rm -r option. | To remove a non-empty directory type: `rm` `-r` + **directory to be removed** | `rm` `-r` `website/` |
|`rmdir` is a command used to remove empty directories | To remove empty directories use `rmdir` + **directory to be removed** | `rmdir` `website/assets/music/` |
|`mv` is a command use to move and rename directories. Where source is the file or directory that you want to move and destination is where the directory or file is going. Both, source and destination can be either absolute or relative path. | The basic formula of the `mv` command is: `mv` + **source + destination** | To move a directory of file use: `mv` `/Downloads/week5.md cis106-spring/week5` |
|`cp` is a command used to copy file/directories from a source to a destination. | The `cp` command uses the same structure as the `mv` command: `cp`+ **file/directory to copy + destination** |`cp` `/Downloads/wallpapers/ /Pictures/wallpapers/` |
|`ln` is a command used to create a hard link of file. Hard links point to the data of a file on the hard drive. Therefore they share the same inode number.| To create a hard link type: `ln` **+ file name + new hard link file name** | `ln file ~/Downloads/fileHL`
|`man` are documentation files that describe linux shell commands, executable programs, system calls, special files, and so forth.| To view the manual of a command type: `man` + **command** | `man ls` |

### Brace expansion and how to use it

Brace expansion is not a wild card, but another feature of bash that allows you to generate arbitrary strings to use with commands.

**For example:**

- To create a whole directory structure in a single command type: `mkdir -p ~/Music/music/{jazz,rock}/{mp3files,music_videos,otherfiles}/new{1...3}`
- To create N number of files type:
`touch website{1...7}.html`
- To remove multiple files type:
`rm -r {dir2,dir3,file.txt,file2.txt}`
(linux-hpc)=
# Introduction to Linux and High-Performance Computing

An OS is a resource manager that is used to access system resources by users and application programs. [Linux](https://github.com/torvalds/linux) is an open source OS developed by [Linus Torvalds](https://en.wikipedia.org/wiki/Linus_Torvalds).  Linux is based on [Unix](https://en.wikipedia.org/wiki/Unix), and therefore shares much of its functionality with other unix based operating systems (such as MacOS.) Linux is the most widely used OS in computational research groups and runs much of the internet because it is freely available.

## The Linux Terminal

* Please make sure you can [open a terminal](https://github.com/medford-group/bdqm-vip/blob/master/files/installing_software.md)
* You issue commands in the terminal
* more complicated than you're used to, but much more powerful once mastered
* this lets you navigate file systems, edit files, and run code


* start by typing `ls`
* `ls` lists files in your current directory
* most common command

### Moving Through File Structures

* run `pwd`
* This stands for "print working directory"
* shows you where you are
* you're inside a file system in your "home directory"

![alt text](https://swcarpentry.github.io/shell-novice/fig/filesystem.svg "Linux File Structure")


* There is the "root" directory which is "/" and a few beneath it
* "Users" is where user home directories are kept

#### The ls Command
![alt text](https://swcarpentry.github.io/shell-novice/fig/home-directories.svg "Linux Home Directory Structure")
* run `ls -F`
* shows the slashes
* run `ls -F /`
* `ls -f /tmp`
* `ls --help` for help
* `man ls` give the manual (press "q" to exit this)
* `ls -j` doesn't work
* what does `ls -l` do?
* `ls -F -a` to see hidden files



#### The cd Command
* `cd` lets you change directories
* `cd /`
* this takes us to the root directory
* `cd ~`
* tidle is always your home directory
* `.` is the current directory `..` is one directory up
* `cd .`
* `cd ..`

#### Quick Problem
![alt text](https://swcarpentry.github.io/shell-novice/fig/filesystem-challenge.svg "File Problem")

if `pwd` shows `/Users/thing` what will `ls -F ../backup` display


#### Making Files and Directories
* `mkdir` makes directories
* `mkdir thesis`
* `cd data`
* `nano draft.txt`
* write something
* `ctrl + X` saves and quits
* `^` is `ctrl`
* editing files in terminal is important for research
* Questions


#### Removing Files
* be extremely careful
* no recycle bin in linux
* `rm [filename]`
* `rm -r` for folders

#### Running Code
* for our purposes we'll use `python [program name]`
* make a python script
* run script

### Scripts, Environments, and Aliases
* terminals are running a "shell" program. Most commonly, basic shell, or "bash" (other options: c shell, fish, etc.)
* shell commands can be strung together and combined with loops/conditions to form "scripts" (usually .sh files)
* by default, a "run commands" or "rc" script will be run when the shell starts (usually ~/.bashrc)
* shells can access "environment variables" which tell them where files live (e.g. $PATH, $PYTHONPATH)
* aliases can be used to create shortcuts and make new commands


### Using ssh To Get Onto The Supercomputer
* ssh is a secure remote linux terminal
* can be done through other programs on windows like [Putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/)
* `ssh -X [username]@pace-ice.pace.gatech.edu`
* `-X` allows visual data to be sent to your computer

## Linux Cluster Supercomputers
* pace is a [Linux cluster supercomputer](https://en.wikipedia.org/wiki/Computer_cluster)
* It is several computers all running linux connected together
* Supercomputers are not one big fast computer, it is many reasonably fast computers connected together
![alt text](https://ucdavis-bioinformatics-training.github.io/2017-June-RNA-Seq-Workshop/monday/cluster_diagram.png "Cluster Supercomputer Structure")
* If you want to learn more about PACE-ICE works, you can visit [PACE-ICE]{https://pace.gatech.edu/pace-ice-instructional-cluster-environment-education}. 

## Lectures
The link to the corresponding lectures (by Brabson) are as follows:
1. https://mediaspace.gatech.edu/media/VIP-BDQM-L02a-Intro_to_Linux_Computing/1_kb78m0hg 
2. https://mediaspace.gatech.edu/media/VIP-BDQM-L02d-slurm_bash_scripting/1_hqyzso1y 
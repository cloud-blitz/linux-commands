```shell
[user@hostname <current dir>]<user> #/$
```
```$```: This is the default user shell prompt. It appears when you are logged in as a regular user.
```#```: This is the root shell prompt. It appears when you are logged in as the superuser (root) or when you have escalated your privileges using ```sudo```. The root prompt indicates that you have administrative privileges and can execute commands with elevated access.
example for regular user ```ubuntu@hostname:~$``` and root user```root@hostname:~#```


```shell
 [root@server0 /]# who
```
Display current logged in all users with their details

```shell
 [root@server0 /]# whoami
```
Display current user details.
```shell
 [root@server0 /]# w
```
Display current user username.
```shell
 [root@server0 /]# wh <tab> <tab>
```
To see similar commands or autocomplete cmd.
```shell
 [root@server0 /]# clear or ctrl+l
```
It clears screen but not background data.

```shell
 [root@server0 /]# cal
```
It displays current month of calendar.
```shell
 [root@server0 /]# cal 2016
```
It displays specified year calendar.
```shell
 [root@server0 /]# cal 07 2015
```
It displays specific months calendar in particular year
```shell
 [root@server0 /]# cal -3
```
It displays previous, current and next month's calendar of current year.
```shell
 [root@server0 /]# cal -j 2015
```
It displays Julian days of particular year.
```shell
 [root@server0 /]# date
```
It shows current date and time.
```shell
 [root@server0 /]# date -j <year> -s “DD MM YYYY HH:MM:SS 
```
It set date and time.
```shell
 [root@server0 /]# reboot or init 6
```
To restart the system
```shell
 [root@server0 /]# poweroff or init 0
```
To power off system.
```shell
 [root@server0 /]# shutdown or shutdown -h 10
```
It shutdown system after 10 min and broadcast message to all users.
```shell
 [root@server0 /]# shutdown -c
```
It cancels shutdown timer and broadcast message to all users.
```shell
 [root@server0 /]# logout or exit or ctrl + D
```
Logout from currently logged in user.
```shell
 [root@server0 /]# hostname or hostname -s
```
Shows machine name
```shell
 [root@server0 /]# hostnamectl 
```
Show detailed information about system
```shell
 [root@server0 /]# username -a 
```
It displays operating system kernel name.
```shell
 [root@server0 /]# username -r 
```
It display all information regarding system
```shell
 [root@server0 /]# free -h
```
It display RAM information in human readable form
```shell
 [root@server0 /]# lsusb
```
It lists all available USB devices.
```shell
 [root@server0 /]# lspci
```
It list all PCI devices
```shell
 [root@server0 /]# lscpu
```
It list processor information.
```shell
 [root@server0 /]# dmidecode
```
It display all hardware information.(root)
```shell
 [root@server0 /]# man
```
Show manual of mentioned command
```shell
 [root@server0 /]# info
```
Same as that of man command
```shell
 [root@server0 /]# whatis
```
Display one line description of manual page. (#mandb command should use to update database manuals.)
```shell
 [root@server0 /]# <command> --help
```
Show short description of manual page. –help is option thus, some command may not support this option.
```shell
 [root@server0 /]# which <CMD>
```
To know path of command file.
```shell
 [root@server0 /]# touch filename.txt
```
touch command is used to create files. Using touch command, multiple files can be created. 
- examples 
    - ```[root@server0 /]# touch /root/file1.txt```
    - ```[root@server0 /]# touch /root/Desktop/file1.txt /etc/data.mp3```
    - ```[root@server0 /]# touch /root/{data.txt,file.txt,demo.mp3}```
    - ```[root@server0 /]# touch /root/file{1..100}.txt```


```shell
 [root@server0 /]# mkdir dir1
```
 mkdir command creates directories. Creating multiple directories are also possible using mkdir command 
- examples 
    - ```[root@server0 /]# mkdir /dir1```
    - ```[root@server0 /]# mkdir /dir1 /root/Desktop/dir2 /etc/demo```
    - ```[root@server0 /]# mkdir /root/{demo,data,practice}```
    - ```[root@server0 /]# mkdir /practical{1..10}```
    - ```[root@server0 /]# mkdir –p /demo/data/practice```

```shell
 [root@server0 /]# cat /root/anaconda-ks.cfg
```
cat command is used to get data of file as output on the terminal. Reading out large file leads to navigate in terminal, which require separate scrolling device (mouse). So, cat command is very useful in reading smaller files with few lines of data in command line. 
- examples 
    - ```[root@server0 /]# cat /root/anaconda-ks.cfg```
```shell
 [root@server0 /]# more /root/anaconda-ks.cfg
```
more command provides line by line navigation and page by page navigation in downward direction but, upward scrolling not possible.
```shell
 [root@server0 /]# less /root/anaconda-ks.cfg
```
 less command allow navigation keys for scrolling up and down. Thus, it is more useful command than any other four command.
```shell
 [root@server0 /]# head /root/anaconda-ks.cfg
```
head command show few lines from top of the file. If head command is used without any option, it will show top ten lines by default. –n is used to give count of lines to be shown.
```shell
 [root@server0 /]# tail /root/anaconda-ks.cfg
```
tail command show few lines from bottom of file. If tail command is used without any option, it will show bottom ten lines by default. –n is used to give count of lines to be shown.
```shell
 [root@server0 /]# sort file1.txt
```
Sort command will display result in ascending or descending order. Without option, data will be shown in ascending order. 
- examples 
    - ```[root@server0 /]#  sort –r file1.txt```
 
```shell
 [root@server0 /]#  cp /root/anaconda-ks.cfg ~/Desktop/kickstart.txt
```
Copy operation use to copy files and directories in Linux, from one location to another. It will copy contents of one file to another. If destination file is not exist in given location then automatically new file will be generated. 
- examples 
    - ```[root@server0 /]# cp /root/anaconda-ks.cfg ~/Desktop/kickstart.txt```
    - ```[root@server0 /]# cp /root/anaconda-ks.cfg /mnt/```
    - ```[root@server0 /]# cp -r /etc /root```
    - ```[root@server0 /]# cp –r /root/* /media```
    - ```[root@server0 /]# cp –rv /abc.txt/xyz.mp3/media```
```shell
 [root@server0 /]# mv /root/anaconda-ks.cfg /mnt/
```
Move and rename both operation can be performed using ‘mv’ command. It moves files and directories from one location to another. It is possible to move and rename at the same time. 
- example 
    - ```[root@server0 /]# mv /root/anaconda-ks.cfg /mnt/```
    - ```[root@server0 /]# mv /media ~/Desktop/```
    - ```[root@server0 /]# mv /root/* /mnt/```
    - ```[root@server0 /]# mv fower flower.txt```
    - ```[root@server0 /]# mv /root/anaconda-ks.cfg /root/kickstart.cfg```, 
    - ```[root@server0 /]# mv /opt /demo```
    - ```[root@server0 /]# mv /root/anaconda-ks.cfg ~/Desktop/kickstart.txt```
```shell
 [root@server0 /]# rmdir /Demo
```
rmdir command only deletes empty directories.
```shell
 [root@server0 /]# rm -vf /Demo/file1.txt
```
rm command is use to delete files and directories. 
- examples 
    - ```rm /Demo/file10.txt```
    - ```rm -vf /Demo/file1.txt```
    - ```rm –f /Demo/*```,```rm –r /Demo```

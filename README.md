# cheatsheet
 Various commands and snippets that might be needed.
 
### Update all downloaded docker images
````
docker images |grep -v REPOSITORY|awk '{print $1}'|xargs -L1 docker pull
````
### Detect all outgoing port blocking
````
time nmap -p- portquiz.net | grep -i open
````

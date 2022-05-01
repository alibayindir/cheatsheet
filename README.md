# cheatsheet

 Various commands and snippets that might be needed.
## Update all downloaded docker images
````bash
docker images |grep -v REPOSITORY|awk '{print $1}'|xargs -L1 docker pull

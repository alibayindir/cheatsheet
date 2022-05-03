# cheatsheet
 Various commands and snippets that might be needed.
 
### Update all downloaded docker images
````
docker images |grep -v REPOSITORY |awk '{print $1":"$2}' |xargs -L1 docker pull
````
### Detect all outgoing port blocking
````
time nmap -p- portquiz.net | grep -i open
````
### Replace string "foo" with "bar" in all files in the directory recursively

 find ./ -type f -exec sed -i 's/foo/bar/g' {} \;

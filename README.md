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
````
find ./ -type f -exec sed -i 's/foo/bar/g' {} \;
````
### Create systemd-boot entry for root at /dev/sda2
````
string=$"title\tArch Linux\nlinux\t/vmlinuz-linux\ninitrd\t/intel-ucode.img\ninitrd\t/initramfs-linux.img\n" string2="options root=" string3=$(lsblk -Po UUID /dev/sda2 | tr -d '"') && echo -e $string$string2$string3 rw
````

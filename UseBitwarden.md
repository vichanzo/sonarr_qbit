
```
docker run -it ubuntu bash

apt update
apt install wget

wget https://github.com/bitwarden/cli/releases/download/v1.21.1/bw-linux-1.21.1.zip

apt install unzip
unzip bw-linux-1.21.1.zip 
chmod +x bw
./bw login

```

```
export BW_SESSION="T0XSMY...."
bw get attachment photo.png --itemid 99ee88d2-6046-4ea7-92c2-acac464b1412 --output /Users/myaccount/Pictures/
```

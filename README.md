# sonarr_qbit

Here's a quick start using Play-With-Docker (PWD) to very quickly set up a Sonarr-Qbittorrent-Jacket stack containing Prometheus, Grafana and Node scraper to monitor your Docker infrastructure. The Try in PWD below allows you to quickly deploy the stack with a click of the button.  In order to use this you will need a Docker login.

[![Try in PWD](https://github.com/play-with-docker/stacks/raw/master/assets/images/button.png)](https://labs.play-with-docker.com/?stack=https://raw.githubusercontent.com/vichanzo/sonarr_qbit/main/docker-compose.yml)


OK, I get it you might not trust me to just click a link in my GitHub.  If you prefer to do this the manual way, use the URL here to open "Play With Docker" then copy and paste the below commands.

Open https://labs.play-with-docker.com

Once you get to the command line, use these commands:
```
adduser -u 1000 -D sqbit
echo sqbit:aSecur3Passw0rd | chpasswd
git clone https://github.com/vichanzo/sonarr_qbit
cd sonarr_qbit/
docker-compose up -d
``` 

What does this do?
 1) "adduser -u 1000 -D sqbit":creates a user with UID 1000 with username sqbit
 2) "echo sqbit:aSecur3Passw0rd | chpasswd": changes the password to the sqbit user to "aSecur3Passw0rd".  (In fact I don't even think this step is needed.)
 3) "git clone https://github.com/vichanzo/sonarr_qbit": this will clone the github repository and create a folder in the current directory with the docker-compose.yml file.  This Docker-Compose has all the instructions to download the Dockers you need.
 4) "cd sonarr_qbit/  &&  docker-compose up -d": change into the folder then create the Docker Stack.

That's it.  After you finish this you can follow the guide by TechnoDadLife to set it up.  
     https://www.youtube.com/watch?v=5rtGBwBuzQE&t=710s 

     https://unraid-guides.com/2021/01/17/how-to-add-all-indexers-from-jackett-to-sonarr-and-radarr

How can I clone the testing branch?
```
git clone --branch testing https://github.com/vichanzo/sonarr_qbit
``` 

Key git commands
```
git config credential.helper store
git clone --branch testing https://github.com/vichanzo/sonarr_qbit
cd ~/sonarr_qbit
touch this_file.txt
git add this_file.txt
git commit -a -m "commit comment"
git push
``` 

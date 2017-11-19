# Docker-ubuntu

Ubuntu server details:

root@aimscare-devbox:/home/aimscare# lsb_release -a
No LSB modules are available.
Distributor ID:	Ubuntu
Description:	Ubuntu 16.04.3 LTS
Release:	16.04
Codename:	xenial

Docker Installation:

Docker version :  docker-ce_17.09.0~ce-0~ubuntu_amd64.deb  

Download deb file from  https://download.docker.com/linux/ubuntu/dists/xenial/pool/stable/amd64/

To clean/remove previous installation:

root@aimscare-devbox:/home/aimscare# sudo apt-get -y remove docker docker-engine

Install Docker using deb package:

root@aimscare-devbox:/home/aimscare# sudo dpkg -i docker-ce_17.09.0-ce-0-ubuntu_amd64.deb
Selecting previously unselected package docker-ce.
(Reading database ... 68185 files and directories currently installed.)
Preparing to unpack docker-ce_17.09.0-ce-0-ubuntu_amd64.deb ...
Unpacking docker-ce (17.09.0~ce-0~ubuntu) ...
dpkg: dependency problems prevent configuration of docker-ce:
 docker-ce depends on libltdl7 (>= 2.4.6); however:
  Package libltdl7 is not installed.

dpkg: error processing package docker-ce (--install):
 dependency problems - leaving unconfigured
Processing triggers for systemd (229-4ubuntu19) ...
Processing triggers for ureadahead (0.100.0-19) ...
Processing triggers for man-db (2.7.5-1) ...
Errors were encountered while processing:
 docker-ce

root@aimscare-devbox:/home/aimscare# sudo apt-get install libltdl7

root@aimscare-devbox:/home/aimscare# sudo dpkg -i docker-ce_17.09.0-ce-0-ubuntu_amd64.deb
(Reading database ... 68396 files and directories currently installed.)
Preparing to unpack docker-ce_17.09.0-ce-0-ubuntu_amd64.deb ...
Unpacking docker-ce (17.09.0~ce-0~ubuntu) over (17.09.0~ce-0~ubuntu) ...
Setting up docker-ce (17.09.0~ce-0~ubuntu) ...
Processing triggers for systemd (229-4ubuntu19) ...
Processing triggers for ureadahead (0.100.0-19) ...
Processing triggers for man-db (2.7.5-1) ...


root@aimscare-devbox:/home/aimscare# sudo docker run hello-world




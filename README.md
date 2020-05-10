# IIEC_Docker_Project_on_OwnCloud

Under IIEC-RISE 1.0 Campaign I learnt Docker from basic to advanced under the training of Vimal Daga Sir. This is my final project using Docker to set-up OwnCloud server

**Requirements:**

   * Operating System- I have used RedHat 8
   
   * Docker installed
   
   * Docker-compose downloaded
   
**In case of connectivity issues:**

      iptables -F 
      iptables -P FORWARD ACCEPT 


      firewall-cmd  --zone=trusted  --change-interface=docker0  --permanent
      firewall-cmd  --zone=trusted --add-masquerade  --permanent
      firewall-cmd  --add-port=3306/tcp
      firewall-cmd  --reload 
      
      systemctl restart docker 

**Steps:**
* clone this repository in your system
* start docker using

      systemctl start docker
* make a new folder for docker-compose

      mkdir <folder_name>
* copy paste the docker-compose.yml file from the repository
      
      cd <folder_name>
      ls
      docker-compose.yml
* start docker-compose

      docker-compose up
* now the owncloud server is ready and can be accessed through any device with LAN connectivity
you can access it using your IP or localhost

---your own owncloud server is setup!!!----

all the required images (MariaDB,Redis,owncloud) will be downloaded by the docker-compose itself
> Screenshots of these steps are also provided of the above steps     
    
    

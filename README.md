# Zipkin:

### Once Docker is installed, spin a Zipkin Docker container:- 

```
     #docker run -d -p 9411:9411 openzipkin/zipkin
```     
### Install Java:-

   ```
     
    #apt-get  update
    
    #apt-get install -y default-jdk jq vim
    
    #java -version
    
  ```
     
### Install Zipkin:-

   ```
    #curl -sSL https://zipkin.io/quickstart.sh | bash -s
     
    #java -jar zipkin.jar
     
    #mkdir /opt/zipkin
     
    #mv zipkin.jar /opt/zipkin
     
    #ls /opt/zipkin
     
   ```   
### Create a group and user:-

  ```
    #groupadd -r zipkin
     
    #useradd -r -s /bin/false -g zipkin zipkin
     
    #chown -R zipkin:zipkin /opt/zipkin
  ```    
### Create Systemd Service:-
   
   ```
    #mv zipkin.service /etc/systemd/system/zipkin.service
     
    #systemctl daemon-reload
     
    #systemctl start zipkin.service
     
    #systemctl status zipkin.service
   ```
     
     
     
     

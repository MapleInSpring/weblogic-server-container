# Oracle-Weblogic11g-Docker

To build a container with weblogic server, take following steps:
1. `git clone git@github.com:MapleInSpring/weblogic-server-container.git`
1. Download Java JDK [jdk-6u45-linux-x64.bin](https://www.oracle.com/technetwork/java/javase/downloads/java-archive-downloads-javase6-419409.html) to local folder
1. Download Weblogic server [wls1036_generic.jar](https://www.oracle.com/technetwork/middleware/ias/downloads/wls-main-097127.html) to local folder
1. `docker build . -t weblogic-server`
1. `docker run -d --name myweblogic -e base_domain_default_password=@1password -p 7001:7001 weblogic-server`
1. `docker logs myweblogic`

If everything goes well, then access the admin console by `http://localhost:7001/console`

Username: weblogic
Password: 123456

### OS
* This image uses [Debian][1] 8 _(jessie)_.

### Content
* [Oracle Java][2]: JDK & JRE
  * [Java 8][3]

### Tags
* [8.0.43]

### Run
* Simple:
`docker run -d celiasaidani/tomcat`
* Exposed:
`docker run -it --name=tomcatInstance -p 8081:8080 celiasaidani/tomcat`

### For testing with mySql (Prod instance)
`docker network connect prod-network tomcatInstance`

### Access
* The server should be accessible from `http://localhost:8081`.
* Tomcat Web Application Manager: `http://localhost:8081/manager/html` (default username/password: tomcat/s3cret)


[1]: https://hub.docker.com/_/debian/
[2]: https://hub.docker.com/r/celiasaidani/java8/
[3]: https://github.com/celiaSaidani/Dockerfiles/tree/java8


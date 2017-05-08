### OS
* This image uses [Debian][1] 8 _(jessie)_.

### Content
* Mysql ``

### Run

## Create Dockerfile
* Create a Dockerfile from celiasaidani/maven:onbuild (for testing java+maven)
* Build the image:
`docker build -t mavenonbuild .`
* Run an instance test of the image:
`docker run -it --name mevenOnBuild mavenonbuild`

* Create a Dockerfile from celiasaidani/maven
* Build the image: 
`docker build -t maven .`
* Run an instance of the image:
`docker run -it --name mavenInstance maven`

## For testing (java+maven) with mysql: uses test-network
`docker run -it --rm --name my-maven-project -v "$PWD":/usr/src/maven -w /usr/src/maven --net=test-network  celiasaidani/maven mvn clean test`

### Credit
Based on [official] maven repository. 
(Only difference, this image is using Oracle JDK instead of OpenJDK).

[1]: https://hub.docker.com/_/debian/
[2]: https://hub.docker.com/_/maven/

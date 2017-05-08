### OS
* This image uses [Debian][1] 8 _(jessie)_.

### Content
* Oracle Java _8_ : JDK & JRE.
* Maven `3.5`

### Run

## Create Dockerfile
* Create a Dockerfile from celiasaidani/maven:onbuild
* Build the image:
`docker build -t mavenonbuild .`
* Run an instance of the image:
`docker run -it --name mavenOnbuildInstance mavenonbuild`

* Create a Dockerfile from celiasaidani/maven
* Build the image:
`docker build -t maven .`
* Run an instance of the image:
`docker run -it --name mavenInstance maven`

## For testing (java+maven) with mysql: uses Test-network
docker run -it --rm --name my-maven-project -v "$PWD":/usr/src/maven -w /usr/src/maven --net=Test-network  celiasaidani/maven mvn clean test

### Credit
Based on [official] maven repository. 
(Only difference, this image is using Oracle JDK instead of OpenJDK).

[1]: https://hub.docker.com/_/debian/
[2]: https://hub.docker.com/_/maven/

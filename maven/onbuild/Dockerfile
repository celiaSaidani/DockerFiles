
FROM celiasaidani/maven

RUN mkdir -p /usr/app/src

ONBUILD ADD ./src /usr/app/src \&&
		ADD ./pom.xml /usr/app
WORKDIR /usr/app

RUN mvn clean package
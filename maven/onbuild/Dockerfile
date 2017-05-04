
FROM celiasaidani/maven

RUN mkdir -p /usr/app/src

ONBUILD ADD ./src /usr/app/src \&&
		ADD ./pom.xml /usr/app
RUN echo $JAVA_HOME

RUN mvn clean package
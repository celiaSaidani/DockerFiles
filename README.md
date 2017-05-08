### OS
* This image uses [Debian][1] 8 _(jessie)_.

### Content
* Mysql ``

### Run

## Create Dockerfile
* Build the image:
`docker build -t mysql .`
* Run an instance test of the image:
`docker run -d --name="mysql-Test" -e MYSQL_PASSWORD=password -p 3307:3306 mysql`
* insert table test in database:
`mysql -u <USER> -p<YOURPASSWORD> 127.0.0.1 -port=3306<./setup/1-SCHEMA.sql`
`mysql -u <USER> -p<YOURPASSWORD> 127.0.0.1 -port=3306<./setup/2-PRIVILEGES.sql`
`mysql -u <USER> -p<YOURPASSWORD> 127.0.0.1 -port=3306<./setup/3-ENTRIES.sql`
* Run an instance Prod of the image:
`docker run -d --name="mysql-Prod" -e MYSQL_PASSWORD=password -p 3307:3306 mysql`
* insert table test in database:
`mysql -u <USER> -p<YOURPASSWORD> 127.0.0.1 -port=3306<./setup/1-SCHEMA.sql`
`mysql -u <USER> -p<YOURPASSWORD> 127.0.0.1 -port=3306<./setup/2-PRIVILEGES.sql`

### Credit
Based on [official] maven repository. 
(Only difference, this image is using Oracle JDK instead of OpenJDK).

[1]: https://hub.docker.com/_/debian/
[2]: https://hub.docker.com/_/maven/

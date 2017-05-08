### OS
* This image uses [Debian][1] 8 _(jessie)_.

### Content
* Mysql ``

### Run

## Create Dockerfile
* Build the image:
`docker build -t mysql .`
* Run an instance test of the image:
`docker run -d --name="mysql-Test" -e MYSQL_PASSWORD=password -p 3307:3306 mysql`<br />
* insert table test in database:<br />
`mysql -u <USER> -p<YOURPASSWORD> 127.0.0.1 -port=3306<./setup/1-SCHEMA.sql`<br />
`mysql -u <USER> -p<YOURPASSWORD> 127.0.0.1 -port=3306<./setup/2-PRIVILEGES.sql` <br />
`mysql -u <USER> -p<YOURPASSWORD> 127.0.0.1 -port=3306<./setup/3-ENTRIES.sql`<br />
* Run an instance Prod of the image:<br />
`docker run -d --name="mysql-Prod" -e MYSQL_PASSWORD=password -p 3307:3306 mysql`
* insert table test in database:<br />
`mysql -u <USER> -p<YOURPASSWORD> 127.0.0.1 -port=3306<./setup/1-SCHEMA.sql`<br />
`mysql -u <USER> -p<YOURPASSWORD> 127.0.0.1 -port=3306<./setup/2-PRIVILEGES.sql` <br />

### Credit
Based on [official] maven repository. 
(Only difference, this image is using Oracle JDK instead of OpenJDK).

[1]: https://hub.docker.com/_/debian/
[2]: https://hub.docker.com/_/maven/

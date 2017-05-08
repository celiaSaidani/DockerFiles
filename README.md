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
### Docker network for testing with maven
`docker network create test-network`<br />
`docker network connect test-network mysql-Test`<br />

### Docker network for testing with tomcat
`docker network create prod-network`<br />
`docker network connect prod-network mysql-Prod`<br />



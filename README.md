# BCtrade

A blockchain-based(hyperledger) web application built by vue+springboot

# Quick Start

## prerequisite

nodejs

webpack-dev-server

node_modules

maven



## web application

locate to the directory, download the dependencies and use npm run command 

```shell
$ cd front
$ sudo npm install #be patient, It's going to take a while
$ # if permissions denied in mkdir, try the following command
$ # npm install --unsafe-perm
$ sudo npm run dev
```



## backend

```shell
$ cd backend
$ mvn package -DskipTests
$ if maven version is not greater than 3.2.0, please follow the guides in https://blog.csdn.net/qq_38974638/article/details/112784951
$ mvn test -Dtest=AddAccountTest#enrollAdminTest
$ java -jar target/demo-0.0.1-SNAPSHOT.jar
$ #if the system shows no main manifest run the following command
$ # java -cp target/demo-0.0.1-SNAPSHOT.jar com.example.demo.DemoApplication
$ # 
```



### api

```yaml
#Register service, the registered user information is placed in the body, the example is as follows
register:
http://localhost:8999/admin/register
body:
{
  "id":"114514",
  "username":"luojun",
  "password":"1919810",
  "available":"true",
  "role":"user",
  "regtime":" "
}

#Login service
login:
	http://localhost:8999/admin/login?username=bt&password=bt
	username和password是请求的参数
	
#Log out	
logout:
	http://localhost:8999/admin/logout	

#Permission test: The user whose permission is user requests the api to receive hello messages
hello:
	http://localhost:8999/admin/hello
	
#Permission test: Users with permission to admin request that the api will receive hello messages.
ahello:
	http://localhost:8999/admin/ahello
```


# Lab :: Hello World :: Spring Boot Application

[![Build Status](https://travis-ci.org/odaceo/lab-hello-world-spring-boot.svg)](https://travis-ci.org/odaceo/lab-hello-world-spring-boot)
[![License](https://img.shields.io/github/license/odaceo/lab-hello-world-spring-boot.svg)](LICENSE)

## Description

A Simple web application with Spring Boot.

## Prerequisites

As craftsmen we love crafting software on a clean workbench. 

We believe that a clean workbench helps us focus on what really matters: 
_handcrafting every design and code with great care_. 

[Vagrant](https://www.vagrantup.com/) helps us create such a workbench and install 
the prerequisites, and nothing more.

As a benefit, we keep our workbench as clean as possible over time.  

[Vagrant](https://www.vagrantup.com/downloads.html) must be installed on your 
computer to mount the workbench for this project.

Open a Terminal and run the following commands:

```shell
vagrant up
vagrant ssh
cd /vagrant
```

## Building the application

The build command creates a standalone JAR file.

``` shell
mvn clean package
```

## Running the application

To launch the application use the following command:

``` shell
java -jar target/hello-world-0.5.1.jar
```

To run the service use the following command: 

``` shell
curl http://localhost:8080/greeting?name=Alexandre
```

To check the application's health use the following command:

``` shell
curl http://localhost:9090/health
```

## Releasing the application

Step-by-step instructions for releasing the application:

1. Start a new release

        git flow release start 0.6.0

1. Bump the version number

        mvn versions:set -DnewVersion=0.6.0 

1. Update the documentation

1. Commit pending changes

        git commit -am "Bump the version number"

1. Finish the release

        git flow release finish -m "Release 0.6.0" 0.6.0
  
Make sure all artifacts have been successfully uploaded to [Bintray](https://bintray.com/odaceo/maven/lab-hello-world-spring-boot).

## Reporting Issues

Issues can be reported at [https://github.com/odaceo/lab-hello-world-spring-boot/issues](https://github.com/odaceo/lab-hello-world-spring-boot/issues)

## Source code

The source code is available at [https://github.com/odaceo/lab-hello-world-spring-boot](https://github.com/odaceo/lab-hello-world-spring-boot)

## License

All the source code is distributed under [ASL 2.0](LICENSE).

## Copyright

© 2015 [Odaceo](http://odaceo.ch). All rights reserved.

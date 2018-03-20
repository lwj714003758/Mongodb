# MongoDB (start to learn MongoDB)

## Overview

Use this tutorial to install MongoDB Community Edition on Red Hat Enterprise Linux or CentOS Linux versions 6 and 7 using .rpm packages.

```
PLATFORM SUPPORT:
          This installation guide only supports 64-bit systems. See Platform Support for details.
     MongoDB 3.4 removes support for Red Hat Enterprise Linux 5.
```
- Install MongoDB On Linux
- MongoDB Shell
- MongoDB CRUB Operations

## Packages

MongoDB provides officially supported packages in their own repository. This repository contains the following packages:
 ```
     Package Name	Description

      mongodb-org	A metapackage that will automatically install the four component packages listed below.

mongodb-org-server	Contains the mongod daemon and associated configuration and init scripts.

mongodb-org-mongos	Contains the mongos daemon.

mongodb-org-shell	Contains the mongo shell.

mongodb-org-tools	Contains the following MongoDB tools: mongoimport bsondump, mongodump, mongoexport, mongofiles, mongoperf, mongorestore, mongostat, and mongotop.
```
*The mongodb-org-server package provides an initialization script that starts mongod with the /etc/mongod.conf configuration file.*

*The default /etc/mongod.conf configuration file supplied by the packages have bind_ip set to 127.0.0.1 by default. Modify this setting as needed for your environment before initializing a replica set.*

## Install MongoDB Community Edition


- Configure the package management system (yum).

*Create a /etc/yum.repos.d/mongodb-org-3.6.repo file so that you can install MongoDB directly, using yum.*

**For MongoDB 3.6**

```
[mongodb-org-3.6]
name=MongoDB Repository
baseurl=https://repo.mongodb.org/yum/redhat/$releasever/mongodb-org/3.6/x86_64/
gpgcheck=1
enabled=1
gpgkey=https://www.mongodb.org/static/pgp/server-3.6.asc
```

- Install the MongoDB Packages

*To install the latest stable version of MongoDB, issue the following command:*
  `sudo yum install -y mongodb-org ` 

*To install a specific release of MongoDB, specify each component package individually and append the version number to the package name, as in the following example:*

`sudo yum install -y mongodb-org-3.6.3 mongodb-org-server-3.6.3 mongodb-org-shell-3.6.3 mongodb-org-mongos-3.6.3 mongodb-org-tools-3.6.3`

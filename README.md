# MongoDB (start to learn MongoDB)

# Overview

- Install MongoDB On Linux
- MongoDB Shell
- MongoDB CRUB Operations

**Install MongoDB On Linux**
- Configure repository.
**Create an /etc/yum.repos.d/mongodb-enterprise.repo file so that you can install MongoDB enterprise directly, using yum.**

```
[mongodb-enterprise]
name=MongoDB Enterprise Repository
baseurl=https://repo.mongodb.com/yum/redhat/$releasever/mongodb-enterprise/3.6/$basearch/
gpgcheck=1
enabled=1
gpgkey=https://www.mongodb.org/static/pgp/server-3.6.asc
```
- Install the MongoDB Enterprise packages

**Install the 3.6 release candidate version of MongoDB Enterprise.**

**Issue the following command:**

    `sudo yum install -y mongodb-enterprise`
**Install a specific release of MongoDB Enterprise.**

**To install a specific release, you must specify each component package individually along with the version number, as in the following example:**

    `sudo yum install -y mongodb-enterprise-3.6.3 mongodb-enterprise-server-3.6.3 mongodb-enterprise-shell-3.6.3 mongodb-enterprise-mongos-3.6.3 mongodb-enterprise-tools-3.6.3`

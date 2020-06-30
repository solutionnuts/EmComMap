===============
Install CouchDB
===============

CouchDB can be installed on Linux, Mac and Windows. CouchDB can also be installed in **Standalone** or **Clustered** mode. We will just cover a Linux standalone installation in this document. For more information on Mac and Windwos or creating a clustered installation, please visit the official `CouchDB website <https://couchdb.apache.org>`_.

If you are running one of the following versions of Linux, the easiest way to install is using the binary packages.

* Debian 9 (stretch)
* Debian 10 (buster)
* Ubuntu 16.04 (xenial)
* Ubuntu 18.04 (bionic)
* Ubuntu 20.04 (focal)
* CentOS/RHEL 6
* CentOS/RHEL 7
* CentOS/RHEL 8

Debian 9 (stretch)
------------------

1. Start by enabling the Apache CouchDB package repository.

    $ sudo apt-get install -y apt-transport-https gnupg ca-certificates
    
    $ echo "deb https://apache.bintray.com/couchdb-deb stretch main" | sudo tee /etc/apt/sources.list.d/couchdb.list
    
2. Install the CouchDB GPG key

    $ sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 8756C4F765C9AC3CB6B85D62379CE192D401AB61
    
3. Update the repository and install the CouchDB package

    $ sudo apt update

    $ sudo apt install -y couchdb

Debian 10 (buster)
------------------



Ubuntu 16.04 (xenial)
---------------------



Ubuntu 18.04 (bionic)
---------------------



Ubuntu 20.04 (focal)
--------------------


CentOS/RHEL 6
-------------


CentOS/RHEL 7
-------------


CentOS/RHEL 8
-------------



Docker
------

**COMING SOON!**

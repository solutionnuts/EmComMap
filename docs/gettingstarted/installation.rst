=====================
EmComMap Installation
=====================

* App can be encrypted (https) or unencrypted (http) which is required for amateur radio
* Can be installed on any webserver whether internet facing or private (ex. MESH networking)
* Relies on three server platforms, each of which can be deployed redundantly to avoid single points of failure

    - CouchDB
    - Map tile server
    - Web server (e.g. Apache2 or nginx)


Install CouchDB
---------------

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
++++++++++++++++++

1. Start by enabling the Apache CouchDB package repository ::

    $ sudo apt-get install -y apt-transport-https gnupg ca-certificates
    $ echo "deb https://apache.bintray.com/couchdb-deb stretch main" | sudo tee /etc/apt/sources.list.d/couchdb.list
    
2. Install the CouchDB GPG key ::

    $ sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 8756C4F765C9AC3CB6B85D62379CE192D401AB61
    
3. Update the repository and install the CouchDB package ::

    $ sudo apt update
    $ sudo apt install -y couchdb

Debian 10 (buster)
++++++++++++++++++

1. Start by enabling the Apache CouchDB package repository ::

    $ sudo apt-get install -y apt-transport-https gnupg ca-certificates
    $ echo "deb https://apache.bintray.com/couchdb-deb buster main" | sudo tee /etc/apt/sources.list.d/couchdb.list
    
2. Install the CouchDB GPG key ::

    $ sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 8756C4F765C9AC3CB6B85D62379CE192D401AB61
    
3. Update the repository and install the CouchDB package ::

    $ sudo apt update
    $ sudo apt install -y couchdb

Ubuntu 16.04 (xenial)
+++++++++++++++++++++

1. Start by enabling the Apache CouchDB package repository ::

    $ sudo apt-get install -y apt-transport-https gnupg ca-certificates
    $ echo "deb https://apache.bintray.com/couchdb-deb xenial main" | sudo tee /etc/apt/sources.list.d/couchdb.list
    
2. Install the CouchDB GPG key ::

    $ sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 8756C4F765C9AC3CB6B85D62379CE192D401AB61
    
3. Update the repository and install the CouchDB package ::

    $ sudo apt update
    $ sudo apt install -y couchdb

Ubuntu 18.04 (bionic)
+++++++++++++++++++++

1. Start by enabling the Apache CouchDB package repository ::

    $ sudo apt-get install -y gnupg ca-certificates
    $ echo "deb https://apache.bintray.com/couchdb-deb bionic main" | sudo tee /etc/apt/sources.list.d/couchdb.list
    
2. Install the CouchDB GPG key ::

    $ sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 8756C4F765C9AC3CB6B85D62379CE192D401AB61
    
3. Update the repository and install the CouchDB package ::

    $ sudo apt update
    $ sudo apt install -y couchdb

Ubuntu 20.04 (focal)
++++++++++++++++++++

1. Start by enabling the Apache CouchDB package repository ::

    $ sudo apt-get install -y gnupg ca-certificates
    $ echo "deb https://apache.bintray.com/couchdb-deb focal main" | sudo tee /etc/apt/sources.list.d/couchdb.list
    
2. Install the CouchDB GPG key ::

    $ sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 8756C4F765C9AC3CB6B85D62379CE192D401AB61
    
3. Update the repository and install the CouchDB package ::

    $ sudo apt update
    $ sudo apt install -y couchdb

CentOS
++++++

1. Start by enabling the Apache CouchDB package repository. Place the following text into ``/etc/yum.repos.d/bintray-apache-couchdb-rpm.repo`` ::

        [bintray--apache-couchdb-rpm]
        name=bintray--apache-couchdb-rpm
        baseurl=http://apache.bintray.com/couchdb-rpm/el$releasever/$basearch/
        gpgcheck=0
        repo_gpgcheck=0
        enabled=1
    
2. Update the repository and install the CouchDB package ::

       $ sudo yum -y install epel-release && sudo yum -y install couchdb
    
RHEL 7
++++++

1. Start by enabling the Apache CouchDB package repository. Place the following text into ``/etc/yum.repos.d/bintray-apache-couchdb-rpm.repo`` ::

    [bintray--apache-couchdb-rpm]
    name=bintray--apache-couchdb-rpm
    baseurl=http://apache.bintray.com/couchdb-rpm/el6/$basearch/
    gpgcheck=0
    repo_gpgcheck=0
    enabled=1

2. Update the repository and install the CouchDB package ::

    $ sudo yum -y install epel-release && sudo yum -y install couchdb

RHEL 7
++++++

1. Start by enabling the Apache CouchDB package repository. Place the following text into ``/etc/yum.repos.d/bintray-apache-couchdb-rpm.repo`` ::

    [bintray--apache-couchdb-rpm]
    name=bintray--apache-couchdb-rpm
    baseurl=http://apache.bintray.com/couchdb-rpm/el7/$basearch/
    gpgcheck=0
    repo_gpgcheck=0
    enabled=1
    
2. Update the repository and install the CouchDB package ::

    $ sudo yum -y install epel-release && sudo yum -y install couchdb

RHEL 8
++++++

1. Start by enabling the Apache CouchDB package repository. Place the following text into ``/etc/yum.repos.d/bintray-apache-couchdb-rpm.repo`` ::

    [bintray--apache-couchdb-rpm]
    name=bintray--apache-couchdb-rpm
    baseurl=http://apache.bintray.com/couchdb-rpm/el8/$basearch/
    gpgcheck=0
    repo_gpgcheck=0
    enabled=1

2. Update the repository and install the CouchDB package ::

    $ sudo yum -y install epel-release && sudo yum -y install couchdb

Docker
++++++

**COMING SOON!**

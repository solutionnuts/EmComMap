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
* CentOS

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

Docker
++++++

**COMING SOON!**

Install Map Tile Server
-----------------------

**Docker is required to install the map tile server**

Maps are powered by OpenStreeMap data. They are ready to use and not need to render the tiles after download.

1. Install Docker with the following command ::

    $ curl -sSL https://get.docker.com/ | sh
    
2. Make a directory to store your map tile file and then change directory to it ::

    $ mkdir openmaptiles       (or whatever you want to name the directory)
    $ cd openmaptiles
    
3. Launch a Docker container with the following command. It will download the OpenMapTiles-Server container image from the Docker Hub and launch the OpenMapTiles-Server container in **detached** mode and will restart the container when system is rebooted for any reason. Detached mode allows the program to launch without leaving a terminal window open. ::

    $ docker run -dit --name <disiredservername> -v $(pwd):/data -p 8080:80 --restart always klokantech/openmaptiles-server

.. warning:: The Docker OpenMapTiles container **MUST** be run from the directory you created above.

|

.. image:: _images/OpenMapTiles_Configure_1.png
    :alt: OpenMapTiles Setup Screen
    :align: right

4. Open a web browser and navigate to **http://<hostname or IP>:8080/** and click **START**

|
|
|
|
|
|
|
|
|

.. image:: _images/OpenMapTiles_Configure_2.png
    :alt: OpenMapTiles Setup Screen
    :align: right

5. Select the region that you want to install the tiles for and then click **CONTINUE**.  Most regions will require you to setup a free account on the `OpenMapTiles website <https://openmaptiles.org>`_

|
|
|
|
|
|
|

.. image:: _images/OpenMapTiles_Configure_3.png
    :alt: OpenMapTiles Setup Screen
    :align: right
    
6. Uncheck all but **Klokantech Basic** and click **CONTINUE**

|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|

.. image:: _images/OpenMapTiles_Configure_6.png
    :alt: OpenMapTiles Setup Screen
    :align: right
    
7. Click **Click here to get the download key**. You will be taken to the OpenMapTiles site. It will walk you through signing up for a free account if you don't already have one and then provide you with a **DOWNLOAD KEY**. Copy and paste it into the form and click **START DOWNLOAD**.

8. Once the download has completed, click **OPEN SERVER**.

Install Web Server
------------------

You can run whichever webserver you like but we will be using Apache2 for this example.

Ubuntu/Debian
+++++++++++++

1. Run the following command to install **Apache2** ::

    $ sudo apt install -y httpd

2. Change directory to ``/var/www/html`` and download EmComMap ::

    $ cd /var/www/html
    $ sudo git clone https://github.com/DanRuderman/EmComMap.git

3. Restart the Apache2 webserver ::

    $ sudo apache2ctl restart

CentOS
++++++

1. Run the following commands to update the **httpd** package index and install **httpd** (Apache2) ::

    $ sudo yum update httpd
    $ sudo yum install httpd

2. Start your web server. Apache does not start automatically on CentOS once the installation completes. ::
    
    $ sudo systemctl start httpd
    
3. Confirm Apache is running ::
    
    $ sudo systemctl status httpd

Docker
++++++

**COMING SOON**

EmComMap Configuration
----------------------

1. Open the file ``/var/www/html/EmComMap/html/config.js`` in a text editor ::

    $ sudo vim /var/www/html/EmComMap/html/config.js
    
2. Towards the top of the file you will see these lines ::

    const RUN_LOCATION = "local";

    if(RUN_LOCATION == "my-install") {
        var TILE_SERVER = 'http://<host>:8080/styles/klokantech-basic/{z}/{x}/{y}.png';
        var TILE_SERVER_OPTS = {
        maxZoom: 18,
        attribution: 'Map data &copy; <a href="https://www.openstreetmap.org/">OpenStreetMap</a> contributors, ' +
            '<a href="https://creativecommons.org/licenses/by-sa/2.0/">CC-BY-SA</a>, ' +
            'Server courtesy of <a href="https://openmaptiles.com/">OpenMapTiles</a>'
        };
        var DEFAULT_DB_HOST = '<host>';
        
3. Change the **RUN_LOCATION** string to ``my-install`` instead of ``local``

4. Change both instances of ``<host>`` to the hostname or IP of your EmComMap server.

.. note:: If you have the CouchDB server on a different computer, then you will need to use that computer's address for **DEFAULT_DB_HOST**.


Spark Playground
-----

This vagrant box will install a single-instance Apache Spark 2.0.0, on Ubuntu 14.04, with JDK 8.

To start the vagrant box, simply install Vagrant and VirtualBox, then run this command:

```
vagrant up
```

This will set up a virtual machine with the following configurations:

* Ubuntu 16.04 
* Apache Spark 2.0.0
* JDK 8
* Static IP address: 192.168.0.25, ports mapped to 8080 and 7077 for Spark

The Spark is installed under path `/spark`

## Start Spark

# Login to the virtual machine:
```
vagrant ssh
```

# Start Spark cluster
```
/spark/sbin/start-all.sh
```
You may need to enter the user password for "vagrant", which is default to "vagrant".

# Verify Spark is started and healthy
Go to local browser and browse to `http://localhost:8081`. The Spark web UI should show up.

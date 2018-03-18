Tomcat native installation
==========================

This ansible playbook will install Tomcat native and it's dependency (Openssl and APR) from source.


Source
------

All source are already there in source directory. If you want to install a different version of these packages, then download and copy it under same directory. But, you will also need to modify env.yml file by proving new name of these source tar ball file name.

Installation Path
-----------------

It will copy source from ansible system to target server under /usr/src and also untar in the same directory for build.

Then, it will install openssl and apr in /opt/libs directory. After that it will build and install tomcat native in /opt/tomcat-native.

**Note:** It will also create a backup of already installed libs and tomcat-native by adding .old as suffix.

Installation Steps
------------------

Run below command by replacing host address and domain user account.

**ansible-playbook -i \<host name or ip>, -u \<domain user> install.yml**
  
**Note:** There is a comma after host address.

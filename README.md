# Getting Started with Spark using Scala

## Installation
1. Download and install [git](https://git-scm.com/downloads).
2. Clone gsss project from Git [repository](https://github.com/skomarovsky/gsss)
3. Download or upgrade Java JDK to latest [version](http://www.oracle.com/technetwork/java/javase/downloads/index.html) of SE Developer Kit.
4. Download or upgrade sbt to latest [version](https://www.scala-sbt.org/1.x/docs/Installing-sbt-on-Windows.html).
5. Download Docker community edition for [Windows](https://store.docker.com/editions/community/docker-ce-desktop-windows). You must to use version of
Docker which is support of Windows installed on your computer version. 
    
## Starting Spark Standalone cluster
1. Find and start <B>Docker Quickstart terminal</b>. It will start Docker Virtual Box machine.
2. From Windows command prompt change folder to the <font color="green">gsss/docker</font> folder.
3. Type *docker-compose up*. You can monitor startup process in <B>Docker Quickstart terminal</b>

## Connecting to the cluster
1. Open new windows command prompt.
2. Check if cluster up and running, type *docker ps*.
![result](docs/images/dockerps.png)
If you can find both docker_master_1 and docker_worker_1 than your Spark cluster up and runing.
3. Type *docker run -i -t docker_master_1 /bin/bash*
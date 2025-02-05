[![Build Status](https://travis-ci.org/hasalex/eap-build.svg)](https://travis-ci.org/hasalex/eap-build)

Building JBoss EAP 6, or something similar...

Why ?
=====
As I'm not able to build JBoss EAP 6, I've made a script who can download JBoss EAP 6's source code, download it's Maven repository, patch the repository and launch the build.

The result won't be a JBoss EAP 6 binary but something with a few differences.

How ?
=====
You can get the build script with git or wget.

With git
--------
If you want to run the script :

    git clone git://github.com/hasalex/eap-build.git
    cd eap-build
    ./build-eap.sh

By default, it builds EAP 6.4.5. You can build other versions by passing the number to the build :

    ./build-eap.sh 6.2.2

Without git
-----------
If you don't want to use git, download the archive, unzip it and run the main script :

    wget https://github.com/hasalex/eap-build/archive/master.zip
    unzip master.zip
    cd eap-build-master
    ./build-eap.sh

Versions
--------
For the moment, it supports 6.2.0, 6.2.1, 6.2.2, 6.2.3, 6.2.4, 6.3.0, 6.3.1, 6.3.2, 6.3.3, 6.4.0, 6.4.1, 6.4.2, 6.4.3, 6.4.4, 6.4.5, 7.0.0-alpha.

For older versions (6.0.x, 6.1.x), you'll have to checkout the matching tag.

Prerequisite and systems supported
==================================
The script is in bash. It should run on almost all bash-compatible systems. You have to install **wget**, **unzip**, **patch** and **java (JDK)** first.

It has been tested on the following systems :
* MacOS X 10.7 and 10.9
* CentOS 6.4    after "yum install wget unzip java-1.6.0-openjdk java-1.6.0-openjdk-devel"
* Ubuntu 12.04  after "apt-get install openjdk-6-jdk"
* Fedora 20, 21, 22

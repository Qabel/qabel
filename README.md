# Qabel documentation
For the documentation take a look at the [wiki](https://github.com/Qabel/qabel-doc/wiki/Table-of-contents) in our documentation [repository](https://github.com/Qabel/qabel-doc).

qabel
=====

Gradle superproject for all Qabel projects.

## requirements

0. redis-server

0. nodejs

0. npm

0. python moduls from qabel-drop/requirements.txt

## building source

0. Make sure you have a working [git client](http://git-scm.com/) installed

0. clone the source
   ```
   git clone https://github.com/Qabel/qabel.git
   cd qabel
   git submodule init
   git submodule update
   ```
   
0. build the project
   ```
   ./gradlew build
   ```


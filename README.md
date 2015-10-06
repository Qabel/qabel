# Qabel documentation
For the documentation take a look at the [wiki](https://github.com/Qabel/qabel-doc/wiki/Table-of-contents) in our documentation [repository](https://github.com/Qabel/qabel-doc).

qabel
=====

[![Build Status](https://travis-ci.org/Qabel/qabel.svg?branch=master)](https://travis-ci.org/Qabel/qabel)

Gradle superproject for all Qabel projects.

## requirements

0. redis-server

0. nodejs

0. npm

0. python3.4

0. python moduls from qabel-drop/requirements.txt
   ```
   this could for example automaticly be done using python-pip:
      pip install -r qabel-drop/requirements.txt
   ```

0. python modules from qabel-accounting/requirements.txt
   ```
   virtualenv --python=python3.4 qabel-accounting
   source qabel-accounting/bin/activate
   pip install -r qabel-drop/requirements.txt
   ```

0. migrations for qabel-accounting
   ```
   cd qabel-accounting
   ./manage.py migrate
   ```

0. lsof (Linux only)

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

## starting the Servers
Normaly the drop and storage server should be started automaticaly, but if you would like to start the servers manually you need to do the following steps

0. dropserver
   ```
   linux:
     ./qabel-drop/drop_server.py
  
   windows:
     python ./qabel-drop/drop_server.py
   ```
0. storage-server
   ```
   cd qabel-storage
   npm install
   
   linux:
      nodejs app.js

   windows
      node app.js
   ```

0. accounting-server
   ```
   cd qabel-accounting
   bin/python3.4 manage.py runserver
   ```
   

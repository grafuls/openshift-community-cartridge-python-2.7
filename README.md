openshift-community-cartridge-python-2.7
========================================

This git repository is a community supported cartridge to help you get
started with using Python-2.7 on Red Hat's OpenShift PaaS. 


Steps to create a Python 2.7 app on OpenShift
---------------------------------------------

Create an account at http://openshift.redhat.com/

Create a namespace, if you haven't already do so

    rhc domain create -n <yournamespace>

Create a python-2.7 application (you can name it anything via -a)

    rhc app create -a pecanpie -t python-2.7


Template Sample Application Caveats
-----------------------------------

The default template application is optimized for app creation times/speed
and so will run a simple WSGI HTTP server on app creation. 
For more details, see: http://docs.python.org/2/library/wsgiref.html#module-wsgiref.simple_server

And on a first git push (without any code/setup modifications), the app
template's setup.py will install greenlet and gevent and run the app with
a fast WSGI server based on libevent-http (from gevent).
For more details, see: http://www.gevent.org/  



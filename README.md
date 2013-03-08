CF Kettle
=========

My own version of Dr Nic's DIY PaaS. Borrows some of his scripts/config files.

Runs nats, dea, stager and cloud_controller and let's you deploy an application using vmc

Getting started
---------------

# Pick a domain name, e.g. mycf.me
# Edit /etc/hosts to resolve api.mycf.me to 127.0.0.1
# Edit config/cloud_controller/cc_config and edit the external_uri property: e.g. mycf.me:9022
# Configure redis to run on port 5454 or edit redis/port in cc_config
# Run 'rake bundle_install'
# Run 'foreman start' to start everything
# Run 'vmc target http://api.mycf.me:9022'
# Run 'vmc register' to create a user
# Deploy an Node or Ruby application. vmc push hangs checking for the app's status but the app is running so control-c.

Currently there is no router so the application can only be accessed directly

TODOS
-----

Add more components including a router.

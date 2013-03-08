CF Kettle
=========

My own version of Dr Nic's DIY PaaS. Borrows some of his scripts/config files.

Runs nats, dea, stager and cloud_controller and let's you deploy an application using vmc

Getting started
---------------

1. Pick a domain name, e.g. mycf.me
2. Edit /etc/hosts to resolve api.mycf.me to 127.0.0.1
3. Edit config/cloud_controller/cc_config and edit the external_uri property: e.g. mycf.me:9022
4. Configure redis to run on port 5454 or edit redis/port in cc_config
5. Run 'rake bundle_install'
6. Run 'foreman start' to start everything
7. Run 'vmc target http://api.mycf.me:9022'
8. Run 'vmc register' to create a user
9. Deploy an Node or Ruby application. vmc push hangs checking for the app's status but the app is running so control-c.

Currently there is no router so the application can only be accessed directly

TODOS
-----

Add more components including a router.
